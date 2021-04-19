---
description: 加密單一安全通訊端層通訊協定 (SSL) 封包。
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: 'SslEncryptPacket 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975338"
---
# <a name="sslencryptpacket-function"></a><span data-ttu-id="441b4-103">SslEncryptPacket 函式</span><span class="sxs-lookup"><span data-stu-id="441b4-103">SslEncryptPacket function</span></span>

<span data-ttu-id="441b4-104">**SslEncryptPacket** 函式會將單一 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)加密 (SSL) 封包。</span><span class="sxs-lookup"><span data-stu-id="441b4-104">The **SslEncryptPacket** function encrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="441b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="441b4-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="441b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="441b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="441b4-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="441b4-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="441b4-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="441b4-109">*hKey* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="441b4-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-110">用來加密封包的金鑰控制碼。</span><span class="sxs-lookup"><span data-stu-id="441b4-110">The handle to the key that is used to encrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="441b4-111">*pbInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="441b4-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-112">包含要加密之封包的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="441b4-112">A pointer to the buffer that contains the packet to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="441b4-113">*cbInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="441b4-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-114">*PbInput* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="441b4-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="441b4-115">*pbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="441b4-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-116">接收加密封包的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="441b4-116">A pointer to a buffer to receive the encrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="441b4-117">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="441b4-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-118">*PbOutput* 緩衝區的長度（位元組）。</span><span class="sxs-lookup"><span data-stu-id="441b4-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="441b4-119">*pcbResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="441b4-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-120">寫入 *pbOutput* 緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="441b4-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="441b4-121">*SequenceNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="441b4-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-122">對應至此封包的序號。</span><span class="sxs-lookup"><span data-stu-id="441b4-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="441b4-123">*dwContentType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="441b4-123">*dwContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-124">對應到這個封包的內容類型，指定用來處理包含的封包的較高層級通訊協定。</span><span class="sxs-lookup"><span data-stu-id="441b4-124">The content type that corresponds to this packet, which specifies the higher level protocol used to process the enclosed packet.</span></span>



| <span data-ttu-id="441b4-125">值</span><span class="sxs-lookup"><span data-stu-id="441b4-125">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="441b4-126">意義</span><span class="sxs-lookup"><span data-stu-id="441b4-126">Meaning</span></span>                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <span data-ttu-id="441b4-127"><dt>**CT \_變更 \_ 加密 \_ 規格**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="441b4-127"><dt>**CT\_CHANGE\_CIPHER\_SPEC**</dt> <dt>20</dt></span></span> </dl> | <span data-ttu-id="441b4-128">表示 ciphering 策略中的變更。</span><span class="sxs-lookup"><span data-stu-id="441b4-128">Indicates a change in the ciphering strategy.</span></span><br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <span data-ttu-id="441b4-129"><dt>**CT \_警示**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="441b4-129"><dt>**CT\_ALERT**</dt> <dt>21</dt></span></span> </dl>                                          | <span data-ttu-id="441b4-130">指出包含的封包包含警示。</span><span class="sxs-lookup"><span data-stu-id="441b4-130">Indicates that the enclosed packet contains an alert.</span></span><br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <span data-ttu-id="441b4-131"><dt>**CT \_交握**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="441b4-131"><dt>**CT\_HANDSHAKE**</dt> <dt>22</dt></span></span> </dl>                              | <span data-ttu-id="441b4-132">指出包含的封包是交握通訊協定的一部分。</span><span class="sxs-lookup"><span data-stu-id="441b4-132">Indicates that the enclosed packet is part of the handshake protocol.</span></span><br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <span data-ttu-id="441b4-133"><dt>**CT \_APPLICATIONDATA**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="441b4-133"><dt>**CT\_APPLICATIONDATA**</dt> <dt>23</dt></span></span> </dl>            | <span data-ttu-id="441b4-134">指出封包包含應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="441b4-134">Indicates that the packet contains application data.</span></span><br/>                  |



 

</dd> <dt>

<span data-ttu-id="441b4-135">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="441b4-135">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441b4-136">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="441b4-136">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="441b4-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="441b4-137">Return value</span></span>

<span data-ttu-id="441b4-138">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="441b4-138">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="441b4-139">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="441b4-139">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="441b4-140">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="441b4-140">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="441b4-141">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="441b4-141">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="441b4-142">Description</span><span class="sxs-lookup"><span data-stu-id="441b4-142">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="441b4-143">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="441b4-143"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="441b4-144">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="441b4-144">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="441b4-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="441b4-145">Requirements</span></span>



| <span data-ttu-id="441b4-146">需求</span><span class="sxs-lookup"><span data-stu-id="441b4-146">Requirement</span></span> | <span data-ttu-id="441b4-147">值</span><span class="sxs-lookup"><span data-stu-id="441b4-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="441b4-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="441b4-148">Minimum supported client</span></span><br/> | <span data-ttu-id="441b4-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="441b4-149">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="441b4-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="441b4-150">Minimum supported server</span></span><br/> | <span data-ttu-id="441b4-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="441b4-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="441b4-152">標頭</span><span class="sxs-lookup"><span data-stu-id="441b4-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="441b4-153"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="441b4-153"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="441b4-154">DLL</span><span class="sxs-lookup"><span data-stu-id="441b4-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="441b4-155"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="441b4-155"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

