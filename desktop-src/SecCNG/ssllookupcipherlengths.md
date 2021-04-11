---
description: 傳回 NCRYPT \_ SSL \_ 密碼 \_ 長度結構，其中包含輸入通訊協定、加密套件和金鑰類型的標頭和結尾長度。
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: 'SslLookupCipherLengths 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943877"
---
# <a name="ssllookupcipherlengths-function"></a><span data-ttu-id="cff07-103">SslLookupCipherLengths 函式</span><span class="sxs-lookup"><span data-stu-id="cff07-103">SslLookupCipherLengths function</span></span>

<span data-ttu-id="cff07-104">**SslLookupCipherLengths** 函式會傳回 [**NCRYPT \_ SSL \_ 加密 \_ 長度**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**)結構，其中包含輸入通訊協定、加密套件和金鑰類型的標頭和結尾長度。</span><span class="sxs-lookup"><span data-stu-id="cff07-104">The **SslLookupCipherLengths** function returns an [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff07-105">語法</span><span class="sxs-lookup"><span data-stu-id="cff07-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cff07-106">參數</span><span class="sxs-lookup"><span data-stu-id="cff07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cff07-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cff07-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff07-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cff07-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="cff07-109">*dwProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cff07-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff07-110">其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="cff07-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="cff07-111">*dwCipherSuite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cff07-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff07-112">其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="cff07-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="cff07-113">*dwKeyType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cff07-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff07-114">其中一個 [**CNG SSL 提供者金鑰類型識別碼**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="cff07-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="cff07-115">對於非 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly) 編譯 (ECC) 的金鑰類型，請將此參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="cff07-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cff07-116">*pCipherLengths* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cff07-116">*pCipherLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cff07-117">接收 [**NCRYPT \_ SSL \_ 密碼 \_ 長度**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) 結構之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="cff07-117">A pointer to a buffer to receive the [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cff07-118">*cbCipherLengths* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cff07-118">*cbCipherLengths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff07-119">*PCipherLengths* 參數所指向之緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cff07-119">The length, in bytes, of the buffer pointed to by the *pCipherLengths* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cff07-120">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cff07-120">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cff07-121">此參數會保留供日後使用，且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="cff07-121">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cff07-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="cff07-122">Return value</span></span>

<span data-ttu-id="cff07-123">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="cff07-123">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="cff07-124">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="cff07-124">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="cff07-125">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="cff07-125">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="cff07-126">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="cff07-126">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="cff07-127">Description</span><span class="sxs-lookup"><span data-stu-id="cff07-127">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cff07-128">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="cff07-128"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="cff07-129">*HSslProvider* 參數包含不正確指標。</span><span class="sxs-lookup"><span data-stu-id="cff07-129">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="cff07-130">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="cff07-130"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="cff07-131">*PCipherLengths* 參數設定為 **Null** ，或 *cbCipherLengths* 所指定的緩衝區長度太短。</span><span class="sxs-lookup"><span data-stu-id="cff07-131">The *pCipherLengths* parameter is set to **NULL** or the buffer length specified by the *cbCipherLengths* is too short.</span></span><br/> |
| <dl> <span data-ttu-id="cff07-132">不 <dt>**超過 \_錯誤的 \_ 旗標**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="cff07-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="cff07-133">*DwFlags* 參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="cff07-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="cff07-134">備註</span><span class="sxs-lookup"><span data-stu-id="cff07-134">Remarks</span></span>

<span data-ttu-id="cff07-135">**SslLookupCipherLengths** 函式是針對 [*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly)（ (TLS) 1.1 或更新版本的交談）進行呼叫，以查詢要求的通訊協定、加密套件和金鑰類型的標頭和結尾長度。</span><span class="sxs-lookup"><span data-stu-id="cff07-135">The **SslLookupCipherLengths** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.1 or later conversations to query the header and trailer lengths for the requested protocol, cipher suite, and key type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cff07-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="cff07-136">Requirements</span></span>



| <span data-ttu-id="cff07-137">需求</span><span class="sxs-lookup"><span data-stu-id="cff07-137">Requirement</span></span> | <span data-ttu-id="cff07-138">值</span><span class="sxs-lookup"><span data-stu-id="cff07-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cff07-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cff07-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cff07-140">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cff07-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cff07-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cff07-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cff07-142">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cff07-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cff07-143">標頭</span><span class="sxs-lookup"><span data-stu-id="cff07-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="cff07-144"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="cff07-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="cff07-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cff07-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cff07-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cff07-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

