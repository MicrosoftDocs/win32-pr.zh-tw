---
description: 列舉安全通訊端層的通訊協定 (SSL) 通訊協定提供者所支援的加密套件。
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: 'SslEnumCipherSuites 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318992"
---
# <a name="sslenumciphersuites-function"></a><span data-ttu-id="65956-103">SslEnumCipherSuites 函式</span><span class="sxs-lookup"><span data-stu-id="65956-103">SslEnumCipherSuites function</span></span>

<span data-ttu-id="65956-104">**SslEnumCipherSuites** 函式會列舉 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者所支援的加密套件。</span><span class="sxs-lookup"><span data-stu-id="65956-104">The **SslEnumCipherSuites** function enumerates the cipher suites supported by a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="65956-105">語法</span><span class="sxs-lookup"><span data-stu-id="65956-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="65956-106">參數</span><span class="sxs-lookup"><span data-stu-id="65956-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65956-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65956-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65956-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="65956-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="65956-109">*hPrivateKey* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="65956-109">*hPrivateKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65956-110">[*私密金鑰*](/windows/desktop/SecGloss/p-gly)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="65956-110">The handle of a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="65956-111">指定私密金鑰時， **SslEnumCipherSuites** 會列舉與私密金鑰相容的加密套件。</span><span class="sxs-lookup"><span data-stu-id="65956-111">When a private key is specified, **SslEnumCipherSuites** enumerates the cipher suites that are compatible with the private key.</span></span> <span data-ttu-id="65956-112">例如，如果私密金鑰是 DSS 金鑰，則只 \_ 會傳回 dss DHE 加密套件。</span><span class="sxs-lookup"><span data-stu-id="65956-112">For example, if the private key is a DSS key, then only the DSS\_DHE cipher suites are returned.</span></span> <span data-ttu-id="65956-113">如果私密金鑰是 RSA 金鑰，但不支援原始解密作業，則不會傳回 SSL2 加密套件。</span><span class="sxs-lookup"><span data-stu-id="65956-113">If the private key is an RSA key, but it does not support raw decryption operations, then the SSL2 cipher suites are not returned.</span></span>

<span data-ttu-id="65956-114">當您未指定私密金鑰時，請將此參數設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="65956-114">Set this parameter to **NULL** when you are not specifying a private key.</span></span>

> [!Note]  
> <span data-ttu-id="65956-115">*HPrivateKey* 控制碼是藉由呼叫 [**SslOpenPrivateKey**](sslopenprivatekey.md)函數來取得的。</span><span class="sxs-lookup"><span data-stu-id="65956-115">A *hPrivateKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="65956-116">不支援從 [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) 函數取得的控制碼。</span><span class="sxs-lookup"><span data-stu-id="65956-116">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="65956-117">*ppCipherSuite* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="65956-117">*ppCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65956-118">[**NCRYPT \_ SSL \_ 密碼 \_ 套件**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)結構的指標，用來接收清單中下一個加密套件的位址。</span><span class="sxs-lookup"><span data-stu-id="65956-118">A pointer to a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure to receive the address of the next cipher suite in the list.</span></span>

</dd> <dt>

<span data-ttu-id="65956-119">*ppEnumState* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="65956-119">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="65956-120">緩衝區的指標，指出加密套件清單中目前的位置。</span><span class="sxs-lookup"><span data-stu-id="65956-120">A pointer to a buffer that indicates the current position in the list of cipher suites.</span></span>

<span data-ttu-id="65956-121">在第一次呼叫 **SslEnumCipherSuites** 時，將指標設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="65956-121">Set the pointer to **NULL** on the first call to **SslEnumCipherSuites**.</span></span> <span data-ttu-id="65956-122">在每個後續的呼叫中，將未修改的值傳遞回 **SslEnumCipherSuites**。</span><span class="sxs-lookup"><span data-stu-id="65956-122">On each subsequent call, pass the unmodified value back to **SslEnumCipherSuites**.</span></span>

<span data-ttu-id="65956-123">如果沒有更多可用的加密套件，您應該呼叫 [**SslFreeBuffer**](sslfreebuffer.md)函數來釋放 *ppEnumState* 。</span><span class="sxs-lookup"><span data-stu-id="65956-123">When there are no more cipher suites available, you should free *ppEnumState* by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="65956-124">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65956-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65956-125">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="65956-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65956-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="65956-126">Return value</span></span>

<span data-ttu-id="65956-127">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="65956-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="65956-128">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="65956-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="65956-129">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="65956-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="65956-130">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="65956-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="65956-131">Description</span><span class="sxs-lookup"><span data-stu-id="65956-131">Description</span></span>                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="65956-132">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="65956-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>      | <span data-ttu-id="65956-133">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="65956-133">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="65956-134">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="65956-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="65956-135">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="65956-135">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="65956-136">不 <dt>**超過 \_沒有 \_ 其他 \_ 專案**</dt> <dt>0x8009002AL</dt></span><span class="sxs-lookup"><span data-stu-id="65956-136"><dt>**NTE\_NO\_MORE\_ITEMS**</dt> <dt>0x8009002AL</dt></span></span> </dl> | <span data-ttu-id="65956-137">不支援其他加密套件。</span><span class="sxs-lookup"><span data-stu-id="65956-137">No additional cipher suites are supported.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="65956-138">備註</span><span class="sxs-lookup"><span data-stu-id="65956-138">Remarks</span></span>

<span data-ttu-id="65956-139">若要列舉 SSL 提供者所支援的所有加密套件，請在迴圈中呼叫 **SslEnumCipherSuites** 函式，直到不超過最 **大的 \_ \_ \_ 專案** 傳回為止。</span><span class="sxs-lookup"><span data-stu-id="65956-139">To enumerate all cipher suites supported by the SSL provider, call the **SslEnumCipherSuites** function in a loop until **NTE\_NO\_MORE\_ITEMS** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="65956-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="65956-140">Requirements</span></span>



| <span data-ttu-id="65956-141">需求</span><span class="sxs-lookup"><span data-stu-id="65956-141">Requirement</span></span> | <span data-ttu-id="65956-142">值</span><span class="sxs-lookup"><span data-stu-id="65956-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65956-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65956-143">Minimum supported client</span></span><br/> | <span data-ttu-id="65956-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65956-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="65956-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65956-145">Minimum supported server</span></span><br/> | <span data-ttu-id="65956-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65956-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="65956-147">標頭</span><span class="sxs-lookup"><span data-stu-id="65956-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="65956-148"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="65956-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="65956-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="65956-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="65956-150"><dt>Ncrypt .lib</dt></span><span class="sxs-lookup"><span data-stu-id="65956-150"><dt>Ncrypt.lib</dt></span></span> </dl>    |
| <span data-ttu-id="65956-151">DLL</span><span class="sxs-lookup"><span data-stu-id="65956-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65956-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65956-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="65956-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65956-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65956-154">**NCRYPT \_ SSL \_ 密碼 \_ 套件**</span><span class="sxs-lookup"><span data-stu-id="65956-154">**NCRYPT\_SSL\_CIPHER\_SUITE**</span></span>](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

