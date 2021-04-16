---
title: 'WM_COMPAREITEM 訊息 (Winuser .h) '
description: 傳送來判斷新專案在主控描繪下拉式方塊或清單方塊的排序清單中的相對位置。
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464240"
---
# <a name="wm_compareitem-message"></a><span data-ttu-id="e348b-104">WM \_ COMPAREITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="e348b-104">WM\_COMPAREITEM message</span></span>

<span data-ttu-id="e348b-105">傳送來判斷新專案在主控描繪下拉式方塊或清單方塊的排序清單中的相對位置。</span><span class="sxs-lookup"><span data-stu-id="e348b-105">Sent to determine the relative position of a new item in the sorted list of an owner-drawn combo box or list box.</span></span> <span data-ttu-id="e348b-106">每當應用程式加入新的專案時，系統會將此訊息傳送給以 [**CBS \_ 排序**](combo-box-styles.md) 或 [**磅 \_ 排序**](list-box-styles.md) 樣式建立的下拉式方塊或清單方塊的擁有者。</span><span class="sxs-lookup"><span data-stu-id="e348b-106">Whenever the application adds a new item, the system sends this message to the owner of a combo box or list box created with the [**CBS\_SORT**](combo-box-styles.md) or [**LBS\_SORT**](list-box-styles.md) style.</span></span>


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e348b-107">參數</span><span class="sxs-lookup"><span data-stu-id="e348b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e348b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e348b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e348b-109">指定傳送 **WM \_ COMPAREITEM** 訊息之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e348b-109">Specifies the identifier of the control that sent the **WM\_COMPAREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="e348b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e348b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e348b-111">[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)結構的指標，其中包含組合或清單方塊中兩個專案的識別碼和應用程式提供的資料。</span><span class="sxs-lookup"><span data-stu-id="e348b-111">Pointer to a [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure that contains the identifiers and application-supplied data for two items in the combo or list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e348b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e348b-112">Return value</span></span>

<span data-ttu-id="e348b-113">傳回值指出兩個專案的相對位置。</span><span class="sxs-lookup"><span data-stu-id="e348b-113">The return value indicates the relative position of the two items.</span></span> <span data-ttu-id="e348b-114">它可能是下表所示的任何值。</span><span class="sxs-lookup"><span data-stu-id="e348b-114">It may be any of the values shown in the following table.</span></span>



| <span data-ttu-id="e348b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e348b-115">Return code</span></span>                                                                          | <span data-ttu-id="e348b-116">Description</span><span class="sxs-lookup"><span data-stu-id="e348b-116">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="e348b-117"><dt>**值**</dt></span><span class="sxs-lookup"><span data-stu-id="e348b-117"><dt>**Value**</dt></span></span> </dl> | <span data-ttu-id="e348b-118">意義</span><span class="sxs-lookup"><span data-stu-id="e348b-118">Meaning</span></span><br/>                                           |
| <dl> <span data-ttu-id="e348b-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="e348b-119"><dt>**-1**</dt></span></span> </dl>    | <span data-ttu-id="e348b-120">專案1在專案2之前的排序次序。</span><span class="sxs-lookup"><span data-stu-id="e348b-120">Item 1 precedes item 2 in the sorted order.</span></span><br/>       |
| <dl> <span data-ttu-id="e348b-121"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="e348b-121"><dt>**0**</dt></span></span> </dl>     | <span data-ttu-id="e348b-122">專案1和2在排序的順序中是相等的。</span><span class="sxs-lookup"><span data-stu-id="e348b-122">Items 1 and 2 are equivalent in the sorted order.</span></span><br/> |
| <dl> <span data-ttu-id="e348b-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e348b-123"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="e348b-124">專案1會依照排序次序來追蹤專案2。</span><span class="sxs-lookup"><span data-stu-id="e348b-124">Item 1 follows item 2 in the sorted order.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="e348b-125">備註</span><span class="sxs-lookup"><span data-stu-id="e348b-125">Remarks</span></span>

<span data-ttu-id="e348b-126">當主控描繪下拉式方塊或清單方塊的擁有者收到此訊息時，擁有者會傳回值，指出 [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) 結構所指定的專案會出現在另一個專案之前。</span><span class="sxs-lookup"><span data-stu-id="e348b-126">When the owner of an owner-drawn combo box or list box receives this message, the owner returns a value indicating which of the items specified by the [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure will appear before the other.</span></span> <span data-ttu-id="e348b-127">一般而言，系統會傳送此訊息數次，直到它決定新專案的確切位置。</span><span class="sxs-lookup"><span data-stu-id="e348b-127">Typically, the system sends this message several times until it determines the exact position for the new item.</span></span>

<span data-ttu-id="e348b-128">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **布林** 值，並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="e348b-128">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="e348b-129">\_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e348b-129">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e348b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e348b-130">Requirements</span></span>



| <span data-ttu-id="e348b-131">需求</span><span class="sxs-lookup"><span data-stu-id="e348b-131">Requirement</span></span> | <span data-ttu-id="e348b-132">值</span><span class="sxs-lookup"><span data-stu-id="e348b-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e348b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e348b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e348b-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e348b-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e348b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e348b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e348b-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e348b-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e348b-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e348b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e348b-138"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e348b-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e348b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e348b-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="e348b-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="e348b-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e348b-141">**COMPAREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="e348b-141">**COMPAREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

<span data-ttu-id="e348b-142">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="e348b-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e348b-143">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="e348b-143">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

