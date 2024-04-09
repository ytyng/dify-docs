# 问题分类

问题分类器定义用户问题的分类条件，LLM 能够根据分类描述定义对话的进展方式。如图所示，在一个典型的客服机器人场景中，问题分类器可以作为知识库检索的前置步骤，对用户意图进行识别，分类处理后能够有效提高知识库的召回效果。

<figure><img src="../../../.gitbook/assets/output (6).png" alt=""><figcaption></figcaption></figure>

配置问题分类器节点主要包含三个部分：

1. 选择输入变量
2. 配置推理模型
3. 编写分类方法

#### **选择输入变量**

在对话类客户情景中，你可以将「开始节点」中的用户输入变量（sys.query）作为问题分类器的输入变量，在自动化/批处理场景中，你可以将客户评价或者邮件内容作为输入变量。

#### **配置推理模型**

问题分类器依靠 LLM 的自然语言处理能力对文本进行分类，你需要为分类器配置一个推理模型。在配置推理模型之前，你可能需要在「系统设置-模型供应商」内完成模型配置。具体配置方式可以参考[模型配置说明](https://docs.dify.ai/v/zh-hans/guides/model-configuration)。选择好模型后可以对模型参数进行配置。

#### **编写分类条件**

你可以手动添加多个分类，通过编写符合该分类的关键词或者描述语句，根据分类条件描述，问题分类器能够根据用户输入的语义来选择适合的流程路径。