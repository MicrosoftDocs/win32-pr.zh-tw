---
title: 'BCM_GETNOTE 訊息 (Commctrl .h) '
description: 取得與命令連結按鈕相關聯的備註文字。 您可以明確地傳送此訊息，或使用按鈕 \_ GetNote 宏。
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967541"
---
# <a name="bcm_getnote-message"></a><span data-ttu-id="5f7ab-105">BCM \_ GETNOTE 訊息</span><span class="sxs-lookup"><span data-stu-id="5f7ab-105">BCM\_GETNOTE message</span></span>

<span data-ttu-id="5f7ab-106">取得與命令連結按鈕相關聯的備註文字。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-106">Gets the text of the note associated with a command link button.</span></span> <span data-ttu-id="5f7ab-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) 宏。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-107">You can send this message explicitly or use the [**Button\_GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f7ab-108">參數</span><span class="sxs-lookup"><span data-stu-id="5f7ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f7ab-109">*wParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5f7ab-109">*wParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f7ab-110">**DWORD** ，指定 *lParam* 所指向的緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-110">A **DWORD** that specifies the size of the buffer pointed to by *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="5f7ab-111">*lParam* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5f7ab-111">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f7ab-112">要接收文字的字串緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-112">The string buffer to receive the text.</span></span> <span data-ttu-id="5f7ab-113">緩衝區必須夠大，才能容納終止的 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-113">The buffer must be large enough to accommodate the terminating NULL character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f7ab-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f7ab-114">Return value</span></span>

<span data-ttu-id="5f7ab-115">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-115">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="5f7ab-116">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-116">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f7ab-117">備註</span><span class="sxs-lookup"><span data-stu-id="5f7ab-117">Remarks</span></span>

<span data-ttu-id="5f7ab-118">**BCM \_ GETNOTE** 訊息只適用于具有 [**BS \_ COMMANDLINK**](button-styles.md)或 [**BS \_ DEFCOMMANDLINK**](button-styles.md)按鈕樣式的按鈕。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-118">The **BCM\_GETNOTE** message works only with buttons that have the [**BS\_COMMANDLINK**](button-styles.md) or [**BS\_DEFCOMMANDLINK**](button-styles.md) button style.</span></span>

<span data-ttu-id="5f7ab-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 將包含：</span><span class="sxs-lookup"><span data-stu-id="5f7ab-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will contain:</span></span>

-   <span data-ttu-id="5f7ab-120">\_ \_ 如果按鈕沒有 [**BS \_ DEFCOMMANDLINK**](button-styles.md)或 [**BS \_ COMMANDLINK**](button-styles.md)樣式，則不支援錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-120">ERROR\_NOT\_SUPPORTED, if the button does not have the [**BS\_DEFCOMMANDLINK**](button-styles.md) or [**BS\_COMMANDLINK**](button-styles.md) style.</span></span>
-   <span data-ttu-id="5f7ab-121">\_緩衝區不足 \_ ，如果 *lParam* 緩衝區太小，則為錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-121">ERROR\_INSUFFICIENT\_BUFFER, if the *lParam* buffer is too small.</span></span> <span data-ttu-id="5f7ab-122">*WParam* 參數將包含所需的緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f7ab-122">The *wParam* parameter will contain the required buffer size, in characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f7ab-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f7ab-123">Requirements</span></span>



| <span data-ttu-id="5f7ab-124">需求</span><span class="sxs-lookup"><span data-stu-id="5f7ab-124">Requirement</span></span> | <span data-ttu-id="5f7ab-125">值</span><span class="sxs-lookup"><span data-stu-id="5f7ab-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7ab-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f7ab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5f7ab-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f7ab-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f7ab-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f7ab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5f7ab-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f7ab-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f7ab-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5f7ab-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f7ab-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f7ab-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f7ab-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f7ab-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f7ab-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="5f7ab-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f7ab-134">按鈕樣式</span><span class="sxs-lookup"><span data-stu-id="5f7ab-134">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="5f7ab-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="5f7ab-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f7ab-136">按鈕類型</span><span class="sxs-lookup"><span data-stu-id="5f7ab-136">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

