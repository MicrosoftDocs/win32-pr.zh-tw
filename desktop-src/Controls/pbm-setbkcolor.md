---
title: 'PBM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定進度列中的背景色彩。
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686167"
---
# <a name="pbm_setbkcolor-message"></a><span data-ttu-id="dec17-104">PBM \_ SETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="dec17-104">PBM\_SETBKCOLOR message</span></span>

<span data-ttu-id="dec17-105">設定進度列中的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="dec17-105">Sets the background color in the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="dec17-106">參數</span><span class="sxs-lookup"><span data-stu-id="dec17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec17-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dec17-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dec17-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="dec17-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dec17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dec17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dec17-110">**COLORREF** 值，指定新的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="dec17-110">**COLORREF** value that specifies the new background color.</span></span> <span data-ttu-id="dec17-111">指定 CLR \_ 預設值，使進度列使用其預設背景色彩。</span><span class="sxs-lookup"><span data-stu-id="dec17-111">Specify the CLR\_DEFAULT value to cause the progress bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec17-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dec17-112">Return value</span></span>

<span data-ttu-id="dec17-113">傳回先前的背景色彩，或 \_ 如果背景色彩為預設色彩，則為 CLR 預設值。</span><span class="sxs-lookup"><span data-stu-id="dec17-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec17-114">備註</span><span class="sxs-lookup"><span data-stu-id="dec17-114">Remarks</span></span>

<span data-ttu-id="dec17-115">啟用視覺化樣式時，此訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="dec17-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec17-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dec17-116">Requirements</span></span>



| <span data-ttu-id="dec17-117">需求</span><span class="sxs-lookup"><span data-stu-id="dec17-117">Requirement</span></span> | <span data-ttu-id="dec17-118">值</span><span class="sxs-lookup"><span data-stu-id="dec17-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dec17-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dec17-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dec17-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dec17-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dec17-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dec17-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dec17-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dec17-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dec17-123">標頭</span><span class="sxs-lookup"><span data-stu-id="dec17-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec17-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dec17-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





