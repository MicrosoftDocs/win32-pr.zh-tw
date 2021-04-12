---
title: 'CQPM_PERSIST 訊息 (Cmnquery .h) '
description: 傳送至查詢表單延伸頁面的 CQPageProc 回呼函式，以允許頁面讀取或寫入持續性記憶體中的查詢資料。
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- CQPM_PERSIST 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025039"
---
# <a name="cqpm_persist-message"></a><span data-ttu-id="9f7c4-104">CQPM \_ 保存訊息</span><span class="sxs-lookup"><span data-stu-id="9f7c4-104">CQPM\_PERSIST message</span></span>

<span data-ttu-id="9f7c4-105">**CQPM \_ 保存** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)回呼函式，以允許頁面讀取或寫入持續性記憶體中的查詢資料。</span><span class="sxs-lookup"><span data-stu-id="9f7c4-105">The **CQPM\_PERSIST** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page to read or write query data from persistent memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f7c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f7c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f7c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f7c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f7c4-108">包含非零值，可讀取查詢資料或零來寫入查詢資料。</span><span class="sxs-lookup"><span data-stu-id="9f7c4-108">Contains nonzero to read the query data or zero to write the query data.</span></span>

</dd> <dt>

<span data-ttu-id="9f7c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f7c4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f7c4-110">應從中讀取或寫入查詢資料之 [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9f7c4-110">Pointer to an [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) interface that the query data should be read from or written to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f7c4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f7c4-111">Return value</span></span>

<span data-ttu-id="9f7c4-112">如果 **成功 \_ ，則傳回** ，否則會傳回標準的 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9f7c4-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f7c4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f7c4-113">Requirements</span></span>



| <span data-ttu-id="9f7c4-114">需求</span><span class="sxs-lookup"><span data-stu-id="9f7c4-114">Requirement</span></span> | <span data-ttu-id="9f7c4-115">值</span><span class="sxs-lookup"><span data-stu-id="9f7c4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f7c4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f7c4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f7c4-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f7c4-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="9f7c4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f7c4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f7c4-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f7c4-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="9f7c4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9f7c4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f7c4-121"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f7c4-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f7c4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f7c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f7c4-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="9f7c4-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="9f7c4-124">**IPersistQuery**</span><span class="sxs-lookup"><span data-stu-id="9f7c4-124">**IPersistQuery**</span></span>](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

