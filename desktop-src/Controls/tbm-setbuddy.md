---
title: 'TBM_SETBUDDY 訊息 (Commctrl .h) '
description: 將視窗指派為 [查看] 控制項的合作者視窗。 [並排顯示] 視窗會自動顯示在相對於控制項方向 (水準或垂直) 的位置。
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024796"
---
# <a name="tbm_setbuddy-message"></a><span data-ttu-id="459bf-105">TBM \_ SETBUDDY 訊息</span><span class="sxs-lookup"><span data-stu-id="459bf-105">TBM\_SETBUDDY message</span></span>

<span data-ttu-id="459bf-106">將視窗指派為 [查看] 控制項的合作者視窗。</span><span class="sxs-lookup"><span data-stu-id="459bf-106">Assigns a window as the buddy window for a trackbar control.</span></span> <span data-ttu-id="459bf-107">[並排顯示] 視窗會自動顯示在相對於控制項方向 (水準或垂直) 的位置。</span><span class="sxs-lookup"><span data-stu-id="459bf-107">Trackbar buddy windows are automatically displayed in a location relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="459bf-108">參數</span><span class="sxs-lookup"><span data-stu-id="459bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="459bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="459bf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="459bf-110">值，指定要顯示好友視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="459bf-110">Value specifying the location at which to display the buddy window.</span></span> <span data-ttu-id="459bf-111">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="459bf-111">This value can be one of the following:</span></span>



| <span data-ttu-id="459bf-112">值</span><span class="sxs-lookup"><span data-stu-id="459bf-112">Value</span></span>                                                                                                                                | <span data-ttu-id="459bf-113">意義</span><span class="sxs-lookup"><span data-stu-id="459bf-113">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="459bf-114"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="459bf-114"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="459bf-115">如果 [對齊程式] 控制項使用 [ [**tb] \_ HORZ**](trackbar-control-styles.md) 樣式，則會在 [顯示] 的左邊顯示好友。</span><span class="sxs-lookup"><span data-stu-id="459bf-115">The buddy will appear to the left of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="459bf-116">如果使用 [Tb] [**\_ 垂直**](trackbar-control-styles.md) 樣式，則會在 [顯示] 控制項上方顯示好友。</span><span class="sxs-lookup"><span data-stu-id="459bf-116">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears above the trackbar control.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="459bf-117"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="459bf-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="459bf-118">如果 [HORZ] 控制項使用 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會在 [顯示] 右邊顯示好友。</span><span class="sxs-lookup"><span data-stu-id="459bf-118">The buddy will appear to the right of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="459bf-119">如果使用 [Tb] [**\_ 垂直**](trackbar-control-styles.md) 樣式，則會在 [顯示] 控制項下方顯示好友。</span><span class="sxs-lookup"><span data-stu-id="459bf-119">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears below the trackbar control.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="459bf-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="459bf-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="459bf-121">將設定為 [處理常式] 控制項的合作者的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="459bf-121">Handle to the window that will be set as the trackbar control's buddy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="459bf-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="459bf-122">Return value</span></span>

<span data-ttu-id="459bf-123">傳回先前指派給該位置之控制項的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="459bf-123">Returns the handle to the window that was previously assigned to the control at that location.</span></span>

## <a name="remarks"></a><span data-ttu-id="459bf-124">備註</span><span class="sxs-lookup"><span data-stu-id="459bf-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="459bf-125">追蹤控制項最多可支援兩個好友視窗。</span><span class="sxs-lookup"><span data-stu-id="459bf-125">Trackbar controls support up to two buddy windows.</span></span> <span data-ttu-id="459bf-126">當您必須在控制項的每一端顯示文字或影像時，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="459bf-126">This can be useful when you must display text or images at each end of the control.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="459bf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="459bf-127">Requirements</span></span>



| <span data-ttu-id="459bf-128">需求</span><span class="sxs-lookup"><span data-stu-id="459bf-128">Requirement</span></span> | <span data-ttu-id="459bf-129">值</span><span class="sxs-lookup"><span data-stu-id="459bf-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="459bf-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="459bf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="459bf-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="459bf-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="459bf-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="459bf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="459bf-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="459bf-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="459bf-134">標頭</span><span class="sxs-lookup"><span data-stu-id="459bf-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="459bf-135"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="459bf-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





