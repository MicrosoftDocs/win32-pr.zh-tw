---
description: 設定預設功能的喜好設定。
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'IH323LineEx：： SetDefaultCapabilityPreferrence 方法 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994220"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a><span data-ttu-id="aa259-103">IH323LineEx：： SetDefaultCapabilityPreferrence 方法</span><span class="sxs-lookup"><span data-stu-id="aa259-103">IH323LineEx::SetDefaultCapabilityPreferrence method</span></span>

<span data-ttu-id="aa259-104">\[**SetDefaultCapabilityPreferrence** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="aa259-104">\[**SetDefaultCapabilityPreferrence** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aa259-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="aa259-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="aa259-106">**SetDefaultCapabilityPreferrence** 方法會設定預設功能的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="aa259-106">The **SetDefaultCapabilityPreferrence** method configures the preference of the default capabilities.</span></span> <span data-ttu-id="aa259-107">功能的預設權數為100。</span><span class="sxs-lookup"><span data-stu-id="aa259-107">Capabilities have a default weight of 100.</span></span> <span data-ttu-id="aa259-108">如果應用程式為功能指定較高的權數，則在 h.264 協商期間會有較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="aa259-108">If the application specifies a higher weight for a capability, it will have a higher priority during the H.245 negotiation.</span></span> <span data-ttu-id="aa259-109">如果應用程式將功能的權數設定為0，它就不會用於 h. 協商。</span><span class="sxs-lookup"><span data-stu-id="aa259-109">If the application sets the weight of a capability to 0, it will not be used in the H.245 negotiation.</span></span>

<span data-ttu-id="aa259-110">這個方法是累計的。</span><span class="sxs-lookup"><span data-stu-id="aa259-110">This method is cumulative.</span></span> <span data-ttu-id="aa259-111">例如，如果第一次呼叫此方法來停用功能，並再次呼叫以停用另一項功能，則這兩個功能會因為這兩個呼叫的結果而停用。</span><span class="sxs-lookup"><span data-stu-id="aa259-111">For example, if this method is called first to disable a capability and is called again to disable another, both capabilities will be disabled as the result of these two calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa259-112">語法</span><span class="sxs-lookup"><span data-stu-id="aa259-112">Syntax</span></span>


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="aa259-113">參數</span><span class="sxs-lookup"><span data-stu-id="aa259-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa259-114">*dwNumCaps* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa259-114">*dwNumCaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa259-115">**DWORD** 值，包含使用此方法設定的功能數目。</span><span class="sxs-lookup"><span data-stu-id="aa259-115">A **DWORD** value that contains the number of capabilities set with this method.</span></span>

</dd> <dt>

<span data-ttu-id="aa259-116">*pCapabilities* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa259-116">*pCapabilities* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa259-117">功能陣列。</span><span class="sxs-lookup"><span data-stu-id="aa259-117">An array of capabilities.</span></span> <span data-ttu-id="aa259-118">陣列的每個元素都是 [**H245 \_ 功能**](h245-capability.md) 值。</span><span class="sxs-lookup"><span data-stu-id="aa259-118">Each element of the array is an [**H245\_CAPABILITY**](h245-capability.md) value.</span></span>

</dd> <dt>

<span data-ttu-id="aa259-119">*pWeights* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa259-119">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa259-120">與功能相關聯的加權陣列。</span><span class="sxs-lookup"><span data-stu-id="aa259-120">An array of weights associated with the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa259-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa259-121">Return value</span></span>

<span data-ttu-id="aa259-122">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="aa259-122">This method can return one of these values.</span></span>



| <span data-ttu-id="aa259-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="aa259-123">Return code</span></span>                                                                                   | <span data-ttu-id="aa259-124">Description</span><span class="sxs-lookup"><span data-stu-id="aa259-124">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa259-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="aa259-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aa259-126">方法成功。</span><span class="sxs-lookup"><span data-stu-id="aa259-126">Method succeeded.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="aa259-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="aa259-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aa259-128">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="aa259-128">Insufficient memory exists to perform the operation.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="aa259-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aa259-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="aa259-130">*PCapabilities* 參數為 **Null**，或 *pWeights* 參數為 **null**，或 *pCapabilities* 和 *PWeights* 都是 **null**，或 pCapabilities 陣列包含不正確 h. 功能物件。</span><span class="sxs-lookup"><span data-stu-id="aa259-130">The *pCapabilities* parameter is **NULL**, or the *pWeights* parameter is **NULL**, or both *pCapabilities* and *pWeights* are **NULL**, or the pCapabilities array contains an invalid H.245 capability object.</span></span><br/> |
| <dl> <span data-ttu-id="aa259-131"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="aa259-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="aa259-132">無法讀取 *pWeights* 陣列的元素或 *pCapabilities* 陣列的元素。</span><span class="sxs-lookup"><span data-stu-id="aa259-132">Unable to read an element of the *pWeights* array or an element of the *pCapabilities* array.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="aa259-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa259-133">Requirements</span></span>



| <span data-ttu-id="aa259-134">需求</span><span class="sxs-lookup"><span data-stu-id="aa259-134">Requirement</span></span> | <span data-ttu-id="aa259-135">值</span><span class="sxs-lookup"><span data-stu-id="aa259-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa259-136">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="aa259-136">TAPI version</span></span><br/> | <span data-ttu-id="aa259-137">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="aa259-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="aa259-138">標頭</span><span class="sxs-lookup"><span data-stu-id="aa259-138">Header</span></span><br/>       | <dl> <span data-ttu-id="aa259-139"><dt>H323priv。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa259-139"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="aa259-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="aa259-140">Library</span></span><br/>      | <dl> <span data-ttu-id="aa259-141"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="aa259-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="aa259-142">DLL</span><span class="sxs-lookup"><span data-stu-id="aa259-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="aa259-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa259-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




