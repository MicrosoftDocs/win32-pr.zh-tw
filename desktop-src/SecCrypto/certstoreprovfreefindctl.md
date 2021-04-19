---
description: 在 CertStoreProvFindCTL 的後續呼叫中，未使用 CertStoreProvFindCTL 回呼所傳回的憑證，因而加以釋放時呼叫。
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: CertStoreProvFreeFindCTL 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989358"
---
# <a name="certstoreprovfreefindctl-callback-function"></a><span data-ttu-id="40b4a-103">CertStoreProvFreeFindCTL 回呼函式</span><span class="sxs-lookup"><span data-stu-id="40b4a-103">CertStoreProvFreeFindCTL callback function</span></span>

<span data-ttu-id="40b4a-104">**CertStoreProvFreeFindCTL** 回呼函式會在 [**CertStoreProvFindCTL**](certstoreprovfindctl.md)回呼所傳回的憑證未使用時呼叫，因此會在後續的 **CertStoreProvFindCTL** 呼叫中釋放。</span><span class="sxs-lookup"><span data-stu-id="40b4a-104">The **CertStoreProvFreeFindCTL** callback function is called when the certificate returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCTL**.</span></span> <span data-ttu-id="40b4a-105">呼叫 CLOSE 回呼之前， [**CertStoreProvFindCTL**](certstoreprovfindctl.md) 回呼傳回的所有憑證都必須由提供者使用 **CertStoreProvFindCTL** 或 **CertStoreProvFreeFindCTL** 來釋放。</span><span class="sxs-lookup"><span data-stu-id="40b4a-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback must be released by the provider using **CertStoreProvFindCTL** or **CertStoreProvFreeFindCTL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b4a-106">語法</span><span class="sxs-lookup"><span data-stu-id="40b4a-106">Syntax</span></span>


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="40b4a-107">參數</span><span class="sxs-lookup"><span data-stu-id="40b4a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40b4a-108">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40b4a-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b4a-109">**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="40b4a-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b4a-110">*pCtlCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40b4a-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b4a-111">[**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="40b4a-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="40b4a-112">*pvStoreProvFindInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40b4a-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b4a-113">包含尋找資訊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="40b4a-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="40b4a-114">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40b4a-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b4a-115">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="40b4a-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40b4a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="40b4a-116">Return value</span></span>

<span data-ttu-id="40b4a-117">如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="40b4a-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="40b4a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="40b4a-118">Requirements</span></span>



| <span data-ttu-id="40b4a-119">需求</span><span class="sxs-lookup"><span data-stu-id="40b4a-119">Requirement</span></span> | <span data-ttu-id="40b4a-120">值</span><span class="sxs-lookup"><span data-stu-id="40b4a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="40b4a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40b4a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="40b4a-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40b4a-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="40b4a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40b4a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="40b4a-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40b4a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40b4a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40b4a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b4a-126">**CertStoreProvFindCTL**</span><span class="sxs-lookup"><span data-stu-id="40b4a-126">**CertStoreProvFindCTL**</span></span>](certstoreprovfindctl.md)
</dt> <dt>

[<span data-ttu-id="40b4a-127">**CTL \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="40b4a-127">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
