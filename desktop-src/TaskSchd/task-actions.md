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
# <a name="task-actions"></a><span data-ttu-id="1248b-111">工作動作</span><span class="sxs-lookup"><span data-stu-id="1248b-111">Task Actions</span></span>

<span data-ttu-id="1248b-112">工作所執行的工作專案稱為「動作」。</span><span class="sxs-lookup"><span data-stu-id="1248b-112">The work items performed by a task are called actions.</span></span> <span data-ttu-id="1248b-113">一個工作可以有單一動作，或是最多 32 個動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-113">A task can have a single action or a maximum of 32 actions.</span></span> <span data-ttu-id="1248b-114">請注意，當指定多個動作時，它們會依序執行。</span><span class="sxs-lookup"><span data-stu-id="1248b-114">Be aware that when multiple actions are specified, they are executed sequentially.</span></span>

## <a name="types-of-actions"></a><span data-ttu-id="1248b-115">動作的類型</span><span class="sxs-lookup"><span data-stu-id="1248b-115">Types of Actions</span></span>

<span data-ttu-id="1248b-116">下表說明可由工作完成的工作或動作類型。</span><span class="sxs-lookup"><span data-stu-id="1248b-116">The following table of actions describes the type of work or actions that can be accomplished by a task.</span></span>

| <span data-ttu-id="1248b-117">動作類型</span><span class="sxs-lookup"><span data-stu-id="1248b-117">Type of Action</span></span>      | <span data-ttu-id="1248b-118">Description</span><span class="sxs-lookup"><span data-stu-id="1248b-118">Description</span></span>                                                             |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="1248b-119">ComHandler 動作</span><span class="sxs-lookup"><span data-stu-id="1248b-119">ComHandler Action</span></span>   | <span data-ttu-id="1248b-120">此動作會引發 COM 處理常式。</span><span class="sxs-lookup"><span data-stu-id="1248b-120">This action fires a COM handler.</span></span>                                        |
| <span data-ttu-id="1248b-121">Exec 動作</span><span class="sxs-lookup"><span data-stu-id="1248b-121">Exec Action</span></span>         | <span data-ttu-id="1248b-122">此動作會執行命令列操作，例如啟動 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="1248b-122">This action executes a command-line operation such as starting Notepad.</span></span> |
| <span data-ttu-id="1248b-123">電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="1248b-123">E-mail Action</span></span>       | <span data-ttu-id="1248b-124">當觸發工作時，此動作會傳送電子郵件。</span><span class="sxs-lookup"><span data-stu-id="1248b-124">This action sends an email when a task is triggered.</span></span>                    |
| <span data-ttu-id="1248b-125">顯示訊息動作</span><span class="sxs-lookup"><span data-stu-id="1248b-125">Show Message Action</span></span> | <span data-ttu-id="1248b-126">這個動作會顯示含有指定訊息和標題的訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="1248b-126">This action shows a message box with a specified message and title.</span></span>     |



 

## <a name="specifying-actions"></a><span data-ttu-id="1248b-127">指定動作</span><span class="sxs-lookup"><span data-stu-id="1248b-127">Specifying Actions</span></span>

<span data-ttu-id="1248b-128">當工作已定義並儲存在工作排程器服務所使用的動作集合中時，就會指定工作的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-128">The actions of a task are specified when the task is defined and stored in a collection of actions used by the Task Scheduler service.</span></span> <span data-ttu-id="1248b-129">下表列出與動作相關聯之 Api 和 XML 元素的參考主題連結。</span><span class="sxs-lookup"><span data-stu-id="1248b-129">The following table lists links to reference topics for the APIs and XML elements that are associated with actions.</span></span>

<span data-ttu-id="1248b-130">如需有關如何使用工作排程器介面、腳本物件和 XML 的詳細資訊和範例，請參閱 [使用工作排程器](using-the-task-scheduler.md)。</span><span class="sxs-lookup"><span data-stu-id="1248b-130">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="interface-apis-for-c-development"></a><span data-ttu-id="1248b-131">適用于 c + + 開發的介面 Api</span><span class="sxs-lookup"><span data-stu-id="1248b-131">Interface APIs for C++ Development</span></span>



| <span data-ttu-id="1248b-132">API</span><span class="sxs-lookup"><span data-stu-id="1248b-132">API</span></span>                                                                    | <span data-ttu-id="1248b-133">描述</span><span class="sxs-lookup"><span data-stu-id="1248b-133">Description</span></span>                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1248b-134">**ITaskDefinition 的 Actions 屬性**</span><span class="sxs-lookup"><span data-stu-id="1248b-134">**Actions Property of ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | <span data-ttu-id="1248b-135">取得或設定工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-135">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="1248b-136">**IActionCollection**</span><span class="sxs-lookup"><span data-stu-id="1248b-136">**IActionCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | <span data-ttu-id="1248b-137">包含工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-137">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="1248b-138">**IComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="1248b-138">**IComHandlerAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | <span data-ttu-id="1248b-139">表示引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-139">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="1248b-140">**IExecAction**</span><span class="sxs-lookup"><span data-stu-id="1248b-140">**IExecAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | <span data-ttu-id="1248b-141">表示執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-141">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="1248b-142">**IEmailAction**</span><span class="sxs-lookup"><span data-stu-id="1248b-142">**IEmailAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | <span data-ttu-id="1248b-143">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-143">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="1248b-144">**IShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="1248b-144">**IShowMessageAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | <span data-ttu-id="1248b-145">表示顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-145">Represents an action that shows a message box.</span></span>               |



 

