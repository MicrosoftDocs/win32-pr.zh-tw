---
title: 'TB_SAVERESTORE 訊息 (Commctrl .h) '
description: 傳送此訊息以起始儲存或還原工具列狀態。
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843059"
---
# <a name="tb_saverestore-message"></a><span data-ttu-id="2cc61-104">TB \_ SAVERESTORE 訊息</span><span class="sxs-lookup"><span data-stu-id="2cc61-104">TB\_SAVERESTORE message</span></span>

<span data-ttu-id="2cc61-105">傳送此訊息以起始儲存或還原工具列狀態。</span><span class="sxs-lookup"><span data-stu-id="2cc61-105">Send this message to initiate saving or restoring a toolbar state.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cc61-106">參數</span><span class="sxs-lookup"><span data-stu-id="2cc61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc61-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cc61-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc61-108">儲存或還原旗標。</span><span class="sxs-lookup"><span data-stu-id="2cc61-108">Save or restore flag.</span></span> <span data-ttu-id="2cc61-109">如果此參數為 **TRUE**，則會儲存資訊。</span><span class="sxs-lookup"><span data-stu-id="2cc61-109">If this parameter is **TRUE**, the information is saved.</span></span> <span data-ttu-id="2cc61-110">如果為 **FALSE**，則會還原資訊。</span><span class="sxs-lookup"><span data-stu-id="2cc61-110">If it is **FALSE**, the information is restored.</span></span>

</dd> <dt>

<span data-ttu-id="2cc61-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cc61-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc61-112">[**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa)結構的指標，指定工具列狀態資訊的登錄機碼、子機碼和值名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc61-112">Pointer to a [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) structure that specifies the registry key, subkey, and value name for the toolbar state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc61-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2cc61-113">Return value</span></span>

<span data-ttu-id="2cc61-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2cc61-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cc61-115">備註</span><span class="sxs-lookup"><span data-stu-id="2cc61-115">Remarks</span></span>

<span data-ttu-id="2cc61-116">針對4.72 版和更早的版本，若要使用這個訊息儲存或還原工具列，工具列控制項的父視窗必須執行 [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) 通知程式碼的處理常式。</span><span class="sxs-lookup"><span data-stu-id="2cc61-116">For version 4.72 and earlier, to use this message to save or restore a toolbar, the parent window of the toolbar control must implement a handler for the [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification code.</span></span> <span data-ttu-id="2cc61-117">工具列會發出此通知，以在每個按鈕還原時取得其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2cc61-117">The toolbar issues this notification to retrieve information about each button as it is restored.</span></span>

<span data-ttu-id="2cc61-118">5.80 版包含新的儲存/還原選項。</span><span class="sxs-lookup"><span data-stu-id="2cc61-118">Version 5.80 includes a new save/restore option.</span></span> <span data-ttu-id="2cc61-119">在程式開始時，當每個按鈕儲存或還原時，您的應用程式將會收到 [TBN \_ 儲存](tbn-save.md) 或 [TBN \_ 還原](tbn-restore.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="2cc61-119">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification.</span></span> <span data-ttu-id="2cc61-120">若要使用此選項，您必須執行通知處理常式，為 Shell 提供成功儲存或還原工具列狀態所需的點陣圖和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="2cc61-120">To use this option, you must implement notification handlers to provide the Shell with the bitmap and state information it needs to successfully save or restore the toolbar state.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc61-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cc61-121">Requirements</span></span>



| <span data-ttu-id="2cc61-122">需求</span><span class="sxs-lookup"><span data-stu-id="2cc61-122">Requirement</span></span> | <span data-ttu-id="2cc61-123">值</span><span class="sxs-lookup"><span data-stu-id="2cc61-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc61-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2cc61-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc61-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2cc61-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2cc61-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2cc61-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc61-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2cc61-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2cc61-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2cc61-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc61-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc61-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2cc61-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="2cc61-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2cc61-131">**TB \_SAVERESTOREW** (Unicode) 和 **TB \_ SAVERESTOREA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="2cc61-131">**TB\_SAVERESTOREW** (Unicode) and **TB\_SAVERESTOREA** (ANSI)</span></span><br/>             |



 

 





