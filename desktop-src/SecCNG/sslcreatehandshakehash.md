---
description: 取得用來雜湊交握訊息的雜湊控制碼。
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: 'SslCreateHandshakeHash 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974400"
---
# <a name="sslcreatehandshakehash-function"></a><span data-ttu-id="28958-103">SslCreateHandshakeHash 函式</span><span class="sxs-lookup"><span data-stu-id="28958-103">SslCreateHandshakeHash function</span></span>

<span data-ttu-id="28958-104">**SslCreateHandshakeHash** 函數會取得用來雜湊交握訊息的雜湊控制碼。</span><span class="sxs-lookup"><span data-stu-id="28958-104">The **SslCreateHandshakeHash** function obtains a hash handle that is used to hash handshake messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="28958-105">語法</span><span class="sxs-lookup"><span data-stu-id="28958-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="28958-106">參數</span><span class="sxs-lookup"><span data-stu-id="28958-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28958-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28958-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28958-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="28958-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="28958-109">*phHandshakeHash* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28958-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28958-110">雜湊控制碼，可傳遞給其他 SSL 提供者函式。</span><span class="sxs-lookup"><span data-stu-id="28958-110">A hash handle that can be passed to other SSL provider functions.</span></span>

</dd> <dt>

<span data-ttu-id="28958-111">*dwProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28958-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28958-112">其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="28958-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

> [!Note]  
> <span data-ttu-id="28958-113">此函式不會搭配 SSL 2.0 通訊協定使用。</span><span class="sxs-lookup"><span data-stu-id="28958-113">This function is not used with the SSL 2.0 protocol.</span></span>

 

</dd> <dt>

<span data-ttu-id="28958-114">*dwCipherSuite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28958-114">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28958-115">其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="28958-115">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="28958-116">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28958-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28958-117">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="28958-117">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28958-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="28958-118">Return value</span></span>

<span data-ttu-id="28958-119">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="28958-119">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="28958-120">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="28958-120">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="28958-121">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="28958-121">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="28958-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="28958-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="28958-123">Description</span><span class="sxs-lookup"><span data-stu-id="28958-123">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="28958-124">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="28958-124"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="28958-125">記憶體不足，無法配置雜湊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="28958-125">There is insufficient memory to allocate the hash buffer.</span></span><br/> |
| <dl> <span data-ttu-id="28958-126">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="28958-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="28958-127">*HSslProvider* 控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="28958-127">The *hSslProvider* handle is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="28958-128">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="28958-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="28958-129">*PhHandshakeHash* 為 null。</span><span class="sxs-lookup"><span data-stu-id="28958-129">The *phHandshakeHash* is null.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="28958-130">備註</span><span class="sxs-lookup"><span data-stu-id="28958-130">Remarks</span></span>

<span data-ttu-id="28958-131">**SslCreateHandshakeHash** 函式是用來產生雜湊以在 SSL 交握期間使用的三個函數之一。</span><span class="sxs-lookup"><span data-stu-id="28958-131">The **SslCreateHandshakeHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="28958-132">呼叫 **SslCreateHandshakeHash** 函數來取得雜湊控制碼。</span><span class="sxs-lookup"><span data-stu-id="28958-132">The **SslCreateHandshakeHash** function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="28958-133">[**SslHashHandshake**](sslhashhandshake.md)函式會使用雜湊控制碼來呼叫任意次數，以將資料加入至雜湊。</span><span class="sxs-lookup"><span data-stu-id="28958-133">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="28958-134">使用雜湊控制碼呼叫 [**SslComputeFinishedHash**](sslcomputefinishedhash.md) 函數，以取得雜湊資料的摘要。</span><span class="sxs-lookup"><span data-stu-id="28958-134">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="28958-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="28958-135">Requirements</span></span>



| <span data-ttu-id="28958-136">需求</span><span class="sxs-lookup"><span data-stu-id="28958-136">Requirement</span></span> | <span data-ttu-id="28958-137">值</span><span class="sxs-lookup"><span data-stu-id="28958-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28958-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28958-138">Minimum supported client</span></span><br/> | <span data-ttu-id="28958-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28958-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="28958-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28958-140">Minimum supported server</span></span><br/> | <span data-ttu-id="28958-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28958-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="28958-142">標頭</span><span class="sxs-lookup"><span data-stu-id="28958-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="28958-143"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="28958-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="28958-144">DLL</span><span class="sxs-lookup"><span data-stu-id="28958-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28958-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28958-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

