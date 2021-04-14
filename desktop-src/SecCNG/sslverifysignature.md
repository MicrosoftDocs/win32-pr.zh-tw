---
description: 使用提供的雜湊和公開金鑰，驗證指定的簽章。
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: 'SslVerifySignature 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847893"
---
# <a name="sslverifysignature-function"></a><span data-ttu-id="218d3-103">SslVerifySignature 函式</span><span class="sxs-lookup"><span data-stu-id="218d3-103">SslVerifySignature function</span></span>

<span data-ttu-id="218d3-104">**SslVerifySignature** 函式會使用提供的 [*雜湊*](/windows/desktop/SecGloss/h-gly)和 [*公開金鑰*](/windows/desktop/SecGloss/p-gly)，驗證指定的簽章。</span><span class="sxs-lookup"><span data-stu-id="218d3-104">The **SslVerifySignature** function verifies the specified signature by using the supplied [*hash*](/windows/desktop/SecGloss/h-gly) and the [*public key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="218d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="218d3-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="218d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="218d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="218d3-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="218d3-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218d3-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="218d3-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="218d3-109">*hPublicKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="218d3-109">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218d3-110">公開金鑰的控制碼。</span><span class="sxs-lookup"><span data-stu-id="218d3-110">The handle to the public key.</span></span>

</dd> <dt>

<span data-ttu-id="218d3-111">*pbHashValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="218d3-111">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218d3-112">緩衝區的指標，其中包含要用來驗證簽章的雜湊。</span><span class="sxs-lookup"><span data-stu-id="218d3-112">A pointer to a buffer that contains the hash to use to verify the signature.</span></span>

</dd> <dt>

<span data-ttu-id="218d3-113">*cbHashValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="218d3-113">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218d3-114">*PbHashValue* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="218d3-114">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="218d3-115">*pbSignature* \[在\]</span><span class="sxs-lookup"><span data-stu-id="218d3-115">*pbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218d3-116">緩衝區的指標，此緩衝區包含要驗證的簽章。</span><span class="sxs-lookup"><span data-stu-id="218d3-116">A pointer to a buffer that contains the signature to verify.</span></span>

</dd> <dt>

<span data-ttu-id="218d3-117">*cbSignature* \[在\]</span><span class="sxs-lookup"><span data-stu-id="218d3-117">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218d3-118">*PbSignature* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="218d3-118">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="218d3-119">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="218d3-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218d3-120">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="218d3-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="218d3-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="218d3-121">Return value</span></span>

<span data-ttu-id="218d3-122">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="218d3-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="218d3-123">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="218d3-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="218d3-124">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="218d3-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="218d3-125">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="218d3-125">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="218d3-126">Description</span><span class="sxs-lookup"><span data-stu-id="218d3-126">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="218d3-127">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="218d3-127"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="218d3-128">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="218d3-128">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="218d3-129">備註</span><span class="sxs-lookup"><span data-stu-id="218d3-129">Remarks</span></span>

<span data-ttu-id="218d3-130">Windows 目前未呼叫 **SslVerifySignature** 函數。</span><span class="sxs-lookup"><span data-stu-id="218d3-130">The **SslVerifySignature** function is not currently called by Windows.</span></span> <span data-ttu-id="218d3-131">此函式是 SSL 提供者介面的必要部分，應完全實作為以確保向前相容性。</span><span class="sxs-lookup"><span data-stu-id="218d3-131">This function is a required part of the SSL Provider interface and should be fully implemented to ensure forward compatibility.</span></span>

<span data-ttu-id="218d3-132">[*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly)的伺服器端目前的執行 (TLS) 連線在用戶端驗證期間呼叫 [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature)函式，以處理憑證驗證訊息。</span><span class="sxs-lookup"><span data-stu-id="218d3-132">Current implementations of the server side of the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) connection call the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) function during the client authentication to process the certificate verify message.</span></span>

## <a name="requirements"></a><span data-ttu-id="218d3-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="218d3-133">Requirements</span></span>



| <span data-ttu-id="218d3-134">需求</span><span class="sxs-lookup"><span data-stu-id="218d3-134">Requirement</span></span> | <span data-ttu-id="218d3-135">值</span><span class="sxs-lookup"><span data-stu-id="218d3-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="218d3-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="218d3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="218d3-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="218d3-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="218d3-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="218d3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="218d3-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="218d3-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="218d3-140">標頭</span><span class="sxs-lookup"><span data-stu-id="218d3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="218d3-141"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="218d3-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="218d3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="218d3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="218d3-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="218d3-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

