---
title: 'CB_GETCOUNT 訊息 (Winuser .h) '
description: 取得下拉式方塊清單方塊中的專案數。
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- CB_GETCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686687"
---
# <a name="cb_getcount-message"></a><span data-ttu-id="19697-104">CB \_ GETCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="19697-104">CB\_GETCOUNT message</span></span>

<span data-ttu-id="19697-105">取得下拉式方塊清單方塊中的專案數。</span><span class="sxs-lookup"><span data-stu-id="19697-105">Gets the number of items in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="19697-106">參數</span><span class="sxs-lookup"><span data-stu-id="19697-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19697-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19697-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19697-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="19697-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="19697-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19697-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19697-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="19697-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19697-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="19697-111">Return value</span></span>

<span data-ttu-id="19697-112">傳回值是清單方塊中的專案數。</span><span class="sxs-lookup"><span data-stu-id="19697-112">The return value is the number of items in the list box.</span></span> <span data-ttu-id="19697-113">如果發生錯誤，則為 CB \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="19697-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="19697-114">備註</span><span class="sxs-lookup"><span data-stu-id="19697-114">Remarks</span></span>

<span data-ttu-id="19697-115">索引是以零為基底，因此傳回的計數會大於最後一個專案的索引值。</span><span class="sxs-lookup"><span data-stu-id="19697-115">The index is zero-based, so the returned count is one greater than the index value of the last item.</span></span>

## <a name="requirements"></a><span data-ttu-id="19697-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="19697-116">Requirements</span></span>



| <span data-ttu-id="19697-117">需求</span><span class="sxs-lookup"><span data-stu-id="19697-117">Requirement</span></span> | <span data-ttu-id="19697-118">值</span><span class="sxs-lookup"><span data-stu-id="19697-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19697-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19697-119">Minimum supported client</span></span><br/> | <span data-ttu-id="19697-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19697-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19697-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19697-121">Minimum supported server</span></span><br/> | <span data-ttu-id="19697-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19697-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19697-123">標頭</span><span class="sxs-lookup"><span data-stu-id="19697-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="19697-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="19697-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