### <a name="scripting-object-apis-for-scripting-development"></a><span data-ttu-id="1248b-146">編寫腳本開發的腳本物件 Api</span><span class="sxs-lookup"><span data-stu-id="1248b-146">Scripting Object APIs for Scripting Development</span></span>



| <span data-ttu-id="1248b-147">API</span><span class="sxs-lookup"><span data-stu-id="1248b-147">API</span></span>                                                      | <span data-ttu-id="1248b-148">描述</span><span class="sxs-lookup"><span data-stu-id="1248b-148">Description</span></span>                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1248b-149">**TaskDefinition 動作**</span><span class="sxs-lookup"><span data-stu-id="1248b-149">**TaskDefinition.Actions**</span></span>](taskdefinition-actions.md) | <span data-ttu-id="1248b-150">取得或設定工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-150">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="1248b-151">**Actioncollection 動作**</span><span class="sxs-lookup"><span data-stu-id="1248b-151">**ActionCollection**</span></span>](actioncollection.md)             | <span data-ttu-id="1248b-152">包含工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-152">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="1248b-153">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="1248b-153">**ComHandlerAction**</span></span>](comhandleraction.md)             | <span data-ttu-id="1248b-154">表示引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-154">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="1248b-155">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="1248b-155">**ExecAction**</span></span>](execaction.md)                         | <span data-ttu-id="1248b-156">表示執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-156">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="1248b-157">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="1248b-157">**EmailAction**</span></span>](emailaction.md)                       | <span data-ttu-id="1248b-158">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-158">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="1248b-159">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="1248b-159">**ShowMessageAction**</span></span>](showmessageaction.md)           | <span data-ttu-id="1248b-160">表示顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-160">Represents an action that shows a message box.</span></span>               |



 

### <a name="xml-elements"></a><span data-ttu-id="1248b-161">XML 元素</span><span class="sxs-lookup"><span data-stu-id="1248b-161">XML Elements</span></span>



