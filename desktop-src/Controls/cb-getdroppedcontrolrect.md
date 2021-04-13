---
title: 'CB_GETDROPPEDCONTROLRECT 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ GETDROPPEDCONTROLRECT 訊息，以取得下拉式方塊中下拉式方塊的螢幕座標。
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465720"
---
# <a name="cb_getdroppedcontrolrect-message"></a><span data-ttu-id="cc54d-104">CB \_ GETDROPPEDCONTROLRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="cc54d-104">CB\_GETDROPPEDCONTROLRECT message</span></span>

<span data-ttu-id="cc54d-105">應用程式會傳送 **CB \_ GETDROPPEDCONTROLRECT** 訊息，以取得下拉式方塊中下拉式方塊的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="cc54d-105">An application sends a **CB\_GETDROPPEDCONTROLRECT** message to retrieve the screen coordinates of a combo box in its dropped-down state.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc54d-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc54d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc54d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc54d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc54d-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="cc54d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cc54d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc54d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc54d-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會在其中斷狀態中接收下拉式方塊的座標。</span><span class="sxs-lookup"><span data-stu-id="cc54d-110">A pointer to the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the coordinates of the combo box in its dropped-down state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc54d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc54d-111">Return value</span></span>

<span data-ttu-id="cc54d-112">如果訊息成功，則傳回值為非零。</span><span class="sxs-lookup"><span data-stu-id="cc54d-112">If the message succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="cc54d-113">如果訊息失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="cc54d-113">If the message fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc54d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc54d-114">Requirements</span></span>



| <span data-ttu-id="cc54d-115">需求</span><span class="sxs-lookup"><span data-stu-id="cc54d-115">Requirement</span></span> | <span data-ttu-id="cc54d-116">值</span><span class="sxs-lookup"><span data-stu-id="cc54d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc54d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc54d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc54d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc54d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cc54d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc54d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc54d-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc54d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cc54d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cc54d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc54d-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cc54d-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc54d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc54d-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc54d-124">[**矩形**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc54d-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

