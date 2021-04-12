---
title: 'CQPM_ENABLE 訊息 (Cmnquery .h) '
description: 傳送至查詢表單延伸頁面的 CQPageProc 回呼函數，以啟用或停用頁面。
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- CQPM_ENABLE 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024735"
---
# <a name="cqpm_enable-message"></a><span data-ttu-id="1f78c-104">CQPM \_ 啟用訊息</span><span class="sxs-lookup"><span data-stu-id="1f78c-104">CQPM\_ENABLE message</span></span>

<span data-ttu-id="1f78c-105">**CQPM \_ enable** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)回呼函數，以啟用或停用頁面。</span><span class="sxs-lookup"><span data-stu-id="1f78c-105">The **CQPM\_ENABLE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to enable or disable the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f78c-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f78c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f78c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f78c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f78c-108">包含零，可停用頁面或非零值以啟用頁面。</span><span class="sxs-lookup"><span data-stu-id="1f78c-108">Contains zero to disable the page or nonzero to enable the page.</span></span>

</dd> <dt>

<span data-ttu-id="1f78c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f78c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f78c-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="1f78c-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f78c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f78c-111">Return value</span></span>

<span data-ttu-id="1f78c-112">此訊息的傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="1f78c-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f78c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f78c-113">Requirements</span></span>



| <span data-ttu-id="1f78c-114">需求</span><span class="sxs-lookup"><span data-stu-id="1f78c-114">Requirement</span></span> | <span data-ttu-id="1f78c-115">值</span><span class="sxs-lookup"><span data-stu-id="1f78c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f78c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f78c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1f78c-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f78c-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="1f78c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f78c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1f78c-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f78c-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="1f78c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1f78c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f78c-121"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f78c-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f78c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f78c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f78c-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="1f78c-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





