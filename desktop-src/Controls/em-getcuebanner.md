---
title: 'EM_GETCUEBANNER 訊息 (Commctrl .h) '
description: 取得在編輯控制項中顯示為文字提示或提示的文字。
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935055"
---
# <a name="em_getcuebanner-message"></a><span data-ttu-id="4ce2f-104">EM \_ GETCUEBANNER 訊息</span><span class="sxs-lookup"><span data-stu-id="4ce2f-104">EM\_GETCUEBANNER message</span></span>

<span data-ttu-id="4ce2f-105">取得在編輯控制項中顯示為文字提示或提示的文字。</span><span class="sxs-lookup"><span data-stu-id="4ce2f-105">Gets the text that is displayed as the textual cue, or tip, in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ce2f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ce2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce2f-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ce2f-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce2f-108">Unicode 緩衝區的指標，此緩衝區會以文字提示的形式接收文字集。</span><span class="sxs-lookup"><span data-stu-id="4ce2f-108">A pointer to a Unicode buffer that receives the text set as the textual cue.</span></span> <span data-ttu-id="4ce2f-109">呼叫端負責配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ce2f-109">The caller is responsible for allocating the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4ce2f-110">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ce2f-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce2f-111">*WParam* 在 **WCHARs** 中所指向的緩衝區大小，包括終止的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ce2f-111">The size of the buffer pointed to by *wParam* in **WCHARs**, including the terminating **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce2f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ce2f-112">Return value</span></span>

<span data-ttu-id="4ce2f-113">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4ce2f-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ce2f-114">備註</span><span class="sxs-lookup"><span data-stu-id="4ce2f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4ce2f-115">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="4ce2f-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4ce2f-116">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4ce2f-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ce2f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ce2f-117">Requirements</span></span>



| <span data-ttu-id="4ce2f-118">需求</span><span class="sxs-lookup"><span data-stu-id="4ce2f-118">Requirement</span></span> | <span data-ttu-id="4ce2f-119">值</span><span class="sxs-lookup"><span data-stu-id="4ce2f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce2f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ce2f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce2f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ce2f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ce2f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ce2f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce2f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ce2f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ce2f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4ce2f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ce2f-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ce2f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ce2f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ce2f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce2f-127">**編輯 \_ GetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="4ce2f-127">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





