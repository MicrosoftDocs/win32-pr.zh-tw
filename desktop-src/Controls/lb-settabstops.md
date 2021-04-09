---
title: 'LB_SETTABSTOPS 訊息 (Winuser .h) '
description: 設定清單方塊中的定位停駐點位置。
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- LB_SETTABSTOPS message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844104"
---
# <a name="lb_settabstops-message"></a><span data-ttu-id="b3e7a-104">LB \_ SETTABSTOPS 訊息</span><span class="sxs-lookup"><span data-stu-id="b3e7a-104">LB\_SETTABSTOPS message</span></span>

<span data-ttu-id="b3e7a-105">設定清單方塊中的定位停駐點位置。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-105">Sets the tab-stop positions in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3e7a-106">參數</span><span class="sxs-lookup"><span data-stu-id="b3e7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e7a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3e7a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3e7a-108">指定制表位的數目。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-108">Specifies the number of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="b3e7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3e7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3e7a-110">包含索引標籤之整數陣列的第一個成員指標。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-110">Pointer to the first member of an array of integers containing the tab stops.</span></span> <span data-ttu-id="b3e7a-111">整數表示在清單方塊中選取之字型的平均字元寬度的季數。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-111">The integers represent the number of quarters of the average character width for the font that is selected into the list box.</span></span> <span data-ttu-id="b3e7a-112">例如，4的 tab 鍵會放在1.0 個字元的單位，而索引標籤停止的位置則是1.5 個平均字元單位。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-112">For example, a tab stop of 4 is placed at 1.0 character units, and a tab stop of 6 is placed at 1.5 average character units.</span></span> <span data-ttu-id="b3e7a-113">但是，如果清單方塊是對話方塊的一部分，則整數會在對話方塊範本單位中。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-113">However, if the list box is part of a dialog box, the integers are in dialog template units.</span></span> <span data-ttu-id="b3e7a-114">定位停駐點必須以遞增順序排序;不允許反向索引標籤。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-114">The tab stops must be sorted in ascending order; backward tabs are not allowed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3e7a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3e7a-115">Return value</span></span>

<span data-ttu-id="b3e7a-116">如果設定了所有指定的索引標籤，則傳回值為 **TRUE**;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-116">If all the specified tabs are set, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3e7a-117">備註</span><span class="sxs-lookup"><span data-stu-id="b3e7a-117">Remarks</span></span>

<span data-ttu-id="b3e7a-118">若要回應 **LB \_ SETTABSTOPS** 訊息，必須以 [**磅 \_ USETABSTOPS**](list-box-styles.md) 樣式建立清單方塊。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-118">To respond to the **LB\_SETTABSTOPS** message, the list box must have been created with the [**LBS\_USETABSTOPS**](list-box-styles.md) style.</span></span>

<span data-ttu-id="b3e7a-119">如果 *wParam* 為0，而 *lParam* 為 **Null**，則預設的 tab 鍵會停止為兩個對話方塊範本單位。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-119">If *wParam* is 0 and *lParam* is **NULL**, the default tab stop is two dialog template units.</span></span> <span data-ttu-id="b3e7a-120">如果 *wParam* 是1，則清單方塊會以 *lParam* 所指定的距離分隔 tab 鍵。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-120">If *wParam* is 1, the list box will have tab stops separated by the distance specified by *lParam*.</span></span>

<span data-ttu-id="b3e7a-121">如果 *lParam* 指向一個以上的值，將會針對 *lParam* 中的每個值設定制表位，最多可達 *wParam* 所指定的數位。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-121">If *lParam* points to more than a single value, a tab stop will be set for each value in *lParam*, up to the number specified by *wParam*.</span></span>

<span data-ttu-id="b3e7a-122">*LParam* 所指定的值位於對話方塊範本單位中，也就是對話方塊範本中使用的裝置獨立單位。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-122">The values specified by *lParam* are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="b3e7a-123">若要將度量從對話方塊範本單位轉換為螢幕單位 (圖元) ，請使用 [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) 函數。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-123">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="b3e7a-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *LParam* 所指向的緩衝區必須位於可寫入的記憶體中，即使訊息並未修改陣列也是一樣。</span><span class="sxs-lookup"><span data-stu-id="b3e7a-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The buffer pointed to by *lParam* must reside in writable memory, even though the message does not modify the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3e7a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3e7a-125">Requirements</span></span>



| <span data-ttu-id="b3e7a-126">需求</span><span class="sxs-lookup"><span data-stu-id="b3e7a-126">Requirement</span></span> | <span data-ttu-id="b3e7a-127">值</span><span class="sxs-lookup"><span data-stu-id="b3e7a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e7a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3e7a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e7a-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3e7a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b3e7a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3e7a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e7a-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3e7a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b3e7a-132">標頭</span><span class="sxs-lookup"><span data-stu-id="b3e7a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3e7a-133"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b3e7a-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3e7a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3e7a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e7a-135">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-135">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

