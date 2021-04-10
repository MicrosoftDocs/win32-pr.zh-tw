---
description: 計算憑證驗證期間使用的雜湊。
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: 'SslComputeClientAuthHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192299"
---
# <a name="sslcomputeclientauthhash-function"></a><span data-ttu-id="6c13c-103">SslComputeClientAuthHash 函式</span><span class="sxs-lookup"><span data-stu-id="6c13c-103">SslComputeClientAuthHash function</span></span>

<span data-ttu-id="6c13c-104">**SslComputeClientAuthHash** 函式會計算 [*憑證*](/windows/desktop/SecGloss/c-gly)驗證期間所使用的 [*雜湊*](/windows/desktop/SecGloss/h-gly)。</span><span class="sxs-lookup"><span data-stu-id="6c13c-104">The **SslComputeClientAuthHash** function computes a [*hash*](/windows/desktop/SecGloss/h-gly) to use during [*certificate*](/windows/desktop/SecGloss/c-gly) authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c13c-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c13c-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6c13c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c13c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c13c-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c13c-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c13c-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="6c13c-109">*hMasterKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c13c-110">[*主要金鑰*](/windows/desktop/SecGloss/m-gly)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c13c-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="6c13c-111">*hHandshakeHash* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-111">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c13c-112">目前為止所計算之交握雜湊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c13c-112">The handle of the hash of the handshake computed so far.</span></span>

</dd> <dt>

<span data-ttu-id="6c13c-113">*pszAlgId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-113">*pszAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c13c-114">以 null 結束的 Unicode 字串指標，可識別所要求的 [*密碼編譯演算法*](/windows/desktop/SecGloss/c-gly)。</span><span class="sxs-lookup"><span data-stu-id="6c13c-114">A pointer to a null-terminated Unicode string that identifies the requested [*cryptographic algorithm*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="6c13c-115">這可以是其中一個標準的 [**CNG 演算法識別碼**](cng-algorithm-identifiers.md) 或另一個已註冊演算法的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c13c-115">This can be one of the standard [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or the identifier for another registered algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="6c13c-116">*pbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-116">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c13c-117">接收 [*金鑰 BLOB*](/windows/desktop/SecGloss/k-gly)的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="6c13c-117">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="6c13c-118">*CbOutput* 參數包含這個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="6c13c-118">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="6c13c-119">如果此參數為 **Null**，此函式會將所需的大小（以位元組為單位）放在 *pcbResult* 參數所指向的 **DWORD** 中。</span><span class="sxs-lookup"><span data-stu-id="6c13c-119">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6c13c-120">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-120">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c13c-121">*PbOutput* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c13c-121">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6c13c-122">*pcbResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-122">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c13c-123">**DWORD** 值的指標，指定寫入至 *pbOutput* 緩衝區之雜湊的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c13c-123">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6c13c-124">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c13c-125">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="6c13c-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c13c-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c13c-126">Return value</span></span>

<span data-ttu-id="6c13c-127">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6c13c-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="6c13c-128">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="6c13c-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="6c13c-129">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="6c13c-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6c13c-130">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="6c13c-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="6c13c-131">Description</span><span class="sxs-lookup"><span data-stu-id="6c13c-131">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="6c13c-132">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="6c13c-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="6c13c-133">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="6c13c-133">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c13c-134">備註</span><span class="sxs-lookup"><span data-stu-id="6c13c-134">Remarks</span></span>

<span data-ttu-id="6c13c-135">**SslComputeClientAuthHash** 函式會計算在 SSL 信號交換的憑證驗證訊息中傳送的雜湊。</span><span class="sxs-lookup"><span data-stu-id="6c13c-135">The **SslComputeClientAuthHash** function computes the hash that is sent in the certificate verification message of the SSL handshake.</span></span> <span data-ttu-id="6c13c-136">雜湊值的計算方式是建立包含主要密碼的雜湊，並在其中傳送或接收所有先前的交握訊息雜湊。</span><span class="sxs-lookup"><span data-stu-id="6c13c-136">The hash value is computed by creating a hash that contains the master secret with a hash of all previous handshake messages sent or received.</span></span> <span data-ttu-id="6c13c-137">如需 SSL 交握順序的詳細資訊，請參閱 [安全通訊端層 (ssl) 交握的說明](https://support.microsoft.com/kb/257591)。</span><span class="sxs-lookup"><span data-stu-id="6c13c-137">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

<span data-ttu-id="6c13c-138">雜湊的計算方式取決於所使用的通訊協定和加密套件。</span><span class="sxs-lookup"><span data-stu-id="6c13c-138">The manner in which the hash is computed depends on the protocol and cipher suite used.</span></span> <span data-ttu-id="6c13c-139">此外，雜湊取決於所使用的用戶端驗證金鑰類型; *pszAlgId* 參數會指出用於用戶端驗證的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="6c13c-139">In addition, the hash depends on the type of client authentication key used; the *pszAlgId* parameter indicates the type of key used for client authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c13c-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c13c-140">Requirements</span></span>



| <span data-ttu-id="6c13c-141">需求</span><span class="sxs-lookup"><span data-stu-id="6c13c-141">Requirement</span></span> | <span data-ttu-id="6c13c-142">值</span><span class="sxs-lookup"><span data-stu-id="6c13c-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c13c-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c13c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6c13c-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6c13c-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c13c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6c13c-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c13c-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6c13c-147">標頭</span><span class="sxs-lookup"><span data-stu-id="6c13c-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c13c-148"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c13c-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6c13c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6c13c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c13c-150"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c13c-150"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