| <span data-ttu-id="1248b-162">元素</span><span class="sxs-lookup"><span data-stu-id="1248b-162">Element</span></span>                                                                    | <span data-ttu-id="1248b-163">描述</span><span class="sxs-lookup"><span data-stu-id="1248b-163">Description</span></span>                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1248b-164">**行動**</span><span class="sxs-lookup"><span data-stu-id="1248b-164">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)            | <span data-ttu-id="1248b-165">定義工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-165">Defines the actions performed by the task.</span></span>                   |
| [<span data-ttu-id="1248b-166">**ComHandler**</span><span class="sxs-lookup"><span data-stu-id="1248b-166">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | <span data-ttu-id="1248b-167">表示引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-167">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="1248b-168">**Exec**</span><span class="sxs-lookup"><span data-stu-id="1248b-168">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | <span data-ttu-id="1248b-169">表示執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-169">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="1248b-170">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="1248b-170">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | <span data-ttu-id="1248b-171">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-171">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="1248b-172">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="1248b-172">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | <span data-ttu-id="1248b-173">表示顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="1248b-173">Represents an action that shows a message box.</span></span>               |



 

## <a name="using-variables-in-action-properties"></a><span data-ttu-id="1248b-174">在動作屬性中使用變數</span><span class="sxs-lookup"><span data-stu-id="1248b-174">Using Variables in Action Properties</span></span>

<span data-ttu-id="1248b-175">**BSTR** 類型的某些動作屬性可包含 $ (Arg0) ，$ (Arg1) ，...，$ (Arg32 在其字串值中) 變數。</span><span class="sxs-lookup"><span data-stu-id="1248b-175">Some action properties that are of type **BSTR** can contain $(Arg0), $(Arg1), ..., $(Arg32) variables in their string values.</span></span> <span data-ttu-id="1248b-176">這些變數會取代為 [**IRegisteredTask：： Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run)和 [**IRegisteredTask：： RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex)方法的 *params* 參數中所指定的值，或包含在工作的事件觸發程式中。</span><span class="sxs-lookup"><span data-stu-id="1248b-176">These variables are replaced with the values that are specified in the *params* parameter of the [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) and [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) methods or are contained within the event trigger for the task.</span></span> <span data-ttu-id="1248b-177">下表列出可在其字串值中使用變數的動作屬性。</span><span class="sxs-lookup"><span data-stu-id="1248b-177">The following table lists the action properties that can use variables in their string values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1248b-178">動作</span><span class="sxs-lookup"><span data-stu-id="1248b-178">Action</span></span></th>
<th><span data-ttu-id="1248b-179">屬性</span><span class="sxs-lookup"><span data-stu-id="1248b-179">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1248b-180">COM 處理常式動作</span><span class="sxs-lookup"><span data-stu-id="1248b-180">COM Handler Action</span></span></td>
<td><span data-ttu-id="1248b-181">C++：</span><span class="sxs-lookup"><span data-stu-id="1248b-181">C++:</span></span>
<ul>
<li><span data-ttu-id="1248b-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>IComHandlerAction 的 ClassId 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassId Property of IComHandlerAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>IComHandlerAction 的資料屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Data Property of IComHandlerAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1248b-184">指令碼：</span><span class="sxs-lookup"><span data-stu-id="1248b-184">Scripting:</span></span>
<ul>
<li><span data-ttu-id="1248b-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></span></span></li>
<li><span data-ttu-id="1248b-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction 資料</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1248b-187">電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="1248b-187">Email Action</span></span></td>
<td><span data-ttu-id="1248b-188">C++：</span><span class="sxs-lookup"><span data-stu-id="1248b-188">C++:</span></span>
<ul>
<li><span data-ttu-id="1248b-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>IEmailAction 的 Body 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>IEmailAction 的伺服器屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>IEmailAction 的 Subject 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>IEmailAction 的屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>IEmailAction 的 Cc 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Cc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>IEmailAction 的密件副本屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Bcc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>IEmailAction 的 ReplyTo 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From IEmailAction 的屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From Property of IEmailAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1248b-197">指令碼：</span><span class="sxs-lookup"><span data-stu-id="1248b-197">Scripting:</span></span>
<ul>
<li><span data-ttu-id="1248b-198"><a href="emailaction-body.md"><strong>EmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-198"><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></span></span></li>
<li><span data-ttu-id="1248b-199"><a href="emailaction-server.md"><strong>EmailAction 伺服器</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-199"><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></span></span></li>
<li><span data-ttu-id="1248b-200"><a href="emailaction-subject.md"><strong>EmailAction 主題</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-200"><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></span></span></li>
<li><span data-ttu-id="1248b-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span></span></li>
<li><span data-ttu-id="1248b-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span></span></li>
<li><span data-ttu-id="1248b-203"><a href="emailaction-bcc.md"><strong>EmailAction 密件副本</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-203"><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></span></span></li>
<li><span data-ttu-id="1248b-204"><a href="emailaction-replyto.md"><strong>EmailAction ReplyTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-204"><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></span></span></li>
<li><span data-ttu-id="1248b-205"><a href="emailaction-from.md"><strong>EmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-205"><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1248b-206">Exec 動作</span><span class="sxs-lookup"><span data-stu-id="1248b-206">Exec Action</span></span></td>
<td><span data-ttu-id="1248b-207">C++：</span><span class="sxs-lookup"><span data-stu-id="1248b-207">C++:</span></span>
<ul>
<li><span data-ttu-id="1248b-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>IExecAction 的 Arguments 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments Property of IExecAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>IExecAction 的 WorkingDirectory 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory Property of IExecAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1248b-210">指令碼：</span><span class="sxs-lookup"><span data-stu-id="1248b-210">Scripting:</span></span>
<ul>
<li><span data-ttu-id="1248b-211"><a href="execaction-arguments.md"><strong>ExecAction. 引數</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-211"><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></span></span></li>
<li><span data-ttu-id="1248b-212"><a href="execaction-workingdirectory.md"><strong>ExecAction. WorkingDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-212"><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1248b-213">顯示訊息動作</span><span class="sxs-lookup"><span data-stu-id="1248b-213">Show Message Action</span></span></td>
<td><span data-ttu-id="1248b-214">C++：</span><span class="sxs-lookup"><span data-stu-id="1248b-214">C++:</span></span>
<ul>
<li><span data-ttu-id="1248b-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>IShowMessageAction 的 Title 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title Property of IShowMessageAction</strong></a></span></span></li>
<li><span data-ttu-id="1248b-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>IShowMessageAction 的 MessageBody 屬性</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody Property of IShowMessageAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1248b-217">指令碼：</span><span class="sxs-lookup"><span data-stu-id="1248b-217">Scripting:</span></span>
<ul>
<li><span data-ttu-id="1248b-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction 標題</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></span></span></li>
<li><span data-ttu-id="1248b-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction. MessageBody</strong></a></span><span class="sxs-lookup"><span data-stu-id="1248b-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1248b-220">相關主題</span><span class="sxs-lookup"><span data-stu-id="1248b-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1248b-221">關於工作排程器</span><span class="sxs-lookup"><span data-stu-id="1248b-221">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 





