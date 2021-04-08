---
title: 工作動作
description: 工作所執行的工作專案稱為「動作」。 一個工作可以有單一動作，或是最多 32 個動作。 請注意，當指定多個動作時，它們會依序執行。
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- 動作工作排程器
- 動作工作排程器，說明
- 動作工作排程器，執行動作
- 動作工作排程器，COM 處理常式動作
- 執行動作工作排程器
- COM 處理常式動作工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "103680907"
---
# <a name="task-actions"></a>工作動作

工作所執行的工作專案稱為「動作」。 一個工作可以有單一動作，或是最多 32 個動作。 請注意，當指定多個動作時，它們會依序執行。

## <a name="types-of-actions"></a>動作的類型

下表說明可由工作完成的工作或動作類型。

| 動作類型      | Description                                                             |
|---------------------|-------------------------------------------------------------------------|
| ComHandler 動作   | 此動作會引發 COM 處理常式。                                        |
| Exec 動作         | 此動作會執行命令列操作，例如啟動 [記事本]。 |
| 電子郵件動作       | 當觸發工作時，此動作會傳送電子郵件。                    |
| 顯示訊息動作 | 這個動作會顯示含有指定訊息和標題的訊息方塊。     |



 

## <a name="specifying-actions"></a>指定動作

當工作已定義並儲存在工作排程器服務所使用的動作集合中時，就會指定工作的動作。 下表列出與動作相關聯之 Api 和 XML 元素的參考主題連結。

如需有關如何使用工作排程器介面、腳本物件和 XML 的詳細資訊和範例，請參閱 [使用工作排程器](using-the-task-scheduler.md)。

### <a name="interface-apis-for-c-development"></a>適用于 c + + 開發的介面 Api



| API                                                                    | 描述                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**ITaskDefinition 的 Actions 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | 取得或設定工作所執行的動作。              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | 包含工作所執行的動作。                  |
| [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | 表示引發處理常式的動作。                   |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | 表示執行命令列操作的動作。 |
| [**IEmailAction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | 表示傳送電子郵件訊息的動作。            |
| [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | 表示顯示訊息方塊的動作。               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>編寫腳本開發的腳本物件 Api



| API                                                      | 描述                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**TaskDefinition 動作**](taskdefinition-actions.md) | 取得或設定工作所執行的動作。              |
| [**Actioncollection 動作**](actioncollection.md)             | 包含工作所執行的動作。                  |
| [**ComHandlerAction**](comhandleraction.md)             | 表示引發處理常式的動作。                   |
| [**ExecAction**](execaction.md)                         | 表示執行命令列操作的動作。 |
| [**EmailAction**](emailaction.md)                       | 表示傳送電子郵件訊息的動作。            |
| [**ShowMessageAction**](showmessageaction.md)           | 表示顯示訊息方塊的動作。               |



 

### <a name="xml-elements"></a>XML 元素



| 元素                                                                    | 描述                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**行動**](taskschedulerschema-actions-tasktype-element.md)            | 定義工作所執行的動作。                   |
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | 表示引發處理常式的動作。                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | 表示執行命令列操作的動作。 |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | 表示傳送電子郵件訊息的動作。            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | 表示顯示訊息方塊的動作。               |



 

## <a name="using-variables-in-action-properties"></a>在動作屬性中使用變數

**BSTR** 類型的某些動作屬性可包含 $ (Arg0) ，$ (Arg1) ，...，$ (Arg32 在其字串值中) 變數。 這些變數會取代為 [**IRegisteredTask：： Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run)和 [**IRegisteredTask：： RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex)方法的 *params* 參數中所指定的值，或包含在工作的事件觸發程式中。 下表列出可在其字串值中使用變數的動作屬性。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>動作</th>
<th>屬性</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COM 處理常式動作</td>
<td>C++：
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>IComHandlerAction 的 ClassId 屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>IComHandlerAction 的資料屬性</strong></a></li>
</ul>
<br/> 指令碼：
<ul>
<li><a href="comhandleraction-classid.md"><strong>ComHandlerAction</strong></a></li>
<li><a href="comhandleraction-data.md"><strong>ComHandlerAction 資料</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>電子郵件動作</td>
<td>C++：
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>IEmailAction 的 Body 屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>IEmailAction 的伺服器屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>IEmailAction 的 Subject 屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>IEmailAction 的屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>IEmailAction 的 Cc 屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>IEmailAction 的密件副本屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>IEmailAction 的 ReplyTo 屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From IEmailAction 的屬性</strong></a></li>
</ul>
<br/> 指令碼：
<ul>
<li><a href="emailaction-body.md"><strong>EmailAction</strong></a></li>
<li><a href="emailaction-server.md"><strong>EmailAction 伺服器</strong></a></li>
<li><a href="emailaction-subject.md"><strong>EmailAction 主題</strong></a></li>
<li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li>
<li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li>
<li><a href="emailaction-bcc.md"><strong>EmailAction 密件副本</strong></a></li>
<li><a href="emailaction-replyto.md"><strong>EmailAction ReplyTo</strong></a></li>
<li><a href="emailaction-from.md"><strong>EmailAction</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Exec 動作</td>
<td>C++：
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>IExecAction 的 Arguments 屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>IExecAction 的 WorkingDirectory 屬性</strong></a></li>
</ul>
<br/> 指令碼：
<ul>
<li><a href="execaction-arguments.md"><strong>ExecAction. 引數</strong></a></li>
<li><a href="execaction-workingdirectory.md"><strong>ExecAction. WorkingDirectory</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>顯示訊息動作</td>
<td>C++：
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>IShowMessageAction 的 Title 屬性</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>IShowMessageAction 的 MessageBody 屬性</strong></a></li>
</ul>
<br/> 指令碼：
<ul>
<li><a href="showmessageaction-title.md"><strong>ShowMessageAction 標題</strong></a></li>
<li><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction. MessageBody</strong></a></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於工作排程器](about-the-task-scheduler.md)
</dt> </dl>

 

 





