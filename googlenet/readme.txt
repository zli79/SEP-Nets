1. Instruction
   a. train original googlenet using train_val.prototxt and quick_solver.prototxt
      after training we obtain: bvlc_googlenet_quick_iter_600000.caffemodel
      
      you could reference log file: googlenet_train_quick_solver_from_scratch_zl.log

   b. quantilize 3x3, 5x5 or 3x3 and 5x5 filters we get three quantilize models
      For this step, we first fine-tune value to quantilize to from (0.02, 0.03, 0.04, 0.05 ,0.06, 0.07, 
	0.08,0.09), theoretically we could omit this step, but experimentally we did 
      3x3 filters: 0.06 
      5x5 filters: 0.05 
      3x3 and 5x5 filters: 0.06 
      1x1: 0.09 

      after this step we got the following models: 
	googlenet_600000_quant_3x3_0.06.caffemodel
        googlenet_600000_quant_5x5.caffemodel
        googlenet_600000_quant_3x3_5x5_0.06.caffemodel
	googlenet_600000_quant_projAll1x1_0.09.caffemodel
     
      using quant_pattern.py python file to do quantilization, you need to set qualizatio value, 
	(off_set if x > 0 else -off_set)      
   c. fine-tuning the above models with train_val_fix_xxx_pattern.prototxt and 
      quick_solver_fix_xxx_pattern.prototxt (for example, 3x3 case, we keep 3x3 quantilized
	filters, you could see that in train_val_fix_3x3_pattern.prototxt file, we set learning
	rate for that 3x3 convolutional layer as 0) 

      After fine-tuning we obtain model files:
      googlenet_fine_tune_quant_600000_caffemodel_fix_3x3_pattern_iter_600000.caffemodel
      googlenet_fine_tune_quant_600000_caffemodel_fix_5x5_pattern_iter_600000.caffemodel
      googlenet_fine_tune_quant_600000_caffemodel_fix_3x3_5x5_pattern_iter_600000.caffemodel




     
