---
title: 'CB_SETITEMDATA 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETITEMDATA 訊息，以設定與下拉式方塊中指定之專案相關聯的值。
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843900"
---
# <a name="cb_setitemdata-message"></a><span data-ttu-id="e2139-104">CB \_ SETITEMDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="e2139-104">CB\_SETITEMDATA message</span></span>

<span data-ttu-id="e2139-105">應用程式會傳送 **CB \_ SETITEMDATA** 訊息，以設定與下拉式方塊中指定之專案相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="e2139-105">An application sends a **CB\_SETITEMDATA** message to set the value associated with the specified item in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2139-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2139-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2139-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2139-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2139-108">指定專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e2139-108">Specifies the item's zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="e2139-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2139-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2139-110">指定要與專案相關聯的新值。</span><span class="sxs-lookup"><span data-stu-id="e2139-110">Specifies the new value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2139-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2139-111">Return value</span></span>

<span data-ttu-id="e2139-112">如果發生錯誤，傳回值會是 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="e2139-112">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2139-113">備註</span><span class="sxs-lookup"><span data-stu-id="e2139-113">Remarks</span></span>

<span data-ttu-id="e2139-114">如果指定的專案在建立時沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md)樣式的主控描繪下拉式方塊中，則此訊息會取代將專案新增至下拉式方塊的 [**cb \_ ADDSTRING**](cb-addstring.md)或 [**cb \_ INSERTSTRING**](cb-insertstring.md)訊息之 *lParam* 參數中的值。</span><span class="sxs-lookup"><span data-stu-id="e2139-114">If the specified item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, this message replaces the value in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message that added the item to the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2139-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2139-115">Requirements</span></span>



| <span data-ttu-id="e2139-116">需求</span><span class="sxs-lookup"><span data-stu-id="e2139-116">Requirement</span></span> | <span data-ttu-id="e2139-117">值</span><span class="sxs-lookup"><span data-stu-id="e2139-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2139-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2139-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e2139-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2139-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2139-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2139-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e2139-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2139-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2139-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e2139-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2139-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e2139-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2139-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2139-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2139-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="e2139-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e2139-126">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="e2139-126">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="e2139-127">**CB \_ GETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="e2139-127">**CB\_GETITEMDATA**</span></span>](cb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="e2139-128">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="e2139-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





