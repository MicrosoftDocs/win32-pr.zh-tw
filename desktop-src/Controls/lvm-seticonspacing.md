---
title: 'LVM_SETICONSPACING 訊息 (Commctrl .h) '
description: 在具有 LVS) 圖示樣式的清單視圖控制項中，設定圖示之間的間距 \_ 。 您可以明確地傳送此訊息，或使用 ListView \_ SetIconSpacing 宏來傳送。
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843092"
---
# <a name="lvm_seticonspacing-message"></a><span data-ttu-id="f1dbe-105">LVM \_ SETICONSPACING 訊息</span><span class="sxs-lookup"><span data-stu-id="f1dbe-105">LVM\_SETICONSPACING message</span></span>

<span data-ttu-id="f1dbe-106">在具有 [**lvs) \_ 圖示**](list-view-window-styles.md) 樣式的清單視圖控制項中，設定圖示之間的間距。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-106">Sets the spacing between icons in list-view controls that have the [**LVS\_ICON**](list-view-window-styles.md) style.</span></span> <span data-ttu-id="f1dbe-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-107">You can send this message explicitly or by using the [**ListView\_SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1dbe-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1dbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1dbe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1dbe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dbe-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f1dbe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1dbe-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dbe-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定要在 X 軸上的圖示之間設定的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the distance, in pixels, to set between icons on the x-axis.</span></span> <span data-ttu-id="f1dbe-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定要在 y 軸上的圖示之間設定的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the distance, in pixels, to set between icons on the y-axis.</span></span> <span data-ttu-id="f1dbe-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-114">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1dbe-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1dbe-115">Return value</span></span>

<span data-ttu-id="f1dbe-116">傳回 **DWORD** 值，其中包含低字組中之前的 X 軸距離，以及高單字中先前的 y 軸距離。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-116">Returns a **DWORD** value that contains the previous x-axis distance in the low word, and the previous y-axis distance in the high word.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1dbe-117">備註</span><span class="sxs-lookup"><span data-stu-id="f1dbe-117">Remarks</span></span>

<span data-ttu-id="f1dbe-118">*LParam* 的值會相對於圖示點陣圖的左上角。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-118">Values for *lParam* are relative to the upper-left corner of an icon bitmap.</span></span> <span data-ttu-id="f1dbe-119">因此，若要在不重迭的圖示之間設定間距， *lParam* 值必須包含圖示的大小，以及圖示之間所需的空白空間量。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-119">Therefore, to set spacing between icons that do not overlap, the *lParam* values must include the size of the icon, plus the amount of empty space desired between icons.</span></span> <span data-ttu-id="f1dbe-120">不包含圖示寬度的值會導致重迭。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-120">Values that do not include the width of the icon will result in overlaps.</span></span>

<span data-ttu-id="f1dbe-121">定義圖示間距時， *lParam* 值必須設定為4或更大。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-121">When defining the icon spacing, the *lParam* values must set to 4 or larger.</span></span> <span data-ttu-id="f1dbe-122">較小的值不會產生所需的版面配置。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-122">Smaller values will not yield the desired layout.</span></span> <span data-ttu-id="f1dbe-123">若要將圖示重設為預設間距，請將 *lParam* 值設為-1。</span><span class="sxs-lookup"><span data-stu-id="f1dbe-123">To reset the icons to the default spacing, set the *lParam* values to -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1dbe-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1dbe-124">Requirements</span></span>



| <span data-ttu-id="f1dbe-125">需求</span><span class="sxs-lookup"><span data-stu-id="f1dbe-125">Requirement</span></span> | <span data-ttu-id="f1dbe-126">值</span><span class="sxs-lookup"><span data-stu-id="f1dbe-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1dbe-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1dbe-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1dbe-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1dbe-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1dbe-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1dbe-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1dbe-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1dbe-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1dbe-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f1dbe-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1dbe-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1dbe-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

