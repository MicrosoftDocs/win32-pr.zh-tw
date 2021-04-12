---
description: 使用指定的私密金鑰來簽署雜湊。
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: 'SslSignHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468900"
---
# <a name="sslsignhash-function"></a><span data-ttu-id="81679-103">SslSignHash 函式</span><span class="sxs-lookup"><span data-stu-id="81679-103">SslSignHash function</span></span>

<span data-ttu-id="81679-104">**SslSignHash** 函數會使用指定的 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)來簽署 [*雜湊*](/windows/desktop/SecGloss/h-gly)。</span><span class="sxs-lookup"><span data-stu-id="81679-104">The **SslSignHash** function signs a [*hash*](/windows/desktop/SecGloss/h-gly) by using the specified [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="81679-105">簽署進程會在伺服器上執行。</span><span class="sxs-lookup"><span data-stu-id="81679-105">The signing process is performed on the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="81679-106">語法</span><span class="sxs-lookup"><span data-stu-id="81679-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="81679-107">參數</span><span class="sxs-lookup"><span data-stu-id="81679-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81679-108">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81679-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81679-109">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="81679-109">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="81679-110">*hPrivateKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81679-110">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81679-111">用來簽署雜湊之私密金鑰的控制碼。</span><span class="sxs-lookup"><span data-stu-id="81679-111">The handle to the private key to use to sign the hash.</span></span>

</dd> <dt>

<span data-ttu-id="81679-112">*pbHashValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81679-112">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81679-113">緩衝區的指標，其中包含要簽署的雜湊。</span><span class="sxs-lookup"><span data-stu-id="81679-113">A pointer to a buffer that contains the hash to sign.</span></span>

</dd> <dt>

<span data-ttu-id="81679-114">*cbHashValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81679-114">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81679-115">*PbHashValue* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="81679-115">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="81679-116">*pbSignature* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81679-116">*pbSignature* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81679-117">接收雜湊特徵標記的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="81679-117">The address of a buffer that receives the signature of the hash.</span></span> <span data-ttu-id="81679-118">*CbSignature* 參數包含這個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="81679-118">The *cbSignature* parameter contains the size of this buffer.</span></span> <span data-ttu-id="81679-119">若要判斷緩衝區的所需大小大小，請將 *pbSignature* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="81679-119">To determine the required sized size of the buffer, set the *pbSignature* parameter to **NULL**.</span></span> <span data-ttu-id="81679-120">將會在 *pcbResult* 參數中傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="81679-120">The required size of the buffer will be returned in the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="81679-121">*cbSignature* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81679-121">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81679-122">*PbSignature* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="81679-122">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="81679-123">*pcbResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81679-123">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81679-124">值的指標，此值會在完成時包含寫入至 *pbSignature* 緩衝區的實際位元組數目。</span><span class="sxs-lookup"><span data-stu-id="81679-124">A pointer to a value that, upon completion, contains the actual number of bytes written to the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="81679-125">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81679-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81679-126">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="81679-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81679-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="81679-127">Return value</span></span>

<span data-ttu-id="81679-128">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="81679-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="81679-129">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="81679-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="81679-130">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="81679-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="81679-131">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="81679-131">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="81679-132">Description</span><span class="sxs-lookup"><span data-stu-id="81679-132">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="81679-133">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="81679-133"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="81679-134">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="81679-134">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81679-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="81679-135">Requirements</span></span>



| <span data-ttu-id="81679-136">需求</span><span class="sxs-lookup"><span data-stu-id="81679-136">Requirement</span></span> | <span data-ttu-id="81679-137">值</span><span class="sxs-lookup"><span data-stu-id="81679-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81679-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81679-138">Minimum supported client</span></span><br/> | <span data-ttu-id="81679-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81679-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="81679-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81679-140">Minimum supported server</span></span><br/> | <span data-ttu-id="81679-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81679-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="81679-142">標頭</span><span class="sxs-lookup"><span data-stu-id="81679-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="81679-143"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="81679-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="81679-144">DLL</span><span class="sxs-lookup"><span data-stu-id="81679-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81679-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81679-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

