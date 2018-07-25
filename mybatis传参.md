@Param("customid")

<if test="_parameter.get(2).id != null">

 {arg1=10, arg0=0, param3=1, customid=1, param1=0, param2=10}
 
 Result Maps collection does not contain value报错
 resultMap 改成 resultType（自定义的和基本类型） mapper 里面可以是集合
 
 存储过程中有 select 1 则mybatis配置返回值 resultType="int"
 max（$）可以传数据库不同字段
 max（$）会加上''
 
 <if test="_parameter.get(1)!= null">
 
  <if test="_parameter.get(2)!= null">
  
  
  <if test="customid != null">
  
  Error evaluating expression '_parameter.get(1)!= null'. 
  
  Cause: org.apache.ibatis.ognl.MethodFailedException: Method "get" failed for object
  {arg2=10, arg1=0, arg0=558, param3=10, param1=558, param2=0} [org.apache.ibatis.binding.BindingException:
  
  Parameter '1' not found. Available parameters are [arg2, arg1, arg0, param3, param1, param2]]
  
  
  可以修改的地方
  
  SELECT max(avgMemory) as maxavgMemory,model ,min(avgMemory) ,packName
	from script_dfx_measure 
 where   packName='com.cnfastvpn' and type='model'
GROUP BY model


<select id="querydfxmeasureBypackNamea" parameterType="Map" resultType="Map"> 修改这些重复得sql

@RequestParam("applicationid") 浏览器传参
@RequestBody Map<String,String> map body传参

存储过程循环 where  是 相当于if 条件 查询相当于执行

cpu查询结束后 where 条件最小值变大 查询结果相应变大

数据库 string（0.12%） 转换成 float 计算 
String affectrate=  reportMapper.affectbrandrate();
	      String affectcoverage= affectrate.substring(0, affectrate.indexOf("%"));
	      int affectratenums=(int) (Constant.AFFECTUSERSNUM*(Float.valueOf(affectcoverage).floatValue()))/1000000;