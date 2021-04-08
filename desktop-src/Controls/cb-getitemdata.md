---
title: 'CB_GETITEMDATA 訊息 (Winuser .h) '
description: 應用程式會將 CB \_ GETITEMDATA 訊息傳送至下拉式方塊，以抓取與下拉式方塊中指定之專案相關聯的應用程式提供值。
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685896"
---
# <a name="cb_getitemdata-message"></a><span data-ttu-id="739b4-104">CB \_ GETITEMDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="739b4-104">CB\_GETITEMDATA message</span></span>

<span data-ttu-id="739b4-105">應用程式會將 **CB \_ GETITEMDATA** 訊息傳送至下拉式方塊，以抓取與下拉式方塊中指定之專案相關聯的應用程式提供值。</span><span class="sxs-lookup"><span data-stu-id="739b4-105">An application sends a **CB\_GETITEMDATA** message to a combo box to retrieve the application-supplied value associated with the specified item in the combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="739b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="739b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="739b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="739b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="739b4-108">項目之以零起始的索引。</span><span class="sxs-lookup"><span data-stu-id="739b4-108">The zero-based index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="739b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="739b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="739b4-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="739b4-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="739b4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="739b4-111">Return value</span></span>

<span data-ttu-id="739b4-112">傳回值是與專案相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="739b4-112">The return value is the value associated with the item.</span></span> <span data-ttu-id="739b4-113">如果發生錯誤，則為 CB \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="739b4-113">If an error occurs, it is CB\_ERR.</span></span>

<span data-ttu-id="739b4-114">如果專案是在建立時沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md)樣式的主控描繪下拉式方塊中，則傳回值是已將專案新增至下拉式方塊之 [**cb \_ ADDSTRING**](cb-addstring.md)或 [**cb \_ INSERTSTRING**](cb-insertstring.md)訊息的 *lParam* 參數中所包含的值。</span><span class="sxs-lookup"><span data-stu-id="739b4-114">If the item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the return value is the value contained in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message, that added the item to the combo box.</span></span> <span data-ttu-id="739b4-115">如果未使用 **CBS \_ HASSTRINGS** 樣式，則傳回值是包含在 [**CB \_ SETITEMDATA**](cb-setitemdata.md)訊息中的 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="739b4-115">If the **CBS\_HASSTRINGS** style was not used, the return value is the *lParam* parameter contained in a [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="739b4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="739b4-116">Requirements</span></span>



| <span data-ttu-id="739b4-117">需求</span><span class="sxs-lookup"><span data-stu-id="739b4-117">Requirement</span></span> | <span data-ttu-id="739b4-118">值</span><span class="sxs-lookup"><span data-stu-id="739b4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="739b4-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="739b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="739b4-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="739b4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="739b4-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="739b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="739b4-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="739b4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="739b4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="739b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="739b4-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="739b4-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="739b4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="739b4-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="739b4-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="739b4-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="739b4-127">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="739b4-127">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="739b4-128">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="739b4-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="739b4-129">**CB \_ SETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="739b4-129">**CB\_SETITEMDATA**</span></span>](cb-setitemdata.md)
</dt> </dl>

 

 





