---
description: 產生一組安全通訊端層的通訊協定 (SSL) 工作階段金鑰。
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: 'SslGenerateSessionKeys 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982114"
---
# <a name="sslgeneratesessionkeys-function"></a><span data-ttu-id="ae91f-103">SslGenerateSessionKeys 函式</span><span class="sxs-lookup"><span data-stu-id="ae91f-103">SslGenerateSessionKeys function</span></span>

<span data-ttu-id="ae91f-104">**SslGenerateSessionKeys** 函式會產生一組 [*安全通訊端層的通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="ae91f-104">The **SslGenerateSessionKeys** function generates a set of [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) session keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae91f-105">語法</span><span class="sxs-lookup"><span data-stu-id="ae91f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ae91f-106">參數</span><span class="sxs-lookup"><span data-stu-id="ae91f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae91f-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae91f-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ae91f-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ae91f-109">*hMasterKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae91f-110">[*主要金鑰*](/windows/desktop/SecGloss/m-gly)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ae91f-110">The handle to the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="ae91f-111">*phReadKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-111">*phReadKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae91f-112">傳回之讀取按鍵控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="ae91f-112">A pointer to the returned read key handle.</span></span>

</dd> <dt>

<span data-ttu-id="ae91f-113">*phWriteKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-113">*phWriteKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae91f-114">傳回之寫入按鍵控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="ae91f-114">A pointer to the returned write key handle.</span></span>

</dd> <dt>

<span data-ttu-id="ae91f-115">*pParameterList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-115">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae91f-116">[**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx)緩衝區陣列的指標，其中包含用來做為金鑰交換作業一部分的資訊。</span><span class="sxs-lookup"><span data-stu-id="ae91f-116">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="ae91f-117">確切的緩衝區集取決於所使用的通訊協定和加密套件。</span><span class="sxs-lookup"><span data-stu-id="ae91f-117">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="ae91f-118">清單最少會包含緩衝區，其中包含用戶端和伺服器提供的隨機值。</span><span class="sxs-lookup"><span data-stu-id="ae91f-118">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="ae91f-119">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae91f-120">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="ae91f-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae91f-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae91f-121">Return value</span></span>

<span data-ttu-id="ae91f-122">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ae91f-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ae91f-123">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="ae91f-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="ae91f-124">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="ae91f-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="ae91f-125">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ae91f-125">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="ae91f-126">Description</span><span class="sxs-lookup"><span data-stu-id="ae91f-126">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae91f-127">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="ae91f-127"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="ae91f-128">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ae91f-128">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="ae91f-129">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="ae91f-129"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="ae91f-130">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="ae91f-130">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="ae91f-131">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="ae91f-131"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="ae91f-132">*PhReadKey* 或 *phWriteKey* 參數為 null。</span><span class="sxs-lookup"><span data-stu-id="ae91f-132">The *phReadKey* or *phWriteKey* parameter is null.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="ae91f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae91f-133">Requirements</span></span>



| <span data-ttu-id="ae91f-134">需求</span><span class="sxs-lookup"><span data-stu-id="ae91f-134">Requirement</span></span> | <span data-ttu-id="ae91f-135">值</span><span class="sxs-lookup"><span data-stu-id="ae91f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae91f-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae91f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ae91f-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ae91f-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae91f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ae91f-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ae91f-140">標頭</span><span class="sxs-lookup"><span data-stu-id="ae91f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae91f-141"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae91f-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ae91f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ae91f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae91f-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae91f-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

