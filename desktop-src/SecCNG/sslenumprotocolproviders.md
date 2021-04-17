---
description: 傳回已安裝安全通訊端層通訊協定 (SSL) 通訊協定提供者的陣列。
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: 'SslEnumProtocolProviders 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195249"
---
# <a name="sslenumprotocolproviders-function"></a><span data-ttu-id="f0b77-103">SslEnumProtocolProviders 函式</span><span class="sxs-lookup"><span data-stu-id="f0b77-103">SslEnumProtocolProviders function</span></span>

<span data-ttu-id="f0b77-104">**SslEnumProtocolProviders** 函式會傳回已安裝 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者的陣列。</span><span class="sxs-lookup"><span data-stu-id="f0b77-104">The **SslEnumProtocolProviders** function returns an array of installed [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b77-105">語法</span><span class="sxs-lookup"><span data-stu-id="f0b77-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f0b77-106">參數</span><span class="sxs-lookup"><span data-stu-id="f0b77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b77-107">*pdwProviderCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f0b77-107">*pdwProviderCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b77-108">**DWORD** 值的指標，用來接收傳回的通訊協定提供者數目。</span><span class="sxs-lookup"><span data-stu-id="f0b77-108">A pointer to a **DWORD** value to receive the number of protocol providers returned.</span></span>

</dd> <dt>

<span data-ttu-id="f0b77-109">*ppProviderList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f0b77-109">*ppProviderList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b77-110">接收 [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) 結構陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="f0b77-110">A pointer to a buffer that receives the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures.</span></span>

</dd> <dt>

<span data-ttu-id="f0b77-111">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0b77-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b77-112">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="f0b77-112">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b77-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0b77-113">Return value</span></span>

<span data-ttu-id="f0b77-114">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f0b77-114">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="f0b77-115">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="f0b77-115">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="f0b77-116">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="f0b77-116">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f0b77-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f0b77-117">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="f0b77-118">Description</span><span class="sxs-lookup"><span data-stu-id="f0b77-118">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0b77-119">不 <dt>**超過 \_錯誤的 \_ 旗標**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="f0b77-119"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="f0b77-120">*DwFlags* 參數不是零。</span><span class="sxs-lookup"><span data-stu-id="f0b77-120">The *dwFlags* parameter is not zero.</span></span><br/>                              |
| <dl> <span data-ttu-id="f0b77-121">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="f0b77-121"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="f0b77-122">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f0b77-122">Not enough memory is available to allocate necessary buffers.</span></span><br/>     |
| <dl> <span data-ttu-id="f0b77-123">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="f0b77-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="f0b77-124">*PdwProviderCount* 或 *PpProviderList* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f0b77-124">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0b77-125">備註</span><span class="sxs-lookup"><span data-stu-id="f0b77-125">Remarks</span></span>

<span data-ttu-id="f0b77-126">當您完成使用 [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) 結構的陣列時，請呼叫 [**SslFreeBuffer**](sslfreebuffer.md) 函數來釋放陣列。</span><span class="sxs-lookup"><span data-stu-id="f0b77-126">When you have finished using the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures, call the [**SslFreeBuffer**](sslfreebuffer.md) function to free the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b77-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0b77-127">Requirements</span></span>



| <span data-ttu-id="f0b77-128">需求</span><span class="sxs-lookup"><span data-stu-id="f0b77-128">Requirement</span></span> | <span data-ttu-id="f0b77-129">值</span><span class="sxs-lookup"><span data-stu-id="f0b77-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b77-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0b77-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b77-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0b77-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f0b77-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0b77-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b77-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0b77-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f0b77-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f0b77-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0b77-135"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b77-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="f0b77-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f0b77-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0b77-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0b77-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

