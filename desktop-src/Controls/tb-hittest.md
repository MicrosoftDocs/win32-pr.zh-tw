---
title: 'TB_HITTEST 訊息 (Commctrl .h) '
description: 判中斷點位於工具列控制項中的位置。
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934195"
---
# <a name="tb_hittest-message"></a><span data-ttu-id="1ea9d-104">TB \_ system.windows.media.visualtreehelper.hittest 訊息</span><span class="sxs-lookup"><span data-stu-id="1ea9d-104">TB\_HITTEST message</span></span>

<span data-ttu-id="1ea9d-105">判中斷點位於工具列控制項中的位置。</span><span class="sxs-lookup"><span data-stu-id="1ea9d-105">Determines where a point lies in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ea9d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ea9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ea9d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ea9d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1ea9d-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1ea9d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1ea9d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ea9d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ea9d-110">[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，其中包含 **x** 成員中點擊測試的 x 座標，以及 **y** 成員中點擊測試的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="1ea9d-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the x-coordinate of the hit test in the **x** member and the y-coordinate of the hit test in the **y** member.</span></span> <span data-ttu-id="1ea9d-111">座標是相對於工具列的工作區。</span><span class="sxs-lookup"><span data-stu-id="1ea9d-111">The coordinates are relative to the toolbar's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ea9d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ea9d-112">Return value</span></span>

<span data-ttu-id="1ea9d-113">傳回整數值。</span><span class="sxs-lookup"><span data-stu-id="1ea9d-113">Returns an integer value.</span></span> <span data-ttu-id="1ea9d-114">如果傳回值為零或正值，則為點所在之 nonseparator 專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="1ea9d-114">If the return value is zero or a positive value, it is the zero-based index of the nonseparator item in which the point lies.</span></span> <span data-ttu-id="1ea9d-115">如果傳回值為負數，則點不在按鈕中。</span><span class="sxs-lookup"><span data-stu-id="1ea9d-115">If the return value is negative, the point does not lie within a button.</span></span> <span data-ttu-id="1ea9d-116">傳回值的絕對值是分隔符號專案或最接近 nonseparator 專案的索引。</span><span class="sxs-lookup"><span data-stu-id="1ea9d-116">The absolute value of the return value is the index of a separator item or the nearest nonseparator item.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ea9d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ea9d-117">Requirements</span></span>



| <span data-ttu-id="1ea9d-118">需求</span><span class="sxs-lookup"><span data-stu-id="1ea9d-118">Requirement</span></span> | <span data-ttu-id="1ea9d-119">值</span><span class="sxs-lookup"><span data-stu-id="1ea9d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea9d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ea9d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ea9d-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ea9d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ea9d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ea9d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ea9d-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ea9d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ea9d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1ea9d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ea9d-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ea9d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

