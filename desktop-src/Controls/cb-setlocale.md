---
title: 'CB_SETLOCALE 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETLOCALE 訊息來設定下拉式方塊的目前地區設定。 如果下拉式方塊具有 CBS \_ 排序樣式，且使用 CB ADDSTRING 來新增字串 \_ ，則下拉式方塊的地區設定會影響清單專案的排序方式。
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465929"
---
# <a name="cb_setlocale-message"></a><span data-ttu-id="30855-105">CB \_ SETLOCALE 訊息</span><span class="sxs-lookup"><span data-stu-id="30855-105">CB\_SETLOCALE message</span></span>

<span data-ttu-id="30855-106">應用程式會傳送 **CB \_ SETLOCALE** 訊息來設定下拉式方塊的目前地區設定。</span><span class="sxs-lookup"><span data-stu-id="30855-106">An application sends a **CB\_SETLOCALE** message to set the current locale of the combo box.</span></span> <span data-ttu-id="30855-107">如果下拉式方塊具有 [**CBS \_ 排序**](combo-box-styles.md) 樣式，且使用 [**CB \_ ADDSTRING**](cb-addstring.md)來新增字串，則下拉式方塊的地區設定會影響清單專案的排序方式。</span><span class="sxs-lookup"><span data-stu-id="30855-107">If the combo box has the [**CBS\_SORT**](combo-box-styles.md) style and strings are added using [**CB\_ADDSTRING**](cb-addstring.md), the locale of a combo box affects how list items are sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="30855-108">參數</span><span class="sxs-lookup"><span data-stu-id="30855-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30855-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30855-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30855-110">指定下拉式方塊的地區設定識別碼，以在加入文字時用來排序。</span><span class="sxs-lookup"><span data-stu-id="30855-110">Specifies the locale identifier for the combo box to use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="30855-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30855-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30855-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="30855-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30855-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="30855-113">Return value</span></span>

<span data-ttu-id="30855-114">傳回值是先前的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="30855-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="30855-115">如果 *wParam* 指定系統上未安裝的地區設定，則傳回值為 CB \_ ERR，而且目前的下拉式列示方塊地區設定不會變更。</span><span class="sxs-lookup"><span data-stu-id="30855-115">If *wParam* specifies a locale not installed on the system, the return value is CB\_ERR and the current combo box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="30855-116">備註</span><span class="sxs-lookup"><span data-stu-id="30855-116">Remarks</span></span>

<span data-ttu-id="30855-117">使用 [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼，並使用 [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) 宏來建立語言識別項。</span><span class="sxs-lookup"><span data-stu-id="30855-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier and the [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) macro to construct a language identifier.</span></span> <span data-ttu-id="30855-118">語言識別項是由主要語言識別項和子語言識別項所組成。</span><span class="sxs-lookup"><span data-stu-id="30855-118">The language identifier is made up of a primary language identifier and a sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="30855-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="30855-119">Requirements</span></span>



| <span data-ttu-id="30855-120">需求</span><span class="sxs-lookup"><span data-stu-id="30855-120">Requirement</span></span> | <span data-ttu-id="30855-121">值</span><span class="sxs-lookup"><span data-stu-id="30855-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30855-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30855-122">Minimum supported client</span></span><br/> | <span data-ttu-id="30855-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30855-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30855-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30855-124">Minimum supported server</span></span><br/> | <span data-ttu-id="30855-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30855-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30855-126">標頭</span><span class="sxs-lookup"><span data-stu-id="30855-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="30855-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="30855-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30855-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30855-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="30855-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="30855-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30855-130">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="30855-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="30855-131">**CB \_ GETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="30855-131">**CB\_GETLOCALE**</span></span>](cb-getlocale.md)
</dt> <dt>

<span data-ttu-id="30855-132">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="30855-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="30855-133">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="30855-133">**MAKELANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[<span data-ttu-id="30855-134">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="30855-134">**MAKELCID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

