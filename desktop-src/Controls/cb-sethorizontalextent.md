---
title: 'CB_SETHORIZONTALEXTENT 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETHORIZONTALEXTENT 訊息，以圖元為單位來設定捲軸的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- CB_SETHORIZONTALEXTENT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465249"
---
# <a name="cb_sethorizontalextent-message"></a><span data-ttu-id="12e54-104">CB \_ SETHORIZONTALEXTENT 訊息</span><span class="sxs-lookup"><span data-stu-id="12e54-104">CB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="12e54-105">應用程式會傳送 **CB \_ SETHORIZONTALEXTENT** 訊息，以圖元為單位來設定捲軸的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。</span><span class="sxs-lookup"><span data-stu-id="12e54-105">An application sends the **CB\_SETHORIZONTALEXTENT** message to set the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="12e54-106">如果清單方塊的寬度小於此值，水準捲軸會水準滾動清單方塊中的專案。</span><span class="sxs-lookup"><span data-stu-id="12e54-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="12e54-107">如果清單方塊的寬度等於或大於此值，則會隱藏水準捲軸，或者，如果下拉式方塊的 [**CBS \_ DISABLENOSCROLL**](combo-box-styles.md) 樣式為停用。</span><span class="sxs-lookup"><span data-stu-id="12e54-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden or, if the combo box has the [**CBS\_DISABLENOSCROLL**](combo-box-styles.md) style, disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="12e54-108">參數</span><span class="sxs-lookup"><span data-stu-id="12e54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e54-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12e54-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12e54-110">指定清單方塊的可滾動寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="12e54-110">Specifies the scrollable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="12e54-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12e54-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12e54-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="12e54-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12e54-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="12e54-113">Requirements</span></span>



| <span data-ttu-id="12e54-114">需求</span><span class="sxs-lookup"><span data-stu-id="12e54-114">Requirement</span></span> | <span data-ttu-id="12e54-115">值</span><span class="sxs-lookup"><span data-stu-id="12e54-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e54-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12e54-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12e54-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12e54-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12e54-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12e54-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12e54-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12e54-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12e54-120">標頭</span><span class="sxs-lookup"><span data-stu-id="12e54-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12e54-121"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="12e54-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e54-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12e54-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e54-123">**CB \_ GETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="12e54-123">**CB\_GETHORIZONTALEXTENT**</span></span>](cb-gethorizontalextent.md)
</dt> </dl>

 

 





