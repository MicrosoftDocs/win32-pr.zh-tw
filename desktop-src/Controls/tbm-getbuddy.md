---
title: 'TBM_GETBUDDY 訊息 (Commctrl .h) '
description: 抓取指定位置上的 [查看點] 控制項好友視窗控制碼。 指定的位置是相對於控制項的方向 (水準或垂直) 。
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935153"
---
# <a name="tbm_getbuddy-message"></a><span data-ttu-id="810e8-105">TBM \_ GETBUDDY 訊息</span><span class="sxs-lookup"><span data-stu-id="810e8-105">TBM\_GETBUDDY message</span></span>

<span data-ttu-id="810e8-106">抓取指定位置上的 [查看點] 控制項好友視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="810e8-106">Retrieves the handle to a trackbar control buddy window at a given location.</span></span> <span data-ttu-id="810e8-107">指定的位置是相對於控制項的方向 (水準或垂直) 。</span><span class="sxs-lookup"><span data-stu-id="810e8-107">The specified location is relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="810e8-108">參數</span><span class="sxs-lookup"><span data-stu-id="810e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="810e8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="810e8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="810e8-110">指出將會依相對位置抓取哪個合作者視窗控制碼的值。</span><span class="sxs-lookup"><span data-stu-id="810e8-110">Value indicating which buddy window handle will be retrieved, by relative location.</span></span> <span data-ttu-id="810e8-111">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="810e8-111">This value can be one of the following:</span></span>



| <span data-ttu-id="810e8-112">值</span><span class="sxs-lookup"><span data-stu-id="810e8-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="810e8-113">意義</span><span class="sxs-lookup"><span data-stu-id="810e8-113">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="810e8-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="810e8-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="810e8-115">抓取對等的合作者左邊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="810e8-115">Retrieves the handle to the buddy to the left of the trackbar.</span></span> <span data-ttu-id="810e8-116">如果 [顯示] 控制項使用的是 [ [**tb] \_ 垂直**](trackbar-control-styles.md) 樣式，則訊息將會抓取 [資訊] 上方的合作者。</span><span class="sxs-lookup"><span data-stu-id="810e8-116">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy above the trackbar.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="810e8-117"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="810e8-117"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="810e8-118">抓取對等的合作者右邊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="810e8-118">Retrieves the handle to the buddy to the right of the trackbar.</span></span> <span data-ttu-id="810e8-119">如果 [顯示] 控制項使用的是 [ [**tb] \_ 垂直**](trackbar-control-styles.md) 樣式，則訊息將會抓取下方的合作者。</span><span class="sxs-lookup"><span data-stu-id="810e8-119">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy below the trackbar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="810e8-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="810e8-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="810e8-121">必須為零。</span><span class="sxs-lookup"><span data-stu-id="810e8-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="810e8-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="810e8-122">Return value</span></span>

<span data-ttu-id="810e8-123">在 *wParam* 所指定的位置上，傳回好友視窗的控制碼，如果該位置沒有任何好友視窗，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="810e8-123">Returns the handle to the buddy window at the location specified by *wParam*, or **NULL** if no buddy window exists at that location.</span></span>

## <a name="requirements"></a><span data-ttu-id="810e8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="810e8-124">Requirements</span></span>



| <span data-ttu-id="810e8-125">需求</span><span class="sxs-lookup"><span data-stu-id="810e8-125">Requirement</span></span> | <span data-ttu-id="810e8-126">值</span><span class="sxs-lookup"><span data-stu-id="810e8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="810e8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="810e8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="810e8-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="810e8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="810e8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="810e8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="810e8-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="810e8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="810e8-131">標頭</span><span class="sxs-lookup"><span data-stu-id="810e8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="810e8-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="810e8-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





