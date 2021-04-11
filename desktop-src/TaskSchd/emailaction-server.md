---
title: EmailAction。伺服器屬性
description: 針對腳本，取得或設定用來傳送電子郵件的 SMTP 伺服器名稱。
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- 伺服器屬性工作排程器
- 伺服器屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器，伺服器屬性
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317284"
---
# <a name="emailactionserver-property"></a><span data-ttu-id="6f3ad-106">EmailAction。伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="6f3ad-106">EmailAction.Server property</span></span>

<span data-ttu-id="6f3ad-107">\[不再支援此物件。</span><span class="sxs-lookup"><span data-stu-id="6f3ad-107">\[This object is no longer supported.</span></span> <span data-ttu-id="6f3ad-108">請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]</span><span class="sxs-lookup"><span data-stu-id="6f3ad-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="6f3ad-109">針對腳本，取得或設定用來傳送電子郵件的 SMTP 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6f3ad-109">For scripting, gets or sets the name of the SMTP server that you use to send email from.</span></span>

<span data-ttu-id="6f3ad-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f3ad-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3ad-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f3ad-111">Syntax</span></span>


```VB
EmailAction.Server As String
```



## <a name="property-value"></a><span data-ttu-id="6f3ad-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6f3ad-112">Property value</span></span>

<span data-ttu-id="6f3ad-113">您用來傳送電子郵件的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6f3ad-113">The name of the server that you use to send email from.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f3ad-114">備註</span><span class="sxs-lookup"><span data-stu-id="6f3ad-114">Remarks</span></span>

<span data-ttu-id="6f3ad-115">請確認傳送電子郵件的 SMTP 伺服器已正確設定。</span><span class="sxs-lookup"><span data-stu-id="6f3ad-115">Make sure the SMTP server that sends the email is setup correctly.</span></span> <span data-ttu-id="6f3ad-116">電子郵件是使用適用于 Windows SMTP 伺服器的 NTLM 驗證來傳送，這表示用於執行工作的安全性認證也必須具有 SMTP 伺服器的許可權，才能傳送電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="6f3ad-116">E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message.</span></span> <span data-ttu-id="6f3ad-117">如果 SMTP 伺服器是非 Windows 伺服器，則會在伺服器允許匿名存取時傳送電子郵件。</span><span class="sxs-lookup"><span data-stu-id="6f3ad-117">If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access.</span></span> <span data-ttu-id="6f3ad-118">如需設定 SMTP 伺服器的詳細資訊，請參閱 [Smtp 伺服器設定](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)，如需管理 smtp 伺服器設定的詳細資訊，請參閱 [smtp 管理](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="6f3ad-118">For information about setting up the SMTP server, see [SMTP Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true), and for information about managing SMTP server settings, see [SMTP Administration](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f3ad-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f3ad-119">Requirements</span></span>



| <span data-ttu-id="6f3ad-120">需求</span><span class="sxs-lookup"><span data-stu-id="6f3ad-120">Requirement</span></span> | <span data-ttu-id="6f3ad-121">值</span><span class="sxs-lookup"><span data-stu-id="6f3ad-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3ad-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f3ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3ad-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f3ad-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6f3ad-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f3ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3ad-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f3ad-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f3ad-126">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6f3ad-126">End of client support</span></span><br/>    | <span data-ttu-id="6f3ad-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f3ad-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="6f3ad-128">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6f3ad-128">End of server support</span></span><br/>    | <span data-ttu-id="6f3ad-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f3ad-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6f3ad-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6f3ad-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f3ad-131"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f3ad-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f3ad-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6f3ad-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f3ad-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f3ad-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f3ad-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f3ad-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3ad-135">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="6f3ad-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="6f3ad-136">工作排程器</span><span class="sxs-lookup"><span data-stu-id="6f3ad-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

