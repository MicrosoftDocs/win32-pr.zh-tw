---
description: 抓取指定的通訊協定、加密套件和金鑰類型集的加密套件資訊。
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: 'SslLookupCipherSuiteInfo 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852900"
---
# <a name="ssllookupciphersuiteinfo-function"></a><span data-ttu-id="f9363-103">SslLookupCipherSuiteInfo 函式</span><span class="sxs-lookup"><span data-stu-id="f9363-103">SslLookupCipherSuiteInfo function</span></span>

<span data-ttu-id="f9363-104">**SslLookupCipherSuiteInfo** 函式會針對指定的通訊協定、加密套件和金鑰類型集，取得加密套件資訊。</span><span class="sxs-lookup"><span data-stu-id="f9363-104">The **SslLookupCipherSuiteInfo** function retrieves the cipher suite information for a specified protocol, cipher suite, and key type set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9363-105">語法</span><span class="sxs-lookup"><span data-stu-id="f9363-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f9363-106">參數</span><span class="sxs-lookup"><span data-stu-id="f9363-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9363-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f9363-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9363-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f9363-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="f9363-109">*dwProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f9363-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9363-110">其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="f9363-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="f9363-111">*dwCipherSuite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f9363-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9363-112">其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="f9363-112">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="f9363-113">*dwKeyType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f9363-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9363-114">其中一個 [**CNG SSL 提供者金鑰類型識別碼**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="f9363-114">One of the [**CNG SSL Provider Key Type Identifiers**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="f9363-115">*pCipherSuite* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f9363-115">*pCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9363-116">包含 [**NCRYPT \_ SSL \_ 密碼 \_ 套件**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) 結構的緩衝區位址，用來寫入加密套件資訊。</span><span class="sxs-lookup"><span data-stu-id="f9363-116">The address of a buffer that contains a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure in which to write the cipher suite information.</span></span>

</dd> <dt>

<span data-ttu-id="f9363-117">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f9363-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9363-118">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="f9363-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9363-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9363-119">Return value</span></span>

<span data-ttu-id="f9363-120">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f9363-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="f9363-121">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="f9363-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="f9363-122">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="f9363-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f9363-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f9363-123">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="f9363-124">Description</span><span class="sxs-lookup"><span data-stu-id="f9363-124">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="f9363-125">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="f9363-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="f9363-126">*HSslProvider* 控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="f9363-126">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f9363-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9363-127">Requirements</span></span>



| <span data-ttu-id="f9363-128">需求</span><span class="sxs-lookup"><span data-stu-id="f9363-128">Requirement</span></span> | <span data-ttu-id="f9363-129">值</span><span class="sxs-lookup"><span data-stu-id="f9363-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9363-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9363-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f9363-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9363-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f9363-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9363-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f9363-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9363-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9363-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f9363-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9363-135"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9363-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="f9363-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f9363-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9363-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9363-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

