---
description: 在 CertStoreProvFindCRL 的後續呼叫中，未使用 CertStoreProvFindCRL 回呼所傳回的憑證，因而加以釋放時呼叫。
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: CertStoreProvFreeFindCRL 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851052"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a><span data-ttu-id="5b399-103">CertStoreProvFreeFindCRL 回呼函式</span><span class="sxs-lookup"><span data-stu-id="5b399-103">CertStoreProvFreeFindCRL callback function</span></span>

<span data-ttu-id="5b399-104">**CertStoreProvFreeFindCRL** 回呼函式會在 [**CertStoreProvFindCRL**](certstoreprovfindcrl.md)回呼所傳回的憑證未使用時呼叫，因此會在後續的 **CertStoreProvFindCRL** 呼叫中釋放。</span><span class="sxs-lookup"><span data-stu-id="5b399-104">The **CertStoreProvFreeFindCRL** callback function is called when the certificate returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCRL**.</span></span> <span data-ttu-id="5b399-105">呼叫 CLOSE 回呼之前， [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) 回呼傳回的所有憑證都必須由提供者使用 **CertStoreProvFindCRL** 或 **CertStoreProvFreeFindCRL** 來釋放。</span><span class="sxs-lookup"><span data-stu-id="5b399-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback must be released by the provider using **CertStoreProvFindCRL** or **CertStoreProvFreeFindCRL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b399-106">語法</span><span class="sxs-lookup"><span data-stu-id="5b399-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5b399-107">參數</span><span class="sxs-lookup"><span data-stu-id="5b399-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b399-108">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b399-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b399-109">**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5b399-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b399-110">*pCrlCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b399-110">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b399-111">[**CRL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。</span><span class="sxs-lookup"><span data-stu-id="5b399-111">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="5b399-112">*pvStoreProvFindInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b399-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b399-113">包含尋找資訊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="5b399-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="5b399-114">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b399-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b399-115">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="5b399-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b399-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b399-116">Return value</span></span>

<span data-ttu-id="5b399-117">如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5b399-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b399-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b399-118">Requirements</span></span>



| <span data-ttu-id="5b399-119">需求</span><span class="sxs-lookup"><span data-stu-id="5b399-119">Requirement</span></span> | <span data-ttu-id="5b399-120">值</span><span class="sxs-lookup"><span data-stu-id="5b399-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5b399-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b399-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5b399-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b399-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5b399-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b399-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5b399-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b399-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b399-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b399-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b399-126">**CertStoreProvFindCRL**</span><span class="sxs-lookup"><span data-stu-id="5b399-126">**CertStoreProvFindCRL**</span></span>](certstoreprovfindcrl.md)
</dt> <dt>

[<span data-ttu-id="5b399-127">**CRL \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="5b399-127">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
