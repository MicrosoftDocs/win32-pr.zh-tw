---
description: 傳回交握雜湊的控制碼。
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: 'SslHashHandshake 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944965"
---
# <a name="sslhashhandshake-function"></a><span data-ttu-id="fd2ec-103">SslHashHandshake 函式</span><span class="sxs-lookup"><span data-stu-id="fd2ec-103">SslHashHandshake function</span></span>

<span data-ttu-id="fd2ec-104">**SslHashHandshake** 函式會傳回交握雜湊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-104">The **SslHashHandshake** function returns a handle to the handshake hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2ec-105">語法</span><span class="sxs-lookup"><span data-stu-id="fd2ec-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fd2ec-106">參數</span><span class="sxs-lookup"><span data-stu-id="fd2ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd2ec-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd2ec-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2ec-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="fd2ec-109">*hHandshakeHash* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="fd2ec-109">*hHandshakeHash* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2ec-110">雜湊物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-110">The handle to the hash object.</span></span>

</dd> <dt>

<span data-ttu-id="fd2ec-111">*pbInput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fd2ec-111">*pbInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2ec-112">包含要雜湊之資料的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-112">The address of a buffer that contains the data to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="fd2ec-113">*cbInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd2ec-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2ec-114">*PbInput* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-114">The size, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fd2ec-115">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd2ec-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2ec-116">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-116">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd2ec-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd2ec-117">Return value</span></span>

<span data-ttu-id="fd2ec-118">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-118">If the function succeeds, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd2ec-119">備註</span><span class="sxs-lookup"><span data-stu-id="fd2ec-119">Remarks</span></span>

<span data-ttu-id="fd2ec-120">**SslHashHandshake** 函式是用來產生雜湊以在 SSL 交握期間使用的三個函數之一。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-120">The **SslHashHandshake** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="fd2ec-121">呼叫 [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) 函數來取得雜湊控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-121">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="fd2ec-122">**SslHashHandshake** 函式會使用雜湊控制碼來呼叫任意次數，以將資料加入至雜湊。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-122">The **SslHashHandshake** function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="fd2ec-123">使用雜湊控制碼呼叫 [**SslComputeFinishedHash**](sslcomputefinishedhash.md) 函數，以取得雜湊資料的摘要。</span><span class="sxs-lookup"><span data-stu-id="fd2ec-123">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd2ec-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd2ec-124">Requirements</span></span>



| <span data-ttu-id="fd2ec-125">需求</span><span class="sxs-lookup"><span data-stu-id="fd2ec-125">Requirement</span></span> | <span data-ttu-id="fd2ec-126">值</span><span class="sxs-lookup"><span data-stu-id="fd2ec-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2ec-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd2ec-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fd2ec-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd2ec-128">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fd2ec-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd2ec-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fd2ec-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd2ec-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fd2ec-131">標頭</span><span class="sxs-lookup"><span data-stu-id="fd2ec-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd2ec-132"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd2ec-132"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="fd2ec-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fd2ec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd2ec-134"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd2ec-134"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

