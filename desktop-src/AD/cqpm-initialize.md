---
title: 'CQPM_INITIALIZE 訊息 (Cmnquery .h) '
description: 當頁面新增至表單時，傳送至查詢表單延伸頁面的 CQPageProc 回呼函式。
ms.assetid: 29cb39d5-9bc4-472e-8a2f-dc6cd505144a
ms.tgt_platform: multiple
keywords:
- CQPM_INITIALIZE 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_INITIALIZE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e95c7087a9cd2d40387c8d7dd07aa93c8f697fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025040"
---
# <a name="cqpm_initialize-message"></a><span data-ttu-id="51a0a-104">CQPM \_ INITIALIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="51a0a-104">CQPM\_INITIALIZE message</span></span>

<span data-ttu-id="51a0a-105">當頁面新增至表單時， **CQPM \_ INITIALIZE** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="51a0a-105">The **CQPM\_INITIALIZE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is added to a form.</span></span>

## <a name="parameters"></a><span data-ttu-id="51a0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="51a0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51a0a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51a0a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51a0a-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="51a0a-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="51a0a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51a0a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51a0a-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="51a0a-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51a0a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="51a0a-111">Return value</span></span>

<span data-ttu-id="51a0a-112">此訊息的傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="51a0a-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="51a0a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="51a0a-113">Requirements</span></span>



| <span data-ttu-id="51a0a-114">需求</span><span class="sxs-lookup"><span data-stu-id="51a0a-114">Requirement</span></span> | <span data-ttu-id="51a0a-115">值</span><span class="sxs-lookup"><span data-stu-id="51a0a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51a0a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51a0a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="51a0a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51a0a-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="51a0a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51a0a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="51a0a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51a0a-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="51a0a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="51a0a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="51a0a-121"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="51a0a-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51a0a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51a0a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51a0a-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="51a0a-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





