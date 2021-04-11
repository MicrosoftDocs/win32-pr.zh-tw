---
description: 開啟私密金鑰的控制碼。
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: 'SslOpenPrivateKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112688"
---
# <a name="sslopenprivatekey-function"></a><span data-ttu-id="db9cb-103">SslOpenPrivateKey 函式</span><span class="sxs-lookup"><span data-stu-id="db9cb-103">SslOpenPrivateKey function</span></span>

<span data-ttu-id="db9cb-104">**SslOpenPrivateKey** 函式會開啟 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="db9cb-104">The **SslOpenPrivateKey** function opens a handle to a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="db9cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="db9cb-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="db9cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="db9cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9cb-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9cb-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="db9cb-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="db9cb-109">*phPrivateKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-109">*phPrivateKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db9cb-110">要在其中將控制碼寫入至私密金鑰的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="db9cb-110">The address of a buffer in which to write the handle to the private key.</span></span>

<span data-ttu-id="db9cb-111">當您完成使用索引鍵時，您應該呼叫 [**SslFreeObject**](sslfreeobject.md)函式來釋放 *phPrivateKey* 。</span><span class="sxs-lookup"><span data-stu-id="db9cb-111">When you have finished using the key, you should free *phPrivateKey* by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="db9cb-112">*pCertCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-112">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9cb-113">從中取得私密金鑰的憑證位址。</span><span class="sxs-lookup"><span data-stu-id="db9cb-113">The address of the certificate from which to obtain the private key.</span></span>

</dd> <dt>

<span data-ttu-id="db9cb-114">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9cb-115">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="db9cb-115">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9cb-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="db9cb-116">Return value</span></span>

<span data-ttu-id="db9cb-117">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="db9cb-117">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="db9cb-118">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="db9cb-118">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="db9cb-119">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="db9cb-119">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="db9cb-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="db9cb-120">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="db9cb-121">Description</span><span class="sxs-lookup"><span data-stu-id="db9cb-121">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db9cb-122">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="db9cb-122"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="db9cb-123">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="db9cb-123">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="db9cb-124">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="db9cb-124"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="db9cb-125">*HSslProvider* 控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="db9cb-125">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="db9cb-126">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="db9cb-126"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="db9cb-127">*PhPrivateKey* 或 *PCertCoNtext* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="db9cb-127">The *phPrivateKey* or *pCertContext* parameter is **NULL**.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="db9cb-128">備註</span><span class="sxs-lookup"><span data-stu-id="db9cb-128">Remarks</span></span>

<span data-ttu-id="db9cb-129">取得的私密金鑰是 [*憑證*](/windows/desktop/SecGloss/c-gly)內 [*公開/私密金鑰*](/windows/desktop/SecGloss/p-gly)組的一部分。</span><span class="sxs-lookup"><span data-stu-id="db9cb-129">The private key obtained is part of a [*public/private key pair*](/windows/desktop/SecGloss/p-gly) within a [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="db9cb-130">此函式只會從 *pCertCoNtext* 參數所指定的憑證解壓縮私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="db9cb-130">This function merely extracts the private key from the certificate specified by the *pCertContext* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9cb-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="db9cb-131">Requirements</span></span>



| <span data-ttu-id="db9cb-132">需求</span><span class="sxs-lookup"><span data-stu-id="db9cb-132">Requirement</span></span> | <span data-ttu-id="db9cb-133">值</span><span class="sxs-lookup"><span data-stu-id="db9cb-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db9cb-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db9cb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="db9cb-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="db9cb-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db9cb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="db9cb-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db9cb-138">標頭</span><span class="sxs-lookup"><span data-stu-id="db9cb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9cb-139"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="db9cb-139"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="db9cb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="db9cb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db9cb-141"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db9cb-141"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

