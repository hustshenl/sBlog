# 数据字典


### 数据表

+ 文章表`post`
+ 文章元数据表`post_meta`
+ 分类表`taxonomy`
+ 文章分类关系表`post_taxonomy`
+ Git提交记录`commition`

### 文章表

| 字段    | 名称        |  类型 |
|--- |--- |---
| id        | ID             | int(11) 
| status
| name | 文件名称 | varchar(255)
| title     | 文件标题 | varchar(255)
| author
| password
| comment_status
| parent          | 父id
| type
| mime_type
| categories
| tags
| created_at
| updated_at



### 文章元数据表


| 字段        | 名称        |  类型 |
|--- |--- |---
| id                  | ID                 | int(11) 
| post_id        | Post ID        | int(11)
| meta_key    | Meta Key    | varchar(255)
| meta_value | Meta Value | varchar(20480)

### 分类信息表

| 字段        | 名称        |  类型 |
|--- |--- |---
| id                  | ID                 | int(11) 
| status           | 状态             | int(11) 
| name           | 分类名称     | varchar(255)
| type             | 分类类型      | ini(11)
| slug              |  简写            | varchar(255)
| keywords
| description
| parent          | 父id
| level
| sort
| count

### 文章分类关系表


| 字段        | 名称        |  类型 |
|--- |--- |---
| post_id | Post ID | 
| taxonomy_id | Taxonomy ID 
| taxonomy_sort 

### Git提交记录

| 字段        | 名称        |  类型 |
|--- |--- |---
| commit | Commit id | varchar(255)
| apply_at | 提交时间 | int(10)

