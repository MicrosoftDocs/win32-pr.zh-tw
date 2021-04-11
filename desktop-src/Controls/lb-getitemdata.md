---
title: 'LB_GETITEMDATA 訊息 (Winuser .h) '
description: 取得與指定清單方塊專案相關聯的應用程式定義值。
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- LB_GETITEMDATA message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105990"
---
# <a name="lb_getitemdata-message"></a><span data-ttu-id="10d33-104">LB \_ GETITEMDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="10d33-104">LB\_GETITEMDATA message</span></span>

<span data-ttu-id="10d33-105">取得與指定清單方塊專案相關聯的應用程式定義值。</span><span class="sxs-lookup"><span data-stu-id="10d33-105">Gets the application-defined value associated with the specified list box item.</span></span>

## <a name="parameters"></a><span data-ttu-id="10d33-106">參數</span><span class="sxs-lookup"><span data-stu-id="10d33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d33-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10d33-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10d33-108">項目的索引。</span><span class="sxs-lookup"><span data-stu-id="10d33-108">The index of the item.</span></span>

<span data-ttu-id="10d33-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。</span><span class="sxs-lookup"><span data-stu-id="10d33-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="10d33-110">這表示清單方塊不能包含超過32767個專案。</span><span class="sxs-lookup"><span data-stu-id="10d33-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="10d33-111">雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="10d33-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="10d33-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10d33-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10d33-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="10d33-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d33-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="10d33-114">Return value</span></span>

<span data-ttu-id="10d33-115">傳回值是與專案相關聯的值，如果發生錯誤，則為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="10d33-115">The return value is the value associated with the item, or LB\_ERR if an error occurs.</span></span> <span data-ttu-id="10d33-116">如果專案是在主控描繪清單方塊中，而且是以 [**磅 \_ HASSTRINGS**](list-box-styles.md)樣式建立的，則此值會在將專案新增至清單方塊的 [**lb \_ ADDSTRING**](lb-addstring.md)或 [**lb \_ INSERTSTRING**](lb-insertstring.md)訊息的 *lParam* 參數中。</span><span class="sxs-lookup"><span data-stu-id="10d33-116">If the item is in an owner-drawn list box and was created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this value was in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span> <span data-ttu-id="10d33-117">否則，它是 [**LB \_ SETITEMDATA**](lb-setitemdata.md)訊息 *lParam* 中的值。</span><span class="sxs-lookup"><span data-stu-id="10d33-117">Otherwise, it is the value in the *lParam* of the [**LB\_SETITEMDATA**](lb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d33-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="10d33-118">Requirements</span></span>



| <span data-ttu-id="10d33-119">需求</span><span class="sxs-lookup"><span data-stu-id="10d33-119">Requirement</span></span> | <span data-ttu-id="10d33-120">值</span><span class="sxs-lookup"><span data-stu-id="10d33-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d33-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10d33-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10d33-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10d33-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="10d33-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10d33-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10d33-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10d33-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10d33-125">標頭</span><span class="sxs-lookup"><span data-stu-id="10d33-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="10d33-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="10d33-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d33-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10d33-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="10d33-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="10d33-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10d33-129">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="10d33-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="10d33-130">**LB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="10d33-130">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="10d33-131">**LB \_ SETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="10d33-131">**LB\_SETITEMDATA**</span></span>](lb-setitemdata.md)
</dt> </dl>

 

 





