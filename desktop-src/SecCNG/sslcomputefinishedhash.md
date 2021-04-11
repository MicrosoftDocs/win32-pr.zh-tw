---
description: 計算在安全通訊端層通訊協定的完成訊息中傳送的雜湊 (SSL) 信號交換。
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: 'SslComputeFinishedHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943929"
---
# <a name="sslcomputefinishedhash-function"></a><span data-ttu-id="85fb4-103">SslComputeFinishedHash 函式</span><span class="sxs-lookup"><span data-stu-id="85fb4-103">SslComputeFinishedHash function</span></span>

<span data-ttu-id="85fb4-104">**SslComputeFinishedHash** 函式會計算在 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)的完成訊息中傳送的 [*雜湊*](/windows/desktop/SecGloss/h-gly) (SSL) 信號交換。</span><span class="sxs-lookup"><span data-stu-id="85fb4-104">The **SslComputeFinishedHash** function computes the [*hash*](/windows/desktop/SecGloss/h-gly) sent in the finished message of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span> <span data-ttu-id="85fb4-105">如需 SSL 交握順序的詳細資訊，請參閱 [安全通訊端層 (ssl) 交握的說明](https://support.microsoft.com/kb/257591)。</span><span class="sxs-lookup"><span data-stu-id="85fb4-105">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

## <a name="syntax"></a><span data-ttu-id="85fb4-106">語法</span><span class="sxs-lookup"><span data-stu-id="85fb4-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="85fb4-107">參數</span><span class="sxs-lookup"><span data-stu-id="85fb4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85fb4-108">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85fb4-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85fb4-109">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="85fb4-109">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="85fb4-110">*hMasterKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85fb4-110">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85fb4-111">[*主要金鑰*](/windows/desktop/SecGloss/m-gly)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="85fb4-111">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="85fb4-112">*hHandshakeHash* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85fb4-112">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85fb4-113">交握訊息雜湊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="85fb4-113">The handle of the hash of the handshake messages.</span></span>

</dd> <dt>

<span data-ttu-id="85fb4-114">*pbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="85fb4-114">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85fb4-115">緩衝區的指標，此緩衝區會接收完成訊息的雜湊。</span><span class="sxs-lookup"><span data-stu-id="85fb4-115">A pointer to a buffer that receives the hash for the finish message.</span></span>

</dd> <dt>

<span data-ttu-id="85fb4-116">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85fb4-116">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85fb4-117">*PbOutput* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="85fb4-117">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="85fb4-118">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85fb4-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85fb4-119">下列其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="85fb4-119">One of the following constants.</span></span>



| <span data-ttu-id="85fb4-120">值</span><span class="sxs-lookup"><span data-stu-id="85fb4-120">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="85fb4-121">意義</span><span class="sxs-lookup"><span data-stu-id="85fb4-121">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="85fb4-122"><dt>**NCRYPT \_SSL \_ 用戶端 \_ 旗**</dt>標 <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="85fb4-122"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="85fb4-123">指定這是用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="85fb4-123">Specifies that this is a client call.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="85fb4-124"><dt>**NCRYPT \_SSL \_ 伺服器 \_ 旗**</dt>標 <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="85fb4-124"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="85fb4-125">指定這是伺服器呼叫。</span><span class="sxs-lookup"><span data-stu-id="85fb4-125">Specifies that this is a server call.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85fb4-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="85fb4-126">Return value</span></span>

<span data-ttu-id="85fb4-127">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="85fb4-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="85fb4-128">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="85fb4-128">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="85fb4-129">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="85fb4-129">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="85fb4-130">Description</span><span class="sxs-lookup"><span data-stu-id="85fb4-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="85fb4-131">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>2148073510 (0x80090026)</dt></span><span class="sxs-lookup"><span data-stu-id="85fb4-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>2148073510 (0x80090026)</dt></span></span> </dl> | <span data-ttu-id="85fb4-132">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="85fb4-132">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="85fb4-133">備註</span><span class="sxs-lookup"><span data-stu-id="85fb4-133">Remarks</span></span>

<span data-ttu-id="85fb4-134">**SslComputeFinishedHash** 函式是用來產生雜湊以在 SSL 交握期間使用的三個函數之一。</span><span class="sxs-lookup"><span data-stu-id="85fb4-134">The **SslComputeFinishedHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="85fb4-135">呼叫 [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) 函數來取得雜湊控制碼。</span><span class="sxs-lookup"><span data-stu-id="85fb4-135">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="85fb4-136">[**SslHashHandshake**](sslhashhandshake.md)函式會使用雜湊控制碼來呼叫任意次數，以將資料加入至雜湊。</span><span class="sxs-lookup"><span data-stu-id="85fb4-136">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="85fb4-137">使用雜湊控制碼呼叫 **SslComputeFinishedHash** 函數，以取得雜湊資料的摘要。</span><span class="sxs-lookup"><span data-stu-id="85fb4-137">The **SslComputeFinishedHash** function is called with the hash handle to obtain the digest of the hashed data.</span></span>

<span data-ttu-id="85fb4-138">雜湊值的計算方式是使用傳送或接收的所有先前交握訊息的雜湊來雜湊主要密碼。</span><span class="sxs-lookup"><span data-stu-id="85fb4-138">The hash value is computed by hashing the master secret with a hash of all previous handshake messages sent or received.</span></span>

<span data-ttu-id="85fb4-139">*CbOutput* 的值會決定雜湊資料的長度。</span><span class="sxs-lookup"><span data-stu-id="85fb4-139">The value of *cbOutput* determines the length of the hash data.</span></span> <span data-ttu-id="85fb4-140">使用 [*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 通訊協定時，應該一律為 12 (個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="85fb4-140">When the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 protocol is used, this should always be 12 (bytes).</span></span> <span data-ttu-id="85fb4-141">如需詳細資訊，請參閱 [TLS 通訊協定1.0 版](https://www.ietf.org/rfc/rfc2246.txt)。</span><span class="sxs-lookup"><span data-stu-id="85fb4-141">For more information, see [The TLS Protocol Version 1.0](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="requirements"></a><span data-ttu-id="85fb4-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="85fb4-142">Requirements</span></span>



| <span data-ttu-id="85fb4-143">需求</span><span class="sxs-lookup"><span data-stu-id="85fb4-143">Requirement</span></span> | <span data-ttu-id="85fb4-144">值</span><span class="sxs-lookup"><span data-stu-id="85fb4-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="85fb4-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85fb4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="85fb4-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85fb4-146">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="85fb4-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85fb4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="85fb4-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85fb4-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85fb4-149">標頭</span><span class="sxs-lookup"><span data-stu-id="85fb4-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="85fb4-150"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="85fb4-150"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="85fb4-151">DLL</span><span class="sxs-lookup"><span data-stu-id="85fb4-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85fb4-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85fb4-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

