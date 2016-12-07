1、procedure存储过程调试
  
  直接在命令行里CALL ProcedureXXXX,然后select @o_var1, @o_var2;
  例如：
  存储过程为
   create procedure ProcedureXXXX(IN i_user_id INT, OUT o_var1, OUT o_var2)
   BEGIN
        .........
   END$$
   
   那么在命令行里调试就是 CALL ProcedureXXXX（'xxxxxx', @o_var1, @o_var2);
   然后 select @o_var1, @o_var2
   
