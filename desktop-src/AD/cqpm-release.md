---
title: 'CQPM_RELEASE 訊息 (Cmnquery .h) '
description: 當即將卸載頁面時，傳送至查詢表單延伸頁面的 CQPageProc 回呼函數。
ms.assetid: b935ae8d-a07f-4f0d-b379-5512e96a25a5
ms.tgt_platform: multiple
keywords:
- CQPM_RELEASE 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_RELEASE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4957f02b57f499d80f7802b4fe9bd2639485b8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025038"
---
# <a name="cqpm_release-message"></a><span data-ttu-id="7b558-104">CQPM \_ 發行訊息</span><span class="sxs-lookup"><span data-stu-id="7b558-104">CQPM\_RELEASE message</span></span>

<span data-ttu-id="7b558-105">當即將卸載頁面時，會將 **CQPM \_ 發行** 訊息傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7b558-105">The **CQPM\_RELEASE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is about to be unloaded.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b558-106">參數</span><span class="sxs-lookup"><span data-stu-id="7b558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b558-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b558-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b558-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="7b558-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7b558-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b558-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b558-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="7b558-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b558-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b558-111">Return value</span></span>

<span data-ttu-id="7b558-112">此訊息的傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7b558-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b558-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b558-113">Requirements</span></span>



| <span data-ttu-id="7b558-114">需求</span><span class="sxs-lookup"><span data-stu-id="7b558-114">Requirement</span></span> | <span data-ttu-id="7b558-115">值</span><span class="sxs-lookup"><span data-stu-id="7b558-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b558-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b558-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7b558-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b558-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="7b558-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b558-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7b558-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b558-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="7b558-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7b558-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b558-121"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b558-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b558-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b558-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b558-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="7b558-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





