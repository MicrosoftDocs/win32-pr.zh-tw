---
title: 'LB_SETLOCALE 訊息 (Winuser .h) '
description: 設定清單方塊的目前地區設定。 您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有磅 \_ 排序樣式) 的清單方塊，以及 LB ADDSTRING 訊息所加入的文字 \_ 。
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025380"
---
# <a name="lb_setlocale-message"></a><span data-ttu-id="1e7d0-105">LB \_ SETLOCALE 訊息</span><span class="sxs-lookup"><span data-stu-id="1e7d0-105">LB\_SETLOCALE message</span></span>

<span data-ttu-id="1e7d0-106">設定清單方塊的目前地區設定。</span><span class="sxs-lookup"><span data-stu-id="1e7d0-106">Sets the current locale of the list box.</span></span> <span data-ttu-id="1e7d0-107">您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有 [**磅 \_ 排序**](list-box-styles.md) 樣式) 的清單方塊，以及 [**LB \_ ADDSTRING**](lb-addstring.md) 訊息所加入的文字。</span><span class="sxs-lookup"><span data-stu-id="1e7d0-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e7d0-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e7d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e7d0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e7d0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e7d0-110">指定當加入文字時，清單方塊將用來排序的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e7d0-110">Specifies the locale identifier that the list box will use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="1e7d0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e7d0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e7d0-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="1e7d0-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e7d0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e7d0-113">Return value</span></span>

<span data-ttu-id="1e7d0-114">傳回值是先前的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e7d0-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="1e7d0-115">如果 *wParam* 參數指定的地區設定未安裝在系統上，則傳回值為 LB \_ ERR，而且目前的清單方塊地區設定不會變更。</span><span class="sxs-lookup"><span data-stu-id="1e7d0-115">If the *wParam* parameter specifies a locale that is not installed on the system, the return value is LB\_ERR and the current list box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e7d0-116">備註</span><span class="sxs-lookup"><span data-stu-id="1e7d0-116">Remarks</span></span>

<span data-ttu-id="1e7d0-117">使用 [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e7d0-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e7d0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e7d0-118">Requirements</span></span>



| <span data-ttu-id="1e7d0-119">需求</span><span class="sxs-lookup"><span data-stu-id="1e7d0-119">Requirement</span></span> | <span data-ttu-id="1e7d0-120">值</span><span class="sxs-lookup"><span data-stu-id="1e7d0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e7d0-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e7d0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1e7d0-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e7d0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1e7d0-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e7d0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1e7d0-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e7d0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e7d0-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1e7d0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e7d0-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1e7d0-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e7d0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e7d0-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e7d0-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="1e7d0-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e7d0-129">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="1e7d0-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="1e7d0-130">**LB \_ GETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="1e7d0-130">**LB\_GETLOCALE**</span></span>](lb-getlocale.md)
</dt> </dl>

 

