---
title: ShowMessageAction 物件
description: 針對腳本，表示在工作啟動時顯示訊息方塊的動作。
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- ShowMessageAction 物件工作排程器
- ShowMessageAction 物件工作排程器，說明
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384230"
---
# <a name="showmessageaction-object"></a><span data-ttu-id="83676-105">ShowMessageAction 物件</span><span class="sxs-lookup"><span data-stu-id="83676-105">ShowMessageAction object</span></span>

<span data-ttu-id="83676-106">\[不再支援此物件。</span><span class="sxs-lookup"><span data-stu-id="83676-106">\[This object is no longer supported.</span></span> <span data-ttu-id="83676-107">您可以使用 IExecAction 搭配 Windows 腳本 [**MsgBox 函數**](/previous-versions/sfw6660x(v=vs.80)) ，在使用者會話中顯示訊息。\]</span><span class="sxs-lookup"><span data-stu-id="83676-107">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="83676-108">針對腳本，表示在工作啟動時顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="83676-108">For scripting, represents an action that shows a message box when a task is activated.</span></span>

## <a name="members"></a><span data-ttu-id="83676-109">成員</span><span class="sxs-lookup"><span data-stu-id="83676-109">Members</span></span>

<span data-ttu-id="83676-110">**ShowMessageAction** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="83676-110">The **ShowMessageAction** object has these types of members:</span></span>

-   [<span data-ttu-id="83676-111">屬性</span><span class="sxs-lookup"><span data-stu-id="83676-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83676-112">屬性</span><span class="sxs-lookup"><span data-stu-id="83676-112">Properties</span></span>

<span data-ttu-id="83676-113">**ShowMessageAction** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="83676-113">The **ShowMessageAction** object has these properties.</span></span>



| <span data-ttu-id="83676-114">屬性</span><span class="sxs-lookup"><span data-stu-id="83676-114">Property</span></span>                                                        | <span data-ttu-id="83676-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="83676-115">Access type</span></span>           | <span data-ttu-id="83676-116">Description</span><span class="sxs-lookup"><span data-stu-id="83676-116">Description</span></span>                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83676-117">**Id**</span><span class="sxs-lookup"><span data-stu-id="83676-117">**Id**</span></span>](action-id.md)<br/>                              | <span data-ttu-id="83676-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="83676-118">Read/write</span></span><br/> | <span data-ttu-id="83676-119">繼承自 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="83676-119">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="83676-120">取得或設定動作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="83676-120">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="83676-121">**MessageBody**</span><span class="sxs-lookup"><span data-stu-id="83676-121">**MessageBody**</span></span>](showmessageaction-messagebody.md)<br/> | <span data-ttu-id="83676-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="83676-122">Read/write</span></span><br/> | <span data-ttu-id="83676-123">取得或設定訊息方塊中顯示的郵件內文。</span><span class="sxs-lookup"><span data-stu-id="83676-123">Gets or sets the message text that is displayed in the body of the message box.</span></span><br/>                |
| [<span data-ttu-id="83676-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="83676-124">**Title**</span></span>](showmessageaction-title.md)<br/>             | <span data-ttu-id="83676-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="83676-125">Read/write</span></span><br/> | <span data-ttu-id="83676-126">取得或設定訊息方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="83676-126">Gets or sets the title of the message box.</span></span><br/>                                                     |
| [<span data-ttu-id="83676-127">**類型**</span><span class="sxs-lookup"><span data-stu-id="83676-127">**Type**</span></span>](action-type.md)<br/>                          | <span data-ttu-id="83676-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="83676-128">Read-only</span></span><br/>  | <span data-ttu-id="83676-129">繼承自 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="83676-129">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="83676-130">取得動作的類型。</span><span class="sxs-lookup"><span data-stu-id="83676-130">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="83676-131">備註</span><span class="sxs-lookup"><span data-stu-id="83676-131">Remarks</span></span>

<span data-ttu-id="83676-132">對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="83676-132">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="83676-133">若要將工作登入類型設定為 interactive，請在工作主體的 [**LogonType**](principal-logontype.md)屬性中，或在 [**TaskFolder. RegisterTask**](taskfolder-registertask.md)或 [**TaskFolder**](taskfolder-registertaskdefinition.md)的 *LogonType* 參數中指定 3 (工作登入 **\_ \_ 互動式 \_ 權杖**) 或 4 (工作 **登入 \_ \_ 群組**) 。</span><span class="sxs-lookup"><span data-stu-id="83676-133">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="83676-134">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) 元素來指定訊息方塊動作。</span><span class="sxs-lookup"><span data-stu-id="83676-134">When reading or writing your own XML for a task, a message box action is specified using the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="83676-135">範例</span><span class="sxs-lookup"><span data-stu-id="83676-135">Examples</span></span>

<span data-ttu-id="83676-136">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [ (腳本) 的訊息方塊範例 ](/previous-versions//aa381916(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="83676-136">For more information and example code for this scripting object, see [Message Box Example (Scripting)](/previous-versions//aa381916(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="83676-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="83676-137">Requirements</span></span>



| <span data-ttu-id="83676-138">需求</span><span class="sxs-lookup"><span data-stu-id="83676-138">Requirement</span></span> | <span data-ttu-id="83676-139">值</span><span class="sxs-lookup"><span data-stu-id="83676-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83676-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83676-140">Minimum supported client</span></span><br/> | <span data-ttu-id="83676-141">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83676-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="83676-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83676-142">Minimum supported server</span></span><br/> | <span data-ttu-id="83676-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83676-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="83676-144">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="83676-144">End of client support</span></span><br/>    | <span data-ttu-id="83676-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83676-145">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="83676-146">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="83676-146">End of server support</span></span><br/>    | <span data-ttu-id="83676-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83676-147">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="83676-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="83676-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="83676-149"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="83676-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="83676-150">DLL</span><span class="sxs-lookup"><span data-stu-id="83676-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83676-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83676-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

