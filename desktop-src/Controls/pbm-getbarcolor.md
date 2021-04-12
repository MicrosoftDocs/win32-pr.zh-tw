---
title: 'PBM_GETBARCOLOR 訊息 (Commctrl .h) '
description: 取得進度列的色彩。
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104801"
---
# <a name="pbm_getbarcolor-message"></a><span data-ttu-id="d3d00-104">PBM \_ GETBARCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="d3d00-104">PBM\_GETBARCOLOR message</span></span>

<span data-ttu-id="d3d00-105">取得進度列的色彩。</span><span class="sxs-lookup"><span data-stu-id="d3d00-105">Gets the color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3d00-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3d00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d00-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3d00-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d3d00-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d3d00-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d3d00-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3d00-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d3d00-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d3d00-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d00-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3d00-111">Return value</span></span>

<span data-ttu-id="d3d00-112">傳回進度列的色彩。</span><span class="sxs-lookup"><span data-stu-id="d3d00-112">Returns the color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3d00-113">備註</span><span class="sxs-lookup"><span data-stu-id="d3d00-113">Remarks</span></span>

<span data-ttu-id="d3d00-114">這是 [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) 訊息所設定的色彩。</span><span class="sxs-lookup"><span data-stu-id="d3d00-114">This is the color set by the [**PBM\_SETBARCOLOR**](pbm-setbarcolor.md) message.</span></span> <span data-ttu-id="d3d00-115">預設值是 CLR \_ default，定義于 commctrl 中。</span><span class="sxs-lookup"><span data-stu-id="d3d00-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="d3d00-116">此函式只會影響傳統模式，而不會影響任何視覺效果樣式。</span><span class="sxs-lookup"><span data-stu-id="d3d00-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d00-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3d00-117">Requirements</span></span>



| <span data-ttu-id="d3d00-118">需求</span><span class="sxs-lookup"><span data-stu-id="d3d00-118">Requirement</span></span> | <span data-ttu-id="d3d00-119">值</span><span class="sxs-lookup"><span data-stu-id="d3d00-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d00-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3d00-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d00-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3d00-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3d00-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3d00-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d00-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3d00-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3d00-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d3d00-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3d00-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3d00-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





