---
title: 'PBM_SETBARCOLOR 訊息 (Commctrl .h) '
description: 在進度列控制項中設定進度指標列的色彩。
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508915"
---
# <a name="pbm_setbarcolor-message"></a><span data-ttu-id="d0214-104">PBM \_ SETBARCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="d0214-104">PBM\_SETBARCOLOR message</span></span>

<span data-ttu-id="d0214-105">在進度列控制項中設定進度指標列的色彩。</span><span class="sxs-lookup"><span data-stu-id="d0214-105">Sets the color of the progress indicator bar in the progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0214-106">參數</span><span class="sxs-lookup"><span data-stu-id="d0214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0214-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0214-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0214-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d0214-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d0214-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0214-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0214-110">**COLORREF** 值，指定新的進度指標列色彩。</span><span class="sxs-lookup"><span data-stu-id="d0214-110">The **COLORREF** value that specifies the new progress indicator bar color.</span></span> <span data-ttu-id="d0214-111">指定 CLR \_ 預設值會使進度列使用其預設的進度指示器列色彩。</span><span class="sxs-lookup"><span data-stu-id="d0214-111">Specifying the CLR\_DEFAULT value causes the progress bar to use its default progress indicator bar color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0214-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0214-112">Return value</span></span>

<span data-ttu-id="d0214-113">傳回上一個進度指標列色彩，或 \_ 如果進度指示器列色彩是預設色彩，則為 CLR 預設值。</span><span class="sxs-lookup"><span data-stu-id="d0214-113">Returns the previous progress indicator bar color, or CLR\_DEFAULT if the progress indicator bar color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0214-114">備註</span><span class="sxs-lookup"><span data-stu-id="d0214-114">Remarks</span></span>

<span data-ttu-id="d0214-115">啟用視覺化樣式時，此訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="d0214-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0214-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0214-116">Requirements</span></span>



| <span data-ttu-id="d0214-117">需求</span><span class="sxs-lookup"><span data-stu-id="d0214-117">Requirement</span></span> | <span data-ttu-id="d0214-118">值</span><span class="sxs-lookup"><span data-stu-id="d0214-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0214-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0214-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0214-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0214-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0214-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0214-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0214-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0214-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0214-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d0214-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0214-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0214-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





