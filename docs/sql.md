# 数据库
## ts_group_homework_statistics
> 教师组作业统计表

字段|注释
--|--
id|主键
book_id|教材id: -1表示人机对话， -2表示笔试考场
grade_id|教材年级id，见 [ts_book_grade](/sql?id=ts_book_grade)
version_id|教材版本id，见 [ts_book_version](/sql?id=ts_book_version)
unit_id|单元id，0表示跨单元
homework_id|作业id，见 [ts_homework](/sql?id=ts_homework)
homework_type|作业类型:1-教师作业，2-组内作业，3-系统作业
term|学年，见ts_term
class_id|班级id，见ts_online_class
user_id|教师用户id
sender_id|发布人用户id
sender_type|发布人类型:1-老师，2-教研组，3-代理商，4-系统作业，5-家长
start_time|作业开始时间
status|作业状态:1-保存；2-已发布，未截止；3-撤销；4-已发布，已截止；5-已发布，未开始；
update_time|更新时间

## ts_homework
> 作业表

字段|注释
--|--
id|主键
sender_type|发布人类型:1-老师，2-教研组，3-代理商，4-系统作业，5-家长
sender_id|发布人用户id
work_type|作业类型:1-班级作业，2-学生作业，3-个性化作业，4-集体作业
practice_type|试题类型:1-普通练习 6-练听力 7-练口语 8-写作文 9-背课文 10-背单词 11-词汇语法 12-短文阅读
version_id|教材版本id，见 [ts_book_version](/sql?id=ts_book_version)
grade_id|教材年级id，见 [ts_book_grade](/sql?id=ts_book_grade)
title|作业标题
status|作业状态:1-保存；2-已发布，未截止；3-撤销；4-已发布，已截止；5-已发布，未开始；
receiver_num|分发人数，针对学生作业、个性化作业等有效，集体性质作业为0
practice_time|预计用时，秒数
end_time|截止时间
start_time|开始时间
create_time|创建时间
score|总分
unit_ids|单元id列表
struct_id|作业结构
struct_type|作业结构类型，1-自由普通作业，2-自由试卷作业,3-考试试卷作业，4-考试普通作业
kind|类型：0 笔试 1 听力 2 口语 3 听力口语 4 笔试听力口语 5 笔试听力 6 笔试口语
config|暂未使用
update_time|更新时间