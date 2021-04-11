---
description: 將單一安全通訊端層通訊協定解密 (SSL) 封包。
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: 'SslDecryptPacket 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943925"
---
# <a name="ssldecryptpacket-function"></a><span data-ttu-id="6e7d4-103">SslDecryptPacket 函式</span><span class="sxs-lookup"><span data-stu-id="6e7d4-103">SslDecryptPacket function</span></span>

<span data-ttu-id="6e7d4-104">**SslDecryptPacket** 函式會將單一 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)解密 (SSL) 封包。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-104">the **SslDecryptPacket** function decrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7d4-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e7d4-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6e7d4-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e7d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e7d4-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="6e7d4-109">*hKey* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-110">用來解密封包的金鑰控制碼。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-110">The handle to the key that is used to decrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="6e7d4-111">*pbInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-112">包含要解密之封包的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-112">A pointer to the buffer that contains the packet to be decrypted.</span></span>

</dd> <dt>

<span data-ttu-id="6e7d4-113">*cbInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-114">*PbInput* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6e7d4-115">*pbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-116">要包含解密封包的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-116">A pointer to a buffer to contain the decrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="6e7d4-117">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-118">*PbOutput* 緩衝區的長度（位元組）。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6e7d4-119">*pcbResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-120">寫入 *pbOutput* 緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6e7d4-121">*SequenceNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-122">對應至此封包的序號。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="6e7d4-123">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7d4-124">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-124">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e7d4-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e7d4-125">Return value</span></span>

<span data-ttu-id="6e7d4-126">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="6e7d4-127">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-127">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="6e7d4-128">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-128">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6e7d4-129">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="6e7d4-129">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="6e7d4-130">Description</span><span class="sxs-lookup"><span data-stu-id="6e7d4-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="6e7d4-131">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="6e7d4-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="6e7d4-132">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-132">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e7d4-133">備註</span><span class="sxs-lookup"><span data-stu-id="6e7d4-133">Remarks</span></span>

<span data-ttu-id="6e7d4-134">封包長度可以是零，例如解密 "HelloRequest" 訊息時。</span><span class="sxs-lookup"><span data-stu-id="6e7d4-134">The length of the packet can be zero, such as when a "HelloRequest" message is decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7d4-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e7d4-135">Requirements</span></span>



| <span data-ttu-id="6e7d4-136">需求</span><span class="sxs-lookup"><span data-stu-id="6e7d4-136">Requirement</span></span> | <span data-ttu-id="6e7d4-137">值</span><span class="sxs-lookup"><span data-stu-id="6e7d4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7d4-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e7d4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6e7d4-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6e7d4-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e7d4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6e7d4-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e7d4-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6e7d4-142">標頭</span><span class="sxs-lookup"><span data-stu-id="6e7d4-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e7d4-143"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e7d4-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6e7d4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6e7d4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e7d4-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e7d4-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

