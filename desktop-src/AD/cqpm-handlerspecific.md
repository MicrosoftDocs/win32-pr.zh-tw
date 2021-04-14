---
title: 'CQPM_HANDLERSPECIFIC 訊息 (Cmnquery .h) '
description: 用於查詢處理常式私用之訊息的基底值。
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- CQPM_HANDLERSPECIFIC 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464553"
---
# <a name="cqpm_handlerspecific-message"></a><span data-ttu-id="994ba-104">CQPM \_ HANDLERSPECIFIC 訊息</span><span class="sxs-lookup"><span data-stu-id="994ba-104">CQPM\_HANDLERSPECIFIC message</span></span>

<span data-ttu-id="994ba-105">**CQPM \_ HANDLERSPECIFIC** 訊息是用於查詢處理常式私用之訊息的基底值。</span><span class="sxs-lookup"><span data-stu-id="994ba-105">The **CQPM\_HANDLERSPECIFIC** message is the base value used for messages that are private to the query handler.</span></span> <span data-ttu-id="994ba-106">查詢處理常式應該將此值新增至私用訊息，以確保不會發生訊息衝突。</span><span class="sxs-lookup"><span data-stu-id="994ba-106">The query handler should add this value to private messages to ensure that message collisions do not occur.</span></span>

## <a name="parameters"></a><span data-ttu-id="994ba-107">參數</span><span class="sxs-lookup"><span data-stu-id="994ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="994ba-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="994ba-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="994ba-109">包含其他訊息資料。</span><span class="sxs-lookup"><span data-stu-id="994ba-109">Contains additional message data.</span></span> <span data-ttu-id="994ba-110">此參數的內容是由查詢處理常式所定義。</span><span class="sxs-lookup"><span data-stu-id="994ba-110">The content of this parameter is defined by the query handler.</span></span>

</dd> <dt>

<span data-ttu-id="994ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="994ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="994ba-112">包含其他訊息資料。</span><span class="sxs-lookup"><span data-stu-id="994ba-112">Contains additional message data.</span></span> <span data-ttu-id="994ba-113">此參數的內容是由查詢處理常式所定義。</span><span class="sxs-lookup"><span data-stu-id="994ba-113">The content of this parameter is defined by the query handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="994ba-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="994ba-114">Return value</span></span>

<span data-ttu-id="994ba-115">傳回值的意義是由查詢處理常式所定義。</span><span class="sxs-lookup"><span data-stu-id="994ba-115">The meaning of the return value is defined by the query handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="994ba-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="994ba-116">Requirements</span></span>



| <span data-ttu-id="994ba-117">需求</span><span class="sxs-lookup"><span data-stu-id="994ba-117">Requirement</span></span> | <span data-ttu-id="994ba-118">值</span><span class="sxs-lookup"><span data-stu-id="994ba-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="994ba-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="994ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="994ba-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="994ba-120">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="994ba-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="994ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="994ba-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="994ba-122">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="994ba-123">標頭</span><span class="sxs-lookup"><span data-stu-id="994ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="994ba-124"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="994ba-124"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="994ba-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="994ba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="994ba-126">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="994ba-126">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





