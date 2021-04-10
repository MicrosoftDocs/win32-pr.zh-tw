---
title: EmailAction.Cc 屬性
description: 針對腳本，取得或設定要在電子郵件訊息中抄送的電子郵件地址。
ms.assetid: 4ad67064-3e6b-4666-a3ce-66e4dcc3f873
keywords:
- Cc 屬性工作排程器
- Cc 屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器、Cc 屬性
topic_type:
- apiref
api_name:
- EmailAction.Cc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f05d7fbd1883aa38ba972eba1eb14767349357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686007"
---
# <a name="emailactioncc-property"></a><span data-ttu-id="cb165-106">EmailAction.Cc 屬性</span><span class="sxs-lookup"><span data-stu-id="cb165-106">EmailAction.Cc property</span></span>

<span data-ttu-id="cb165-107">\[不再支援此物件。</span><span class="sxs-lookup"><span data-stu-id="cb165-107">\[This object is no longer supported.</span></span> <span data-ttu-id="cb165-108">請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]</span><span class="sxs-lookup"><span data-stu-id="cb165-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="cb165-109">針對腳本，取得或設定要在電子郵件訊息中抄送的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cb165-109">For scripting, gets or sets the email address or addresses that you want to Cc in the email message.</span></span>

<span data-ttu-id="cb165-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb165-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb165-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb165-111">Syntax</span></span>


```VB
EmailAction.Cc As String
```



## <a name="property-value"></a><span data-ttu-id="cb165-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="cb165-112">Property value</span></span>

<span data-ttu-id="cb165-113">您要在電子郵件訊息中抄送的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cb165-113">The email address or addresses that you want to Cc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb165-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb165-114">Requirements</span></span>



| <span data-ttu-id="cb165-115">需求</span><span class="sxs-lookup"><span data-stu-id="cb165-115">Requirement</span></span> | <span data-ttu-id="cb165-116">值</span><span class="sxs-lookup"><span data-stu-id="cb165-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb165-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb165-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cb165-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb165-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cb165-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb165-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cb165-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb165-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb165-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cb165-121">End of client support</span></span><br/>    | <span data-ttu-id="cb165-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb165-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="cb165-123">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="cb165-123">End of server support</span></span><br/>    | <span data-ttu-id="cb165-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cb165-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="cb165-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="cb165-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb165-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cb165-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cb165-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cb165-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb165-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb165-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb165-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb165-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb165-130">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="cb165-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="cb165-131">工作排程器</span><span class="sxs-lookup"><span data-stu-id="cb165-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

