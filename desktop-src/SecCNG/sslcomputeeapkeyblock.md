---
description: 計算可延伸驗證通訊協定所使用的金鑰區塊 (EAP) 。
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: 'SslComputeEapKeyBlock 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988748"
---
# <a name="sslcomputeeapkeyblock-function"></a><span data-ttu-id="a08b6-103">SslComputeEapKeyBlock 函式</span><span class="sxs-lookup"><span data-stu-id="a08b6-103">SslComputeEapKeyBlock function</span></span>

<span data-ttu-id="a08b6-104">**SslComputeEapKeyBlock** 函式會計算可延伸驗證通訊協定所使用的金鑰區塊 (EAP) 。</span><span class="sxs-lookup"><span data-stu-id="a08b6-104">The **SslComputeEapKeyBlock** function computes the key block used by the Extensible Authentication Protocol (EAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="a08b6-105">語法</span><span class="sxs-lookup"><span data-stu-id="a08b6-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a08b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="a08b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08b6-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b6-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a08b6-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="a08b6-109">*hMasterKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b6-110">[*主要金鑰*](/windows/desktop/SecGloss/m-gly)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a08b6-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="a08b6-111">*pbRandoms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-111">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b6-112">緩衝區的指標，其中包含 SSL 會話的用戶端 \_ 隨機和伺服器 \_ 隨機值串連。</span><span class="sxs-lookup"><span data-stu-id="a08b6-112">A pointer to a buffer that contains a concatenation of the client\_random and server\_random values of the SSL session.</span></span>

</dd> <dt>

<span data-ttu-id="a08b6-113">*cbRandoms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-113">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b6-114">*PbRandoms* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a08b6-114">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a08b6-115">*pbOutput* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-115">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b6-116">接收金鑰 BLOB 的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="a08b6-116">The address of a buffer that receives the key BLOB.</span></span> <span data-ttu-id="a08b6-117">*CbOutput* 參數包含這個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="a08b6-117">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="a08b6-118">如果此參數為 **Null**，此函式會將所需的大小（以位元組為單位）放在 *pcbResult* 參數所指向的 **DWORD** 中。</span><span class="sxs-lookup"><span data-stu-id="a08b6-118">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a08b6-119">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-119">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b6-120">*PbOutput* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a08b6-120">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a08b6-121">*pcbResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-121">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b6-122">**DWORD** 值的指標，指定寫入至 *pbOutput* 緩衝區之雜湊的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a08b6-122">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a08b6-123">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08b6-124">設定為 **NCRYPT \_ SSL \_ 伺服器 \_ 旗** 標，表示這是伺服器呼叫。</span><span class="sxs-lookup"><span data-stu-id="a08b6-124">Set to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08b6-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="a08b6-125">Return value</span></span>

<span data-ttu-id="a08b6-126">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a08b6-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="a08b6-127">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="a08b6-127">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="a08b6-128">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="a08b6-128">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="a08b6-129">Description</span><span class="sxs-lookup"><span data-stu-id="a08b6-129">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a08b6-130">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="a08b6-130"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="a08b6-131">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="a08b6-131">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a08b6-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="a08b6-132">Requirements</span></span>



| <span data-ttu-id="a08b6-133">需求</span><span class="sxs-lookup"><span data-stu-id="a08b6-133">Requirement</span></span> | <span data-ttu-id="a08b6-134">值</span><span class="sxs-lookup"><span data-stu-id="a08b6-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08b6-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a08b6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a08b6-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-136">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a08b6-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a08b6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a08b6-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a08b6-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a08b6-139">標頭</span><span class="sxs-lookup"><span data-stu-id="a08b6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a08b6-140"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="a08b6-140"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="a08b6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a08b6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a08b6-142"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a08b6-142"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

