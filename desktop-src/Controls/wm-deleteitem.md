---
title: 'WM_DELETEITEM 訊息 (Winuser .h) '
description: 當清單方塊或下拉式方塊終結時，或是當 LB \_ DELETESTRING、lb \_ RESETCONTENT、CB \_ DELETESTRING 或 CB \_ RESETCONTENT 訊息移除專案時，傳送給清單方塊或下拉式方塊的擁有者。
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465145"
---
# <a name="wm_deleteitem-message"></a><span data-ttu-id="29fc4-104">WM \_ DELETEITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="29fc4-104">WM\_DELETEITEM message</span></span>

<span data-ttu-id="29fc4-105">當清單方塊或下拉式方塊終結時，或是當 [**lb \_ DELETESTRING**](lb-deletestring.md)、 [**lb \_ RESETCONTENT**](lb-resetcontent.md)、 [**CB \_ DELETESTRING**](cb-deletestring.md)或 [**CB \_ RESETCONTENT**](cb-resetcontent.md) 訊息移除專案時，傳送給清單方塊或下拉式方塊的擁有者。</span><span class="sxs-lookup"><span data-stu-id="29fc4-105">Sent to the owner of a list box or combo box when the list box or combo box is destroyed or when items are removed by the [**LB\_DELETESTRING**](lb-deletestring.md), [**LB\_RESETCONTENT**](lb-resetcontent.md), [**CB\_DELETESTRING**](cb-deletestring.md), or [**CB\_RESETCONTENT**](cb-resetcontent.md) message.</span></span> <span data-ttu-id="29fc4-106">系統會為每個已刪除的專案傳送 **WM \_ DELETEITEM** 訊息。</span><span class="sxs-lookup"><span data-stu-id="29fc4-106">The system sends a **WM\_DELETEITEM** message for each deleted item.</span></span> <span data-ttu-id="29fc4-107">系統會傳送包含非零專案資料之任何已刪除清單方塊或下拉式方塊專案的 **WM \_ DELETEITEM** 訊息。</span><span class="sxs-lookup"><span data-stu-id="29fc4-107">The system sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="29fc4-108">參數</span><span class="sxs-lookup"><span data-stu-id="29fc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29fc4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29fc4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29fc4-110">指定傳送 **WM \_ DELETEITEM** 訊息之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="29fc4-110">Specifies the identifier of the control that sent the **WM\_DELETEITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="29fc4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29fc4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29fc4-112">[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)結構的指標，其中包含從清單方塊中刪除之專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="29fc4-112">Pointer to a [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) structure that contains information about the item deleted from a list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29fc4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="29fc4-113">Return value</span></span>

<span data-ttu-id="29fc4-114">如果應用程式處理此訊息，則應該傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="29fc4-114">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="29fc4-115">備註</span><span class="sxs-lookup"><span data-stu-id="29fc4-115">Remarks</span></span>

<span data-ttu-id="29fc4-116">Microsoft Windows NT 和更新版本： Windows 僅針對從主控描繪清單方塊中刪除的專案傳送 **WM \_ DELETEITEM** 訊息 (具有 [**磅 \_ OWNERDRAWFIXED**](list-box-styles.md) 或 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式) 或擁有者繪製的下拉式列示方塊， (使用 [**cbs \_ OWNERDRAWFIXED**](combo-box-styles.md) 或 [**cbs \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式) 。</span><span class="sxs-lookup"><span data-stu-id="29fc4-116">Microsoft Windows NT and later: Windows sends a **WM\_DELETEITEM** message only for items deleted from an owner-drawn list box (with the [**LBS\_OWNERDRAWFIXED**](list-box-styles.md) or [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style) or owner-drawn combo box (with the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style).</span></span>

<span data-ttu-id="29fc4-117">Windows 95： Windows 傳送包含非零專案資料之任何已刪除清單方塊或下拉式方塊專案的 **WM \_ DELETEITEM** 訊息。</span><span class="sxs-lookup"><span data-stu-id="29fc4-117">Windows 95: Windows sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>

## <a name="requirements"></a><span data-ttu-id="29fc4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="29fc4-118">Requirements</span></span>



| <span data-ttu-id="29fc4-119">需求</span><span class="sxs-lookup"><span data-stu-id="29fc4-119">Requirement</span></span> | <span data-ttu-id="29fc4-120">值</span><span class="sxs-lookup"><span data-stu-id="29fc4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29fc4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29fc4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="29fc4-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29fc4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="29fc4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29fc4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="29fc4-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29fc4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29fc4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="29fc4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="29fc4-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="29fc4-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29fc4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29fc4-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="29fc4-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="29fc4-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29fc4-129">**CB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="29fc4-129">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="29fc4-130">**CB \_ RESETCONTENT**</span><span class="sxs-lookup"><span data-stu-id="29fc4-130">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="29fc4-131">**DELETEITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="29fc4-131">**DELETEITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[<span data-ttu-id="29fc4-132">**LB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="29fc4-132">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="29fc4-133">**LB \_ RESETCONTENT**</span><span class="sxs-lookup"><span data-stu-id="29fc4-133">**LB\_RESETCONTENT**</span></span>](lb-resetcontent.md)
</dt> </dl>

 

 





