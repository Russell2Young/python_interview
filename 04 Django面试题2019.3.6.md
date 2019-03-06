# Django面试题 2019.3.6



### 以下模型为作者与文章的Django关系模型

```python
# coding=utf-8
from django.db import models

class People(modles.Model):
    """
    作者
    """
    name = models.CharField(max_length=200, help_text=u'姓名')
    age = models.IntegerField(help_text=u'年龄')
    
class Article(modles.Model):
    """
    文章
    """
    people = models.ForeignKey(People, related_name="people_article")
    name = models.CharField(max_length=200, help_text=u'文章名称')
```



1. 使用ORM，写出查询标题包含“abc”的文章

   ```
   
   ```

2. 使用ORM，写出年龄小于30岁的作者

   ```sql
   
   ```

3. 查询由年龄小于30岁的作者所写的文章，请补全以下filter参数：

   ```sql
   query_set = Article.objects.filter(???)
   
   ```

4. 查询所写文章名称包含“abc”的所有作者，请补全以下filter参数：

   ```sql
   query_set = People.objects.filter(???)
   
   ```

   