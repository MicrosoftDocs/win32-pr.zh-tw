---
description: 傳回密碼編譯 API：新一代 (CNG) 雜湊演算法的演算法識別碼，用於傳輸層安全性通訊協定 (TLS) 虛擬隨機函式 (適用于輸入通訊協定、加密套件和金鑰類型的) PRF。
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: 'SslGetCipherSuitePRFHashAlgorithm 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979847"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a><span data-ttu-id="ad686-103">SslGetCipherSuitePRFHashAlgorithm 函式</span><span class="sxs-lookup"><span data-stu-id="ad686-103">SslGetCipherSuitePRFHashAlgorithm function</span></span>

<span data-ttu-id="ad686-104">**SslGetCipherSuitePRFHashAlgorithm** 函式會傳回「密碼編譯 API：新一代」 (CNG) [*雜湊演算法*](/windows/desktop/SecGloss/h-gly)的演算法識別碼，用於 [*傳輸層安全性通訊協定*](/windows/desktop/SecGloss/t-gly) (TLS) [*虛擬隨機函式*](/windows/desktop/SecGloss/p-gly) (適用于輸入通訊協定、加密套件和金鑰類型的 PRF) 。</span><span class="sxs-lookup"><span data-stu-id="ad686-104">The **SslGetCipherSuitePRFHashAlgorithm** function returns the Cryptography API: Next Generation (CNG) Algorithm Identifier of the [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that is used for the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*pseudo-random function*](/windows/desktop/SecGloss/p-gly) (PRF) for the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad686-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad686-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ad686-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad686-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad686-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad686-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad686-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad686-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ad686-109">*dwProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad686-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad686-110">其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="ad686-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="ad686-111">*dwCipherSuite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad686-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad686-112">其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="ad686-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="ad686-113">*dwKeyType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad686-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad686-114">其中一個 [**CNG SSL 提供者金鑰類型識別碼**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="ad686-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="ad686-115">對於非 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly) 編譯 (ECC) 的金鑰類型，請將此參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="ad686-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ad686-116">*szPRFHash* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ad686-116">*szPRFHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad686-117">將用於 TLS PRF 之雜湊的其中一個 [**CNG 演算法識別碼**](cng-algorithm-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="ad686-117">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) for the hash that will be used for the TLS PRF.</span></span>

</dd> <dt>

<span data-ttu-id="ad686-118">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad686-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad686-119">此參數會保留供日後使用，且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="ad686-119">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad686-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad686-120">Return value</span></span>

<span data-ttu-id="ad686-121">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ad686-121">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ad686-122">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="ad686-122">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="ad686-123">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="ad686-123">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="ad686-124">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ad686-124">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="ad686-125">Description</span><span class="sxs-lookup"><span data-stu-id="ad686-125">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad686-126">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="ad686-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="ad686-127">*HSslProvider* 參數包含不正確指標。</span><span class="sxs-lookup"><span data-stu-id="ad686-127">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="ad686-128">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="ad686-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="ad686-129">*SzPRFHash* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ad686-129">The *szPRFHash* parameter is set to **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="ad686-130">不 <dt>**超過 \_不 \_ 支援**</dt>的 <dt>0x80090029L</dt></span><span class="sxs-lookup"><span data-stu-id="ad686-130"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="ad686-131">指定的介面版本不支援選取的函式。</span><span class="sxs-lookup"><span data-stu-id="ad686-131">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="ad686-132">不 <dt>**超過 \_錯誤的 \_ 旗標**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="ad686-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="ad686-133">*DwFlags* 參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="ad686-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="ad686-134">備註</span><span class="sxs-lookup"><span data-stu-id="ad686-134">Remarks</span></span>

<span data-ttu-id="ad686-135">此 **SslGetCipherSuitePRFHashAlgorithm** 函式會針對 tls 1.2 或更新版本的交談呼叫，以查詢將在 tls PRF 中使用的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="ad686-135">This **SslGetCipherSuitePRFHashAlgorithm** function is called for TLS 1.2 or later conversations to query the hashing algorithm that will be used in the TLS PRF.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad686-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad686-136">Requirements</span></span>



| <span data-ttu-id="ad686-137">需求</span><span class="sxs-lookup"><span data-stu-id="ad686-137">Requirement</span></span> | <span data-ttu-id="ad686-138">值</span><span class="sxs-lookup"><span data-stu-id="ad686-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad686-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad686-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ad686-140">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad686-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad686-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad686-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ad686-142">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad686-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad686-143">標頭</span><span class="sxs-lookup"><span data-stu-id="ad686-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad686-144"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad686-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ad686-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ad686-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad686-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad686-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

