---
title: 'CQPM_GETPARAMETERS 訊息 (Cmnquery .h) '
description: 傳送至查詢表單延伸頁面的 CQPageProc 回呼函數，以抓取頁面所執行之查詢的相關資料。
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- CQPM_GETPARAMETERS 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843212"
---
# <a name="cqpm_getparameters-message"></a><span data-ttu-id="da294-104">CQPM \_ GETPARAMETERS 訊息</span><span class="sxs-lookup"><span data-stu-id="da294-104">CQPM\_GETPARAMETERS message</span></span>

<span data-ttu-id="da294-105">**CQPM \_ GETPARAMETERS** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)回呼函數，以抓取頁面所執行之查詢的相關資料。</span><span class="sxs-lookup"><span data-stu-id="da294-105">The **CQPM\_GETPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to retrieve data about the query performed by the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="da294-106">參數</span><span class="sxs-lookup"><span data-stu-id="da294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da294-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da294-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da294-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="da294-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="da294-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da294-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da294-110">[**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)值的指標，此值會接收頁面所執行之查詢的相關資料。</span><span class="sxs-lookup"><span data-stu-id="da294-110">Pointer to a [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) value that receives data about the query performed by the page.</span></span> <span data-ttu-id="da294-111">如果這個參數是 **Null**，則 **DSQUERYPARAMS** 結構必須由擴充功能使用 [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) 函式來配置。</span><span class="sxs-lookup"><span data-stu-id="da294-111">If this parameter is **NULL**, the **DSQUERYPARAMS** structure must be allocated by the extension using the [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da294-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="da294-112">Return value</span></span>

<span data-ttu-id="da294-113">如果 **成功 \_ ，則傳回** ，否則會傳回標準的 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da294-113">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="da294-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="da294-114">Requirements</span></span>



| <span data-ttu-id="da294-115">需求</span><span class="sxs-lookup"><span data-stu-id="da294-115">Requirement</span></span> | <span data-ttu-id="da294-116">值</span><span class="sxs-lookup"><span data-stu-id="da294-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da294-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da294-117">Minimum supported client</span></span><br/> | <span data-ttu-id="da294-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da294-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="da294-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da294-119">Minimum supported server</span></span><br/> | <span data-ttu-id="da294-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da294-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="da294-121">標頭</span><span class="sxs-lookup"><span data-stu-id="da294-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="da294-122"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="da294-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da294-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da294-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da294-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="da294-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="da294-125">**DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="da294-125">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[<span data-ttu-id="da294-126">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="da294-126">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

