---
title: 'CQPM_CLEARFORM 訊息 (Cmnquery .h) '
description: 當頁面內容應該重設為預設值時，傳送至擴充功能頁面查詢的 CQPageProc 回呼函式。
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- CQPM_CLEARFORM 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94af3a31a29da4ce5740c4e326bbf1a8961f9f82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933995"
---
# <a name="cqpm_clearform-message"></a><span data-ttu-id="a9b98-104">CQPM \_ CLEARFORM 訊息</span><span class="sxs-lookup"><span data-stu-id="a9b98-104">CQPM\_CLEARFORM message</span></span>

<span data-ttu-id="a9b98-105">當頁面內容應該重設為預設值時，會將 **CQPM \_ CLEARFORM** 訊息傳送至擴充功能頁面的查詢 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="a9b98-105">The **CQPM\_CLEARFORM** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query for extension page when the contents of the page should be reset to the default values.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9b98-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9b98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9b98-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9b98-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b98-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="a9b98-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b98-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9b98-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b98-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="a9b98-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9b98-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9b98-111">Return value</span></span>

<span data-ttu-id="a9b98-112">如果 **成功 \_ ，則傳回** ，否則會傳回標準的 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a9b98-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b98-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9b98-113">Requirements</span></span>



| <span data-ttu-id="a9b98-114">需求</span><span class="sxs-lookup"><span data-stu-id="a9b98-114">Requirement</span></span> | <span data-ttu-id="a9b98-115">值</span><span class="sxs-lookup"><span data-stu-id="a9b98-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b98-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9b98-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b98-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9b98-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="a9b98-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9b98-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b98-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9b98-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="a9b98-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a9b98-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b98-121"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9b98-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9b98-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9b98-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b98-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="a9b98-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





