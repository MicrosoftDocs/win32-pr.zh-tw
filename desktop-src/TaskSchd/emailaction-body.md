---
title: EmailAction。 Body 屬性
description: 針對腳本，取得或設定包含電子郵件訊息的電子郵件內文。
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- 主體屬性工作排程器
- Body 屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器，主體屬性
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967974"
---
# <a name="emailactionbody-property"></a><span data-ttu-id="80fdc-106">EmailAction。 Body 屬性</span><span class="sxs-lookup"><span data-stu-id="80fdc-106">EmailAction.Body property</span></span>

<span data-ttu-id="80fdc-107">\[不再支援此物件。</span><span class="sxs-lookup"><span data-stu-id="80fdc-107">\[This object is no longer supported.</span></span> <span data-ttu-id="80fdc-108">請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]</span><span class="sxs-lookup"><span data-stu-id="80fdc-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="80fdc-109">針對腳本，取得或設定包含電子郵件訊息的電子郵件內文。</span><span class="sxs-lookup"><span data-stu-id="80fdc-109">For scripting, gets or sets the body of the email that contains the email message.</span></span>

<span data-ttu-id="80fdc-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="80fdc-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fdc-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="80fdc-111">Syntax</span></span>


```VB
EmailAction.Body As String
```



## <a name="property-value"></a><span data-ttu-id="80fdc-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="80fdc-112">Property value</span></span>

<span data-ttu-id="80fdc-113">包含電子郵件訊息的電子郵件內文。</span><span class="sxs-lookup"><span data-stu-id="80fdc-113">The body of the email that contains the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="80fdc-114">備註</span><span class="sxs-lookup"><span data-stu-id="80fdc-114">Remarks</span></span>

<span data-ttu-id="80fdc-115">設定這個屬性值時，值可以是從資源 .dll 檔案抓取的文字。</span><span class="sxs-lookup"><span data-stu-id="80fdc-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="80fdc-116">特製化的字串會用來參考資源檔中的文字。</span><span class="sxs-lookup"><span data-stu-id="80fdc-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="80fdc-117">字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ dll \] 是包含資源的 .Dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。</span><span class="sxs-lookup"><span data-stu-id="80fdc-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="80fdc-118">例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="80fdc-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="80fdc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="80fdc-119">Requirements</span></span>



| <span data-ttu-id="80fdc-120">需求</span><span class="sxs-lookup"><span data-stu-id="80fdc-120">Requirement</span></span> | <span data-ttu-id="80fdc-121">值</span><span class="sxs-lookup"><span data-stu-id="80fdc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80fdc-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80fdc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="80fdc-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80fdc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="80fdc-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80fdc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="80fdc-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80fdc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="80fdc-126">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="80fdc-126">End of client support</span></span><br/>    | <span data-ttu-id="80fdc-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="80fdc-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="80fdc-128">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="80fdc-128">End of server support</span></span><br/>    | <span data-ttu-id="80fdc-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80fdc-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="80fdc-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="80fdc-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="80fdc-131"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="80fdc-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="80fdc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="80fdc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80fdc-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80fdc-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80fdc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80fdc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fdc-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="80fdc-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="80fdc-136">工作排程器</span><span class="sxs-lookup"><span data-stu-id="80fdc-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

