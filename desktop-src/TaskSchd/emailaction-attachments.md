---
title: EmailAction 附件屬性
description: 針對腳本，取得或設定與電子郵件訊息一起傳送的附件陣列。
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- 附件屬性工作排程器
- 附件屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器，附件屬性
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686008"
---
# <a name="emailactionattachments-property"></a><span data-ttu-id="d4c76-106">EmailAction 附件屬性</span><span class="sxs-lookup"><span data-stu-id="d4c76-106">EmailAction.Attachments property</span></span>

<span data-ttu-id="d4c76-107">\[不再支援此物件。</span><span class="sxs-lookup"><span data-stu-id="d4c76-107">\[This object is no longer supported.</span></span> <span data-ttu-id="d4c76-108">請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]</span><span class="sxs-lookup"><span data-stu-id="d4c76-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="d4c76-109">針對腳本，取得或設定與電子郵件訊息一起傳送的附件陣列。</span><span class="sxs-lookup"><span data-stu-id="d4c76-109">For scripting, gets or sets an array of attachments that is sent with the email message.</span></span>

<span data-ttu-id="d4c76-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d4c76-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c76-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4c76-111">Syntax</span></span>


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a><span data-ttu-id="d4c76-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="d4c76-112">Property value</span></span>

<span data-ttu-id="d4c76-113">與電子郵件訊息一起傳送的附件陣列。</span><span class="sxs-lookup"><span data-stu-id="d4c76-113">An array of attachments that is sent with the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c76-114">備註</span><span class="sxs-lookup"><span data-stu-id="d4c76-114">Remarks</span></span>

<span data-ttu-id="d4c76-115">附件陣列中最多可以有八個附件。</span><span class="sxs-lookup"><span data-stu-id="d4c76-115">A maximum of eight attachments can be in the array of attachments.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c76-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4c76-116">Requirements</span></span>



| <span data-ttu-id="d4c76-117">需求</span><span class="sxs-lookup"><span data-stu-id="d4c76-117">Requirement</span></span> | <span data-ttu-id="d4c76-118">值</span><span class="sxs-lookup"><span data-stu-id="d4c76-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c76-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4c76-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c76-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4c76-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d4c76-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4c76-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c76-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4c76-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4c76-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d4c76-123">End of client support</span></span><br/>    | <span data-ttu-id="d4c76-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d4c76-124">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="d4c76-125">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d4c76-125">End of server support</span></span><br/>    | <span data-ttu-id="d4c76-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4c76-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d4c76-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d4c76-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4c76-128"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4c76-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4c76-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d4c76-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4c76-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4c76-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c76-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4c76-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c76-132">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="d4c76-132">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="d4c76-133">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d4c76-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

