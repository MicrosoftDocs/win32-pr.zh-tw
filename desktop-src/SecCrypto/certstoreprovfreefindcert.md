---
description: 在 CertStoreProvFindCert 的後續呼叫中，未使用 CertStoreProvFindCert 回呼所傳回的憑證，因而加以釋放時呼叫。
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: CertStoreProvFreeFindCert 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985015"
---
# <a name="certstoreprovfreefindcert-callback-function"></a><span data-ttu-id="75be5-103">CertStoreProvFreeFindCert 回呼函式</span><span class="sxs-lookup"><span data-stu-id="75be5-103">CertStoreProvFreeFindCert callback function</span></span>

<span data-ttu-id="75be5-104">**CertStoreProvFreeFindCert** 回呼函式會在 [**CertStoreProvFindCert**](certstoreprovfindcert.md)回呼所傳回的憑證未使用時呼叫，因此會在後續的 **CertStoreProvFindCert** 呼叫中釋放。</span><span class="sxs-lookup"><span data-stu-id="75be5-104">The **CertStoreProvFreeFindCert** callback function is called when the certificate returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCert**.</span></span> <span data-ttu-id="75be5-105">呼叫 CLOSE 回呼之前， [**CertStoreProvFindCert**](certstoreprovfindcert.md) 回呼傳回的所有憑證都必須由提供者使用 **CertStoreProvFindCert** 或 **CertStoreProvFreeFindCert** 來釋放。</span><span class="sxs-lookup"><span data-stu-id="75be5-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback must be released by the provider using **CertStoreProvFindCert** or **CertStoreProvFreeFindCert**.</span></span>

## <a name="syntax"></a><span data-ttu-id="75be5-106">語法</span><span class="sxs-lookup"><span data-stu-id="75be5-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="75be5-107">參數</span><span class="sxs-lookup"><span data-stu-id="75be5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75be5-108">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75be5-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75be5-109">**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="75be5-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="75be5-110">*pCertCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75be5-110">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75be5-111">憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。</span><span class="sxs-lookup"><span data-stu-id="75be5-111">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="75be5-112">*pvStoreProvFindInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75be5-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75be5-113">包含尋找資訊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="75be5-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="75be5-114">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75be5-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75be5-115">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="75be5-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75be5-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="75be5-116">Return value</span></span>

<span data-ttu-id="75be5-117">如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="75be5-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="75be5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="75be5-118">Requirements</span></span>



| <span data-ttu-id="75be5-119">需求</span><span class="sxs-lookup"><span data-stu-id="75be5-119">Requirement</span></span> | <span data-ttu-id="75be5-120">值</span><span class="sxs-lookup"><span data-stu-id="75be5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75be5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75be5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="75be5-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75be5-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="75be5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75be5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="75be5-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75be5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75be5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75be5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75be5-126">**憑證 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="75be5-126">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="75be5-127">**CertStoreProvFindCert**</span><span class="sxs-lookup"><span data-stu-id="75be5-127">**CertStoreProvFindCert**</span></span>](certstoreprovfindcert.md)
</dt> </dl>

 

 
