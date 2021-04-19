---
description: 安全通訊端層通訊協定 (SSL) 通訊協定提供者匯入金鑰。
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: 'SslImportKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977273"
---
# <a name="sslimportkey-function"></a><span data-ttu-id="e170b-103">SslImportKey 函式</span><span class="sxs-lookup"><span data-stu-id="e170b-103">SslImportKey function</span></span>

<span data-ttu-id="e170b-104">**SslImportKey** 函式會 (SSL) 通訊協定提供者，將金鑰匯入 [*安全通訊端層的通訊協定*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="e170b-104">The **SslImportKey** function imports a key into the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="e170b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e170b-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e170b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e170b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e170b-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e170b-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e170b-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e170b-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="e170b-109">*phKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e170b-109">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e170b-110">要接收匯入金鑰之 [*密碼編譯金鑰*](/windows/desktop/SecGloss/c-gly) 的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="e170b-110">A pointer to the handle of the [*cryptographic key*](/windows/desktop/SecGloss/c-gly) to receive the imported key.</span></span>

</dd> <dt>

<span data-ttu-id="e170b-111">*pszBlobType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e170b-111">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e170b-112">以 null 終止的 Unicode 字串，其中包含指定 *pbInput* 緩衝區中所包含之 [*BLOB*](/windows/desktop/SecGloss/b-gly)類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e170b-112">A null-terminated Unicode string that contains an identifier that specifies the type of [*BLOB*](/windows/desktop/SecGloss/b-gly) that is contained in the *pbInput* buffer.</span></span> <span data-ttu-id="e170b-113">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e170b-113">This can be one of the following values.</span></span>



| <span data-ttu-id="e170b-114">值</span><span class="sxs-lookup"><span data-stu-id="e170b-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="e170b-115">意義</span><span class="sxs-lookup"><span data-stu-id="e170b-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="e170b-116"><dt>**BCRYPT \_ DH \_ 公用 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-116"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="e170b-117">匯出 Diffie-Hellman 的 [*公開金鑰*](/windows/desktop/SecGloss/p-gly)。</span><span class="sxs-lookup"><span data-stu-id="e170b-117">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="e170b-118">*PbOutput* 緩衝區會立即接收 [**BCRYPT \_ DH \_ 金鑰 \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob)結構，後面接著金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="e170b-118">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="e170b-119"><dt>**BCRYPT \_ ECCPUBLIC \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-119"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="e170b-120"> (ECC) [*公開金鑰*](/windows/desktop/SecGloss/p-gly)匯出 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly)編譯。</span><span class="sxs-lookup"><span data-stu-id="e170b-120">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="e170b-121">*PbOutput* 緩衝區會立即接收 [**BCRYPT \_ ECCKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob)結構，後面接著金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="e170b-121">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="e170b-122"><dt>**BCRYPT 不 \_ 透明的 \_ 金鑰 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-122"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="e170b-123">使用 (CSP) 的單一 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly)專用的格式來匯出 [*對稱金鑰*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="e170b-123">Export a [*symmetric key*](/windows/desktop/SecGloss/s-gly) in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="e170b-124">不透明的 Blob 無法轉移，而且必須使用產生 BLOB 的相同 CSP 來匯入。</span><span class="sxs-lookup"><span data-stu-id="e170b-124">Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="e170b-125"><dt>**BCRYPT \_ RSAPUBLIC \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-125"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="e170b-126">匯出 [*RSA*](/windows/desktop/SecGloss/r-gly) 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="e170b-126">Export an [*RSA*](/windows/desktop/SecGloss/r-gly) public key.</span></span> <span data-ttu-id="e170b-127">*PbOutput* 緩衝區會立即接收 [**BCRYPT \_ RSAKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob)結構，後面接著金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="e170b-127">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="e170b-128">*pbKeyBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e170b-128">*pbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e170b-129">包含 [*金鑰 BLOB*](/windows/desktop/SecGloss/k-gly)的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="e170b-129">A pointer to the buffer that contains the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span>

</dd> <dt>

<span data-ttu-id="e170b-130">*cbKeyBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e170b-130">*cbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e170b-131">*PbKeyBlob* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e170b-131">The size, in bytes, of the *pbKeyBlob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e170b-132">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e170b-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e170b-133">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="e170b-133">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e170b-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="e170b-134">Return value</span></span>

<span data-ttu-id="e170b-135">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e170b-135">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="e170b-136">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="e170b-136">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="e170b-137">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="e170b-137">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="e170b-138">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e170b-138">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="e170b-139">Description</span><span class="sxs-lookup"><span data-stu-id="e170b-139">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e170b-140">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-140"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="e170b-141">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e170b-141">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="e170b-142">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-142"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="e170b-143">*HSslProvider* 控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e170b-143">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="e170b-144">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-144"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="e170b-145">*PhKey* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e170b-145">The *phKey* parameter is **NULL**.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="e170b-146">備註</span><span class="sxs-lookup"><span data-stu-id="e170b-146">Remarks</span></span>

<span data-ttu-id="e170b-147">您可以使用 **SslImportKey** 函式，在將工作階段金鑰從某個進程傳送到另一個進程的過程中，匯入工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="e170b-147">You can use the **SslImportKey** function to import session keys as a part of the process of transferring session keys from one process to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="e170b-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="e170b-148">Requirements</span></span>



| <span data-ttu-id="e170b-149">需求</span><span class="sxs-lookup"><span data-stu-id="e170b-149">Requirement</span></span> | <span data-ttu-id="e170b-150">值</span><span class="sxs-lookup"><span data-stu-id="e170b-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e170b-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e170b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e170b-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e170b-152">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e170b-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e170b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e170b-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e170b-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e170b-155">標頭</span><span class="sxs-lookup"><span data-stu-id="e170b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="e170b-156"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-156"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e170b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e170b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e170b-158"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e170b-158"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

