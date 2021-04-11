---
description: 將安全通訊端層的通訊協定 (SSL) 工作階段金鑰或公開暫時金鑰傳回序列化 BLOB。
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: 'SslExportKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943924"
---
# <a name="sslexportkey-function"></a><span data-ttu-id="d24dc-103">SslExportKey 函式</span><span class="sxs-lookup"><span data-stu-id="d24dc-103">SslExportKey function</span></span>

<span data-ttu-id="d24dc-104">**SslExportKey** 函式會將 [*安全通訊端層的通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) [*工作階段金鑰*](/windows/desktop/SecGloss/s-gly)或公開暫時金鑰傳回序列化 [*BLOB*](/windows/desktop/SecGloss/b-gly)。</span><span class="sxs-lookup"><span data-stu-id="d24dc-104">The **SslExportKey** function returns an [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) [*session key*](/windows/desktop/SecGloss/s-gly) or public ephemeral key into a serialized [*BLOB*](/windows/desktop/SecGloss/b-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="d24dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="d24dc-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d24dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="d24dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d24dc-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24dc-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d24dc-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="d24dc-109">*hKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-109">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24dc-110">要匯出之索引鍵的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d24dc-110">The handle of the key to export.</span></span>

<span data-ttu-id="d24dc-111">當您未指定金鑰時，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d24dc-111">When you are not specifying a key, set this parameter to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="d24dc-112">*HKey* 控制碼是藉由呼叫 [**SslOpenPrivateKey**](sslopenprivatekey.md)函數來取得的。</span><span class="sxs-lookup"><span data-stu-id="d24dc-112">A *hKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="d24dc-113">不支援從 [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) 函數取得的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d24dc-113">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="d24dc-114">*pszBlobType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-114">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24dc-115">以 null 終止的 Unicode 字串，其中包含指定要匯出的 BLOB 類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d24dc-115">A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export.</span></span> <span data-ttu-id="d24dc-116">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d24dc-116">This can be one of the following values.</span></span>



| <span data-ttu-id="d24dc-117">值</span><span class="sxs-lookup"><span data-stu-id="d24dc-117">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="d24dc-118">意義</span><span class="sxs-lookup"><span data-stu-id="d24dc-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="d24dc-119"><dt>**BCRYPT \_ DH \_ 公用 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="d24dc-119"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="d24dc-120">匯出 Diffie-Hellman 的 [*公開金鑰*](/windows/desktop/SecGloss/p-gly)。</span><span class="sxs-lookup"><span data-stu-id="d24dc-120">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="d24dc-121">*PbOutput* 緩衝區會立即接收 [**BCRYPT \_ DH \_ 金鑰 \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob)結構，後面接著金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="d24dc-121">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="d24dc-122"><dt>**BCRYPT \_ ECCPUBLIC \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="d24dc-122"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="d24dc-123"> (ECC) 公開金鑰匯出 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly) 編譯。</span><span class="sxs-lookup"><span data-stu-id="d24dc-123">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) public key.</span></span> <span data-ttu-id="d24dc-124">*PbOutput* 緩衝區會立即接收 [**BCRYPT \_ ECCKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob)結構，後面接著金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="d24dc-124">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="d24dc-125"><dt>**BCRYPT 不 \_ 透明的 \_ 金鑰 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="d24dc-125"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="d24dc-126">使用 (CSP) 的單一 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) 專用的格式來匯出對稱金鑰。</span><span class="sxs-lookup"><span data-stu-id="d24dc-126">Export a symmetric key in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="d24dc-127">不透明的 Blob 無法轉移，而且必須使用產生 BLOB 的相同 *密碼編譯服務提供者* (CSP) 來匯入。</span><span class="sxs-lookup"><span data-stu-id="d24dc-127">Opaque BLOBs are not transferable and must be imported by using the same *cryptographic service provider* (CSP) that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="d24dc-128"><dt>**BCRYPT \_ RSAPUBLIC \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="d24dc-128"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="d24dc-129">匯出 RSA 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="d24dc-129">Export an RSA public key.</span></span> <span data-ttu-id="d24dc-130">*PbOutput* 緩衝區會立即接收 [**BCRYPT \_ RSAKEY \_ BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob)結構，後面接著金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="d24dc-130">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="d24dc-131">*pbOutput* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-131">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d24dc-132">接收 [*金鑰 BLOB*](/windows/desktop/SecGloss/k-gly)的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="d24dc-132">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="d24dc-133">*CbOutput* 參數包含這個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="d24dc-133">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="d24dc-134">如果此參數為 **Null**，此函式會將所需的大小（以位元組為單位）放在 *pcbResult* 參數所指向的 **DWORD** 中。</span><span class="sxs-lookup"><span data-stu-id="d24dc-134">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d24dc-135">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-135">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24dc-136">*PbOutput* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d24dc-136">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d24dc-137">*pcbResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-137">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d24dc-138">**DWORD** 變數的位址，接收復制到 *pbOutput* 緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d24dc-138">The address of a **DWORD** variable that receives the number of bytes copied to the *pbOutput* buffer.</span></span> <span data-ttu-id="d24dc-139">當呼叫函式時，如果 *pbOutput* 參數設定為 **Null** ，則會在此參數所指向的 **DWORD** 中傳回 *pbOutput* 緩衝區所需的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d24dc-139">If the *pbOutput* parameter is set to **NULL** when the function is called, the required size for the *pbOutput* buffer, in bytes, is returned in the **DWORD** pointed to by this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d24dc-140">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-140">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d24dc-141">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="d24dc-141">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d24dc-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="d24dc-142">Return value</span></span>

<span data-ttu-id="d24dc-143">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d24dc-143">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="d24dc-144">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="d24dc-144">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="d24dc-145">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="d24dc-145">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="d24dc-146">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="d24dc-146">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="d24dc-147">Description</span><span class="sxs-lookup"><span data-stu-id="d24dc-147">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="d24dc-148">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="d24dc-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="d24dc-149">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="d24dc-149">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d24dc-150">備註</span><span class="sxs-lookup"><span data-stu-id="d24dc-150">Remarks</span></span>

<span data-ttu-id="d24dc-151">**SslExportKey** 函式可加速將工作階段金鑰從某個進程傳輸到另一個進程，以及將暫時性金鑰匯出為公用部分。</span><span class="sxs-lookup"><span data-stu-id="d24dc-151">The **SslExportKey** function facilitates transporting session keys from one process to another as well as exporting the public portion an ephemeral key.</span></span>

<span data-ttu-id="d24dc-152">當匯出工作階段金鑰時，BLOB 類型不是透明的，也就是說，只要 **SslExportKey** 和 [**SslImportKey**](sslimportkey.md) 函式可以解讀 blob 的格式，就不會有任何意義。</span><span class="sxs-lookup"><span data-stu-id="d24dc-152">When exporting session keys, the BLOB type is opaque, meaning that the format of the BLOB is irrelevant as long as both the **SslExportKey** and [**SslImportKey**](sslimportkey.md) functions can interpret it.</span></span>

<span data-ttu-id="d24dc-153">匯出暫時金鑰的公開部分時，BLOB 類型必須是適當的類型，例如 **NCRYPT \_ DH \_ 公用 \_ BLOB** 或 **NCRYPT \_ ECCPUBLIC \_ BLOB**。</span><span class="sxs-lookup"><span data-stu-id="d24dc-153">When exporting the public portion of an ephemeral key the BLOB type must be the appropriate type, such as **NCRYPT\_DH\_PUBLIC\_BLOB** or **NCRYPT\_ECCPUBLIC\_BLOB**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d24dc-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="d24dc-154">Requirements</span></span>



| <span data-ttu-id="d24dc-155">需求</span><span class="sxs-lookup"><span data-stu-id="d24dc-155">Requirement</span></span> | <span data-ttu-id="d24dc-156">值</span><span class="sxs-lookup"><span data-stu-id="d24dc-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d24dc-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d24dc-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d24dc-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-158">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d24dc-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d24dc-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d24dc-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d24dc-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d24dc-161">標頭</span><span class="sxs-lookup"><span data-stu-id="d24dc-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="d24dc-162"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="d24dc-162"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="d24dc-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d24dc-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d24dc-164"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d24dc-164"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

