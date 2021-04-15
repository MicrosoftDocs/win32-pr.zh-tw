---
title: 'CQPM_SETDEFAULTPARAMETERS 訊息 (Cmnquery .h) '
description: 傳送至查詢表單延伸頁面的 CQPageProc 回呼函數，以設定頁面的替代預設參數。
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- CQPM_SETDEFAULTPARAMETERS 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465157"
---
# <a name="cqpm_setdefaultparameters-message"></a><span data-ttu-id="d30ac-104">CQPM \_ SETDEFAULTPARAMETERS 訊息</span><span class="sxs-lookup"><span data-stu-id="d30ac-104">CQPM\_SETDEFAULTPARAMETERS message</span></span>

<span data-ttu-id="d30ac-105">**CQPM \_ SETDEFAULTPARAMETERS** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)回呼函數，以設定頁面的替代預設參數。</span><span class="sxs-lookup"><span data-stu-id="d30ac-105">The **CQPM\_SETDEFAULTPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to set alternate default parameters for the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="d30ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="d30ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d30ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d30ac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d30ac-108">如果頁面為預設頁面，則包含非零，否則為零。</span><span class="sxs-lookup"><span data-stu-id="d30ac-108">Contains nonzero if the page is the default page or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="d30ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d30ac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d30ac-110">[**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)結構的指標，其中包含 [目錄服務查詢] 對話方塊的相關資料。</span><span class="sxs-lookup"><span data-stu-id="d30ac-110">Pointer to an [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) structure that contains data about the directory service query dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d30ac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d30ac-111">Return value</span></span>

<span data-ttu-id="d30ac-112">此訊息的傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="d30ac-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d30ac-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d30ac-113">Requirements</span></span>



| <span data-ttu-id="d30ac-114">需求</span><span class="sxs-lookup"><span data-stu-id="d30ac-114">Requirement</span></span> | <span data-ttu-id="d30ac-115">值</span><span class="sxs-lookup"><span data-stu-id="d30ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d30ac-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d30ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d30ac-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d30ac-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="d30ac-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d30ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d30ac-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d30ac-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="d30ac-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d30ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d30ac-121"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="d30ac-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d30ac-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d30ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d30ac-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="d30ac-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="d30ac-124">**OPENQUERYWINDOW**</span><span class="sxs-lookup"><span data-stu-id="d30ac-124">**OPENQUERYWINDOW**</span></span>](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





