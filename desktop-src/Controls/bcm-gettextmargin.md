---
title: 'BCM_GETTEXTMARGIN 訊息 (Commctrl .h) '
description: 取得用來在按鈕控制項中繪製文字的邊界。 您可以明確地傳送此訊息，或使用按鈕 \_ GetTextMargin 宏。
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- BCM_GETTEXTMARGIN message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934277"
---
# <a name="bcm_gettextmargin-message"></a><span data-ttu-id="49de9-105">BCM \_ GETTEXTMARGIN 訊息</span><span class="sxs-lookup"><span data-stu-id="49de9-105">BCM\_GETTEXTMARGIN message</span></span>

<span data-ttu-id="49de9-106">取得用來在按鈕控制項中繪製文字的邊界。</span><span class="sxs-lookup"><span data-stu-id="49de9-106">Gets the margins used to draw text in a button control.</span></span> <span data-ttu-id="49de9-107">您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) 宏。</span><span class="sxs-lookup"><span data-stu-id="49de9-107">You can send this message explicitly or use the [**Button\_GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="49de9-108">參數</span><span class="sxs-lookup"><span data-stu-id="49de9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49de9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49de9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49de9-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="49de9-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49de9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49de9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49de9-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含用來繪製文字的邊界。</span><span class="sxs-lookup"><span data-stu-id="49de9-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49de9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="49de9-113">Return value</span></span>

<span data-ttu-id="49de9-114">如果訊息成功，則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="49de9-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="49de9-115">否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="49de9-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49de9-116">備註</span><span class="sxs-lookup"><span data-stu-id="49de9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49de9-117">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="49de9-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="49de9-118">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="49de9-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49de9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="49de9-119">Requirements</span></span>



| <span data-ttu-id="49de9-120">需求</span><span class="sxs-lookup"><span data-stu-id="49de9-120">Requirement</span></span> | <span data-ttu-id="49de9-121">值</span><span class="sxs-lookup"><span data-stu-id="49de9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49de9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49de9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49de9-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49de9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49de9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49de9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49de9-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49de9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49de9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="49de9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="49de9-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="49de9-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

