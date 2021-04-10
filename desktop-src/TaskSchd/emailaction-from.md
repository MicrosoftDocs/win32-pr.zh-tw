---
title: EmailAction 屬性
description: 針對腳本，取得或設定要傳送電子郵件的電子郵件地址。
ms.assetid: befe6900-6fbe-4ba2-aeda-271b770e971a
keywords:
- 從屬性工作排程器
- From 屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器，從屬性
topic_type:
- apiref
api_name:
- EmailAction.From
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d91b132e8d56caba1a21768e4aacfdda855fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104117"
---
# <a name="emailactionfrom-property"></a><span data-ttu-id="99086-106">EmailAction 屬性</span><span class="sxs-lookup"><span data-stu-id="99086-106">EmailAction.From property</span></span>

<span data-ttu-id="99086-107">\[不再支援此物件。</span><span class="sxs-lookup"><span data-stu-id="99086-107">\[This object is no longer supported.</span></span> <span data-ttu-id="99086-108">請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]</span><span class="sxs-lookup"><span data-stu-id="99086-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="99086-109">針對腳本，取得或設定要傳送電子郵件的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="99086-109">For scripting, gets or sets the email address that you want to send the email from.</span></span>

<span data-ttu-id="99086-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="99086-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="99086-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="99086-111">Syntax</span></span>


```VB
EmailAction.From As String
```



## <a name="property-value"></a><span data-ttu-id="99086-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="99086-112">Property value</span></span>

<span data-ttu-id="99086-113">您要傳送電子郵件的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="99086-113">The email address that you want to send the email from.</span></span>

## <a name="requirements"></a><span data-ttu-id="99086-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="99086-114">Requirements</span></span>



| <span data-ttu-id="99086-115">需求</span><span class="sxs-lookup"><span data-stu-id="99086-115">Requirement</span></span> | <span data-ttu-id="99086-116">值</span><span class="sxs-lookup"><span data-stu-id="99086-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99086-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99086-117">Minimum supported client</span></span><br/> | <span data-ttu-id="99086-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99086-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="99086-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99086-119">Minimum supported server</span></span><br/> | <span data-ttu-id="99086-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99086-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99086-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="99086-121">End of client support</span></span><br/>    | <span data-ttu-id="99086-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="99086-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="99086-123">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="99086-123">End of server support</span></span><br/>    | <span data-ttu-id="99086-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99086-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="99086-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="99086-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="99086-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99086-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99086-127">DLL</span><span class="sxs-lookup"><span data-stu-id="99086-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99086-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99086-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99086-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99086-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99086-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="99086-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="99086-131">工作排程器</span><span class="sxs-lookup"><span data-stu-id="99086-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

