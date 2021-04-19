---
description: 執行伺服器端安全通訊端層通訊協定 (SSL) 金鑰交換操作。
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: 'SslImportMasterKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993126"
---
# <a name="sslimportmasterkey-function"></a><span data-ttu-id="42e6a-103">SslImportMasterKey 函式</span><span class="sxs-lookup"><span data-stu-id="42e6a-103">SslImportMasterKey function</span></span>

<span data-ttu-id="42e6a-104">**SslImportMasterKey** 函式會 (SSL) 金鑰交換作業來執行伺服器端 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="42e6a-104">The **SslImportMasterKey** function performs a server-side [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) key exchange operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e6a-105">語法</span><span class="sxs-lookup"><span data-stu-id="42e6a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="42e6a-106">參數</span><span class="sxs-lookup"><span data-stu-id="42e6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e6a-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="42e6a-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="42e6a-109">*hPrivateKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-110">交換中所使用之 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="42e6a-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="42e6a-111">*phMasterKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-111">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-112">要接收 [*主要金鑰*](/windows/desktop/SecGloss/m-gly)的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="42e6a-112">A pointer to the handle to receive the [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="42e6a-113">*dwProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-113">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-114">其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="42e6a-114">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="42e6a-115">*dwCipherSuite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-115">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-116">其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="42e6a-116">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="42e6a-117">*pParameterList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-117">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-118">[**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx)緩衝區陣列的指標，其中包含用來做為金鑰交換作業一部分的資訊。</span><span class="sxs-lookup"><span data-stu-id="42e6a-118">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="42e6a-119">確切的緩衝區集取決於所使用的通訊協定和加密套件。</span><span class="sxs-lookup"><span data-stu-id="42e6a-119">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="42e6a-120">清單最少會包含緩衝區，其中包含用戶端和伺服器提供的隨機值。</span><span class="sxs-lookup"><span data-stu-id="42e6a-120">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="42e6a-121">*pbEncryptedKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-121">*pbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-122">緩衝區的指標，其中包含加密的 premaster 秘密金鑰，並以伺服器的 [*公開金鑰*](/windows/desktop/SecGloss/p-gly) 加密。</span><span class="sxs-lookup"><span data-stu-id="42e6a-122">A pointer to a buffer that contains the encrypted premaster secret key encrypted with the [*public key*](/windows/desktop/SecGloss/p-gly) of the server.</span></span>

</dd> <dt>

<span data-ttu-id="42e6a-123">*cbEncryptedKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-123">*cbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-124">*PbEncryptedKey* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="42e6a-124">The size, in bytes, of the *pbEncryptedKey* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="42e6a-125">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e6a-126">將此參數設定為 **NCRYPT \_ SSL \_ 伺服器 \_ 旗** 標，表示這是伺服器呼叫。</span><span class="sxs-lookup"><span data-stu-id="42e6a-126">Set this parameter to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42e6a-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="42e6a-127">Return value</span></span>

<span data-ttu-id="42e6a-128">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="42e6a-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="42e6a-129">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="42e6a-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="42e6a-130">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="42e6a-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="42e6a-131">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="42e6a-131">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="42e6a-132">Description</span><span class="sxs-lookup"><span data-stu-id="42e6a-132">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42e6a-133">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="42e6a-133"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="42e6a-134">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="42e6a-134">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="42e6a-135">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="42e6a-135"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="42e6a-136">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="42e6a-136">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="42e6a-137">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="42e6a-137"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="42e6a-138">*PhMasterKey* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="42e6a-138">The *phMasterKey* parameter is **NULL**.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="42e6a-139">備註</span><span class="sxs-lookup"><span data-stu-id="42e6a-139">Remarks</span></span>

<span data-ttu-id="42e6a-140">此函式會將 premaster 秘密解密、計算 SSL 主要密碼，然後將此物件的控制碼傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="42e6a-140">This function decrypts the premaster secret, computes the SSL master secret, and returns a handle to this object to the caller.</span></span> <span data-ttu-id="42e6a-141">然後，您可以使用此主要金鑰來衍生 SSL 工作階段金鑰，並完成 SSL 交握。</span><span class="sxs-lookup"><span data-stu-id="42e6a-141">This master key can then be used to derive the SSL session key and finish the SSL handshake.</span></span>

> [!Note]  
> <span data-ttu-id="42e6a-142">使用 [*RSA*](/windows/desktop/SecGloss/r-gly) 金鑰交換演算法時，會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="42e6a-142">This function is used when the [*RSA*](/windows/desktop/SecGloss/r-gly) key exchange algorithm is being used.</span></span> <span data-ttu-id="42e6a-143">使用 [*DH*](/windows/desktop/SecGloss/d-gly) 時，伺服器程式碼會改為呼叫 [**SslGenerateMasterKey**](sslgeneratemasterkey.md) 。</span><span class="sxs-lookup"><span data-stu-id="42e6a-143">When [*DH*](/windows/desktop/SecGloss/d-gly) is used, then the server code calls [**SslGenerateMasterKey**](sslgeneratemasterkey.md) instead.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42e6a-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="42e6a-144">Requirements</span></span>



| <span data-ttu-id="42e6a-145">需求</span><span class="sxs-lookup"><span data-stu-id="42e6a-145">Requirement</span></span> | <span data-ttu-id="42e6a-146">值</span><span class="sxs-lookup"><span data-stu-id="42e6a-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e6a-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42e6a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="42e6a-148">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-148">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="42e6a-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42e6a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="42e6a-150">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42e6a-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="42e6a-151">標頭</span><span class="sxs-lookup"><span data-stu-id="42e6a-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e6a-152"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="42e6a-152"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="42e6a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="42e6a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42e6a-154"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42e6a-154"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

