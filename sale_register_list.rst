7.1.1 委托登记列表管理

    1. *描述*
        获取自己创建的所有委托登记

    2. *接口名称*
        sale_register_list

    3. *请求参数说明*  
      
    \
         .. csv-table:: 
           :header: "字段", "必填", "类型","默认值","说明"
           :widths: 30, 30, 30,30,30

           "keyword", "否", "String","False","筛选关键字"
           "domain", "否", "String","False","筛选关键字"
    
    5. *返回参数说明*

    \
        .. csv-table:: 
           :header: "字段", "必填", "类型","默认值","说明"
           :widths: 20, 20, 20,20,90

           "id", "否", "int","False","单据ID"
           "acreage", "否", "float","0.0","面积从"
           "acreage_to", "否", "float","0.0","面积从"
           "create_date", "否", "date","1900-01-01","日期[格式：yyyy-mm-dd] "
           "contact_name", "否", "string","False","联系人姓名"
           "community_name", "否", "string","False","小区名称"
           "apartment_type_name", "否", "string","False","房型名称"
           "state", "否", "string","draft","状态,固定列表
           
           1. draft：作废
           
           2. revising：修订中
           
           3. dispatching：派工中
           
           4. executing：跟进中
           
           5. done：已关闭
           
           6. cancelled：已取消"

    6. *调用示例*
    
     ::

       $('#sale_register_list').on('click',function(){
           var params = {};
           g_query( 'sale_register_list',params,
               function(response, status, jqXHR){
                   if(response.length>0){
                       console.log('销售-登记-列表：',response[0][0]);
                   }
               },function(jqXHR, status, error){
                     console.log('销售-登记-列表：失败！');
                 }
              );
           });

  5. *返回结果*

   ::

     [
       {'create_date': '2016-05-26 04:57:20', 'acreage_to': 0.0, 'acreage': 0.0, 'community_name': False, 'state': 'draft', 'contact_name': False, 'id': 204, 'apartment_type_name': False},
       {'create_date': '2016-05-29 06:45:40', 'acreage_to': 0.0, 'acreage': 0.0, 'community_name': False, 'state': 'draft', 'contact_name': u'\u5510\u8001\u9e2d\u5148\u751f2', 'id': 228, 'apartment_type_name': False},
       {'create_date': '2016-06-15 10:34:17', 'acreage_to': 0.0, 'acreage': 0.0, 'community_name': False, 'state': 'draft', 'contact_name': False, 'id': 288, 'apartment_type_name': False},
       {'create_date': '2016-06-27 16:45:06', 'acreage_to': 120.0, 'acreage': 100.0, 'community_name': False, 'state': 'draft', 'contact_name': u'\u5f20\u6653\u535a', 'id': 314, 'apartment_type_name': u'\u4e09\u5ba4\u4e24\u5385'},
       {'create_date': '2016-06-27 16:53:35', 'acreage_to': 150.0, 'acreage': 100.0, 'community_name': False, 'state': 'draft', 'contact_name': u'\u5f20\u6653\u535a', 'id': 316, 'apartment_type_name': u'23\u5ba4'},
       {'create_date': '2016-06-30 02:01:18', 'acreage_to': 0.0, 'acreage': 0.0, 'community_name': False, 'state': 'draft', 'contact_name': False, 'id': 324, 'apartment_type_name': False},
       {'create_date': '2016-06-30 02:39:17', 'acreage_to': 0.0, 'acreage': 0.0, 'community_name': False, 'state': 'draft', 'contact_name': False, 'id': 325, 'apartment_type_name': False},
       {'create_date': '2016-06-30 06:48:26', 'acreage_to': 0.0, 'acreage': 0.0, 'community_name': False, 'state': 'draft', 'contact_name': False, 'id': 345, 'apartment_type_name': False},
       {'create_date': '2016-06-30 08:11:21', 'acreage_to': 0.0, 'acreage': 0.0, 'community_name': False, 'state': 'draft', 'contact_name': u'\u5f20\u4e09\u674e', 'id': 350, 'apartment_type_name': False}

     ]
