---
description: 列舉或尋找符合指定準則之外部存放區中的第一個或下一個憑證。
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: CertStoreProvFindCert 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319807"
---
# <a name="certstoreprovfindcert-callback-function"></a><span data-ttu-id="f5716-103">CertStoreProvFindCert 回呼函式</span><span class="sxs-lookup"><span data-stu-id="f5716-103">CertStoreProvFindCert callback function</span></span>

<span data-ttu-id="f5716-104">**CertStoreProvFindCert** 回呼函式會在 [*外部存放區*](../secgloss/e-gly.md)中列舉或尋找符合指定準則的第一個或下一個憑證。</span><span class="sxs-lookup"><span data-stu-id="f5716-104">The **CertStoreProvFindCert** callback function enumerates or finds the first or next certificate in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5716-105">語法</span><span class="sxs-lookup"><span data-stu-id="f5716-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a><span data-ttu-id="f5716-106">參數</span><span class="sxs-lookup"><span data-stu-id="f5716-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5716-107">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5716-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5716-108">**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f5716-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5716-109">*pFindInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5716-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5716-110">[**證書 \_ 存儲 \_ >prov \_ 尋找 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)結構的指標，其中包含傳遞至 [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)函數的所有參數。</span><span class="sxs-lookup"><span data-stu-id="f5716-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="f5716-111">*pPrevCertCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5716-111">*pPrevCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5716-112">找到之憑證的 [**憑證 \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 指標。</span><span class="sxs-lookup"><span data-stu-id="f5716-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) of the certificate found.</span></span> <span data-ttu-id="f5716-113">第一次呼叫函式時，此參數應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f5716-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="f5716-114">在後續的呼叫中，它應該設定為最後一次呼叫時，在 *ppProvCertCoNtext* 參數中傳回的指標。</span><span class="sxs-lookup"><span data-stu-id="f5716-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCertContext* parameter on the last call.</span></span> <span data-ttu-id="f5716-115">在這個參數中傳遞的非 **Null** 指標是由回呼函數釋放。</span><span class="sxs-lookup"><span data-stu-id="f5716-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="f5716-116">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5716-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5716-117">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="f5716-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="f5716-118">*ppvStoreProvFindInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f5716-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5716-119">指向緩衝區指標的指標，以傳回存放區提供者資訊。</span><span class="sxs-lookup"><span data-stu-id="f5716-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="f5716-120">（選擇性）回呼可以傳回這個參數中內部尋找資訊的指標。</span><span class="sxs-lookup"><span data-stu-id="f5716-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="f5716-121">在第一次呼叫之後，這個參數會設定為先前呼叫函數所傳回的指標。</span><span class="sxs-lookup"><span data-stu-id="f5716-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="f5716-122">*ppProvCertCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f5716-122">*ppProvCertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5716-123">在成功尋找時，會在此參數中傳回找到之憑證的指標。</span><span class="sxs-lookup"><span data-stu-id="f5716-123">On a successful find, a pointer to the certificate found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5716-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5716-124">Return value</span></span>

<span data-ttu-id="f5716-125">如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f5716-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5716-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5716-126">Requirements</span></span>



| <span data-ttu-id="f5716-127">需求</span><span class="sxs-lookup"><span data-stu-id="f5716-127">Requirement</span></span> | <span data-ttu-id="f5716-128">值</span><span class="sxs-lookup"><span data-stu-id="f5716-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5716-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5716-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f5716-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5716-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f5716-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5716-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f5716-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5716-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5716-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5716-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5716-134">**憑證 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="f5716-134">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="f5716-135">**證書 \_ 存儲 \_ >PROV \_ 尋找 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f5716-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="f5716-136">**CertFindCertificateInStore**</span><span class="sxs-lookup"><span data-stu-id="f5716-136">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
