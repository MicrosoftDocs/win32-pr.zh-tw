---
description: 抓取用於用戶端驗證之交握雜湊的控制碼。
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: 'SslCreateClientAuthHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974639"
---
# <a name="sslcreateclientauthhash-function"></a><span data-ttu-id="5bf9e-103">SslCreateClientAuthHash 函式</span><span class="sxs-lookup"><span data-stu-id="5bf9e-103">SslCreateClientAuthHash function</span></span>

<span data-ttu-id="5bf9e-104">**SslCreateClientAuthHash** 函式會抓取用於用戶端驗證之交握 [*雜湊*](/windows/desktop/SecGloss/h-gly)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-104">The **SslCreateClientAuthHash** function retrieves a handle to the handshake [*hash*](/windows/desktop/SecGloss/h-gly) that is used for client authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5bf9e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5bf9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5bf9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf9e-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bf9e-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf9e-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5bf9e-109">*phHandshakeHash* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5bf9e-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf9e-110">要接收雜湊控制碼之 **NCRYPT \_ 雜湊 \_ 控制碼** 變數的指標。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-110">A pointer to an **NCRYPT\_HASH\_HANDLE** variable to receive the hash handle.</span></span>

</dd> <dt>

<span data-ttu-id="5bf9e-111">*dwProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bf9e-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf9e-112">其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5bf9e-113">*dwCipherSuite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bf9e-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf9e-114">其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5bf9e-115">*pszHashAlgId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bf9e-115">*pszHashAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf9e-116">其中一個 [**CNG 演算法識別碼**](cng-algorithm-identifiers.md) 值。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-116">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) values.</span></span>

</dd> <dt>

<span data-ttu-id="5bf9e-117">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bf9e-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf9e-118">此參數會保留供日後使用，且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-118">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf9e-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bf9e-119">Return value</span></span>

<span data-ttu-id="5bf9e-120">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5bf9e-121">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5bf9e-122">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5bf9e-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="5bf9e-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="5bf9e-124">Description</span><span class="sxs-lookup"><span data-stu-id="5bf9e-124">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bf9e-125">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="5bf9e-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="5bf9e-126">*HSslProvider* 參數包含不正確指標。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-126">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="5bf9e-127">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="5bf9e-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="5bf9e-128">*PhHandshakeHash* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-128">The *phHandshakeHash* parameter is set to **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="5bf9e-129">不 <dt>**超過 \_不 \_ 支援**</dt>的 <dt>0x80090029L</dt></span><span class="sxs-lookup"><span data-stu-id="5bf9e-129"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="5bf9e-130">指定的介面版本不支援選取的函式。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-130">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="5bf9e-131">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="5bf9e-131"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="5bf9e-132">記憶體不足，無法配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-132">Insufficient memory to allocate buffers.</span></span><br/>                                          |
| <dl> <span data-ttu-id="5bf9e-133">不 <dt>**超過 \_錯誤的 \_ 旗標**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="5bf9e-133"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="5bf9e-134">*DwFlags* 參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-134">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="5bf9e-135">備註</span><span class="sxs-lookup"><span data-stu-id="5bf9e-135">Remarks</span></span>

<span data-ttu-id="5bf9e-136">**SslCreateClientAuthHash** 函式是針對 [*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly)（ (TLS) 1.2 或更新版本的交談）進行呼叫，以建立用來雜湊交握訊息的雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-136">The **SslCreateClientAuthHash** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.2 or later conversations to create hash objects that are used to hash handshake messages.</span></span> <span data-ttu-id="5bf9e-137">它會針對每個可用於用戶端驗證簽章的 [*雜湊演算法*](/windows/desktop/SecGloss/h-gly) 呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="5bf9e-137">It is called once for each possible [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that can be used in the client authentication signature.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf9e-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bf9e-138">Requirements</span></span>



| <span data-ttu-id="5bf9e-139">需求</span><span class="sxs-lookup"><span data-stu-id="5bf9e-139">Requirement</span></span> | <span data-ttu-id="5bf9e-140">值</span><span class="sxs-lookup"><span data-stu-id="5bf9e-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf9e-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5bf9e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf9e-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bf9e-142">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5bf9e-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5bf9e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf9e-144">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bf9e-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5bf9e-145">標頭</span><span class="sxs-lookup"><span data-stu-id="5bf9e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bf9e-146"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="5bf9e-146"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5bf9e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5bf9e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bf9e-148"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bf9e-148"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

