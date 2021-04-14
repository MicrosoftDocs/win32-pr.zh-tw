---
description: 計算 (SSL) 主要秘密金鑰的安全通訊端層通訊協定。
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: 'SslGenerateMasterKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386298"
---
# <a name="sslgeneratemasterkey-function"></a><span data-ttu-id="06e6f-103">SslGenerateMasterKey 函式</span><span class="sxs-lookup"><span data-stu-id="06e6f-103">SslGenerateMasterKey function</span></span>

<span data-ttu-id="06e6f-104">**SslGenerateMasterKey** 函式會 (SSL) 主要秘密金鑰來計算 [*安全通訊端層的通訊協定*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="06e6f-104">The **SslGenerateMasterKey** function computes the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) master secret key.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e6f-105">語法</span><span class="sxs-lookup"><span data-stu-id="06e6f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="06e6f-106">參數</span><span class="sxs-lookup"><span data-stu-id="06e6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e6f-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="06e6f-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-109">*hPrivateKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-110">交換中所使用之 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="06e6f-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-111">*hPublicKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-111">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-112">交換中所使用 [*公開金鑰*](/windows/desktop/SecGloss/p-gly) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="06e6f-112">The handle to the [*public key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-113">*phMasterKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-113">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-114">所產生之 [*主要金鑰*](/windows/desktop/SecGloss/m-gly)的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="06e6f-114">A pointer to the handle to the generated [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-115">*dwProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-115">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-116">其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="06e6f-116">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-117">*dwCipherSuite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-117">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-118">其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="06e6f-118">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-119">*pParameterList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-119">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-120">[**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx)緩衝區陣列的指標，其中包含用來做為金鑰交換作業一部分的資訊。</span><span class="sxs-lookup"><span data-stu-id="06e6f-120">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="06e6f-121">確切的緩衝區集取決於所使用的通訊協定和加密套件。</span><span class="sxs-lookup"><span data-stu-id="06e6f-121">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="06e6f-122">清單最少會包含緩衝區，其中包含用戶端和伺服器提供的隨機值。</span><span class="sxs-lookup"><span data-stu-id="06e6f-122">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-123">*pbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-123">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-124">接收以伺服器的公開金鑰加密之 premaster 秘密的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="06e6f-124">The address of a buffer that receives the premaster secret encrypted with the public key of the server.</span></span> <span data-ttu-id="06e6f-125">*CbOutput* 參數包含這個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="06e6f-125">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="06e6f-126">如果此參數為 **Null**，則此函式會傳回 *pcbResult* 參數所指向之 **DWORD** 中所需的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="06e6f-126">If this parameter is **NULL**, this function returns the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="06e6f-127">執行 RSA 金鑰交換時，會使用這個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06e6f-127">This buffer is used when performing a RSA key exchange.</span></span>

 

</dd> <dt>

<span data-ttu-id="06e6f-128">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-128">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-129">*PbOutput* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="06e6f-129">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-130">*pcbResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-130">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-131">**DWORD** 值的指標，要在其中放置寫入至 *pbOutput* 緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="06e6f-131">A pointer to a **DWORD** value in which to place number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="06e6f-132">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e6f-133">指定此函數是否用於用戶端或伺服器端金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="06e6f-133">Specifies whether this function is being used for client-side or server-side key exchange.</span></span>



| <span data-ttu-id="06e6f-134">值</span><span class="sxs-lookup"><span data-stu-id="06e6f-134">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="06e6f-135">意義</span><span class="sxs-lookup"><span data-stu-id="06e6f-135">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="06e6f-136"><dt>**NCRYPT \_SSL \_ 用戶端 \_ 旗**</dt>標 <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="06e6f-136"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="06e6f-137">指定用戶端金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="06e6f-137">Specifies a client-side key exchange.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="06e6f-138"><dt>**NCRYPT \_SSL \_ 伺服器 \_ 旗**</dt>標 <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="06e6f-138"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="06e6f-139">指定伺服器端金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="06e6f-139">Specifies a server-side key exchange.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e6f-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="06e6f-140">Return value</span></span>

<span data-ttu-id="06e6f-141">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="06e6f-141">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="06e6f-142">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="06e6f-142">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="06e6f-143">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="06e6f-143">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="06e6f-144">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="06e6f-144">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="06e6f-145">Description</span><span class="sxs-lookup"><span data-stu-id="06e6f-145">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06e6f-146">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="06e6f-146"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="06e6f-147">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06e6f-147">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="06e6f-148">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="06e6f-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="06e6f-149">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="06e6f-149">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="06e6f-150">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="06e6f-150"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="06e6f-151">*PhMasterKey* 或 *hPublicKey* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="06e6f-151">The *phMasterKey* or *hPublicKey* parameter is not valid.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="06e6f-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="06e6f-152">Requirements</span></span>



| <span data-ttu-id="06e6f-153">需求</span><span class="sxs-lookup"><span data-stu-id="06e6f-153">Requirement</span></span> | <span data-ttu-id="06e6f-154">值</span><span class="sxs-lookup"><span data-stu-id="06e6f-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e6f-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06e6f-155">Minimum supported client</span></span><br/> | <span data-ttu-id="06e6f-156">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-156">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06e6f-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06e6f-157">Minimum supported server</span></span><br/> | <span data-ttu-id="06e6f-158">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06e6f-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="06e6f-159">標頭</span><span class="sxs-lookup"><span data-stu-id="06e6f-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="06e6f-160"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="06e6f-160"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="06e6f-161">DLL</span><span class="sxs-lookup"><span data-stu-id="06e6f-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06e6f-162"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06e6f-162"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

