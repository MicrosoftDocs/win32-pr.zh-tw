---
title: 'INapSystemHealthAgentCallback CompareSoHRequests 方法 (NapSystemHealthAgent .h) '
description: SHA 用來比較 SoH 要求。
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- CompareSoHRequests 方法 NAP
- CompareSoHRequests 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，CompareSoHRequests 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966509"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a><span data-ttu-id="97ceb-106">INapSystemHealthAgentCallback：： CompareSoHRequests 方法</span><span class="sxs-lookup"><span data-stu-id="97ceb-106">INapSystemHealthAgentCallback::CompareSoHRequests method</span></span>

> [!Note]  
> <span data-ttu-id="97ceb-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="97ceb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="97ceb-108">SHA 會使用 **INapSystemHealthAgentCallback：： CompareSoHRequests** 方法來比較 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="97ceb-108">The **INapSystemHealthAgentCallback::CompareSoHRequests** method is used by the SHA to compare SoH requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="97ceb-109">語法</span><span class="sxs-lookup"><span data-stu-id="97ceb-109">Syntax</span></span>


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a><span data-ttu-id="97ceb-110">參數</span><span class="sxs-lookup"><span data-stu-id="97ceb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97ceb-111">*lhs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97ceb-111">*lhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97ceb-112">比較作業左邊的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 指標。</span><span class="sxs-lookup"><span data-stu-id="97ceb-112">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the left of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="97ceb-113">*rhs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97ceb-113">*rhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97ceb-114">比較作業右邊 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 的指標。</span><span class="sxs-lookup"><span data-stu-id="97ceb-114">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the right of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="97ceb-115">*isEqual* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="97ceb-115">*isEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97ceb-116">**布林** 值的指標，如果 *lhs* 和 *rhs* 語義相等，則為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="97ceb-116">A pointer to a **BOOL** that is **TRUE** if *lhs* and *rhs* are semantically equal, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97ceb-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="97ceb-117">Return value</span></span>

<span data-ttu-id="97ceb-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="97ceb-118">This method can return one of these values.</span></span>



| <span data-ttu-id="97ceb-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="97ceb-119">Return code</span></span>                                                                               | <span data-ttu-id="97ceb-120">Description</span><span class="sxs-lookup"><span data-stu-id="97ceb-120">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="97ceb-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="97ceb-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="97ceb-122">表示成功。</span><span class="sxs-lookup"><span data-stu-id="97ceb-122">Indicates success.</span></span><br/>                         |
| <dl> <span data-ttu-id="97ceb-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="97ceb-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="97ceb-124">方法不是由 SHA 所執行。</span><span class="sxs-lookup"><span data-stu-id="97ceb-124">The method was not implemented by the SHA.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="97ceb-125">備註</span><span class="sxs-lookup"><span data-stu-id="97ceb-125">Remarks</span></span>

<span data-ttu-id="97ceb-126">此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。</span><span class="sxs-lookup"><span data-stu-id="97ceb-126">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="97ceb-127">SHA 應比較 Soh，如果 Soh 是語義相等，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="97ceb-127">The SHA should compare the SoHs and return **TRUE** if the SoHs are semantically equal.</span></span> <span data-ttu-id="97ceb-128">NapAgent 會使用此資訊來判斷是否因為用戶端電腦的狀態變更而應起始 SoH 交換。</span><span class="sxs-lookup"><span data-stu-id="97ceb-128">The NapAgent uses this information to determine if an SoH exchange should be initiated due to change of state of the client machine.</span></span>

<span data-ttu-id="97ceb-129">如果 Sha 將遞增識別碼或時間戳記放入 SoH，則 Soh 可能會有語義相等 (亦即，它們可能會傳達相同的健康情況資訊) ，但它們可能是位元組的不相等。</span><span class="sxs-lookup"><span data-stu-id="97ceb-129">If SHAs have put incremental IDs or time-stamps into their SoH, then SoHs may be semantically equal (i.e. they may convey the same health information), but they may be byte-wise unequal.</span></span> <span data-ttu-id="97ceb-130">Sha 應該會執行此函式來檢查 Soh 是否有語義相等。</span><span class="sxs-lookup"><span data-stu-id="97ceb-130">SHAs should implement this function to check for semantic equality of SoHs.</span></span>

<span data-ttu-id="97ceb-131">如果 Sha 未在其 Soh 中放入任何時間戳記或識別碼，他們可能會選擇不執行此函式並傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="97ceb-131">If SHAs have not put any time-stamps or Ids into their SoHs, they may choose to not implement this function and return **E\_NOTIMPL**.</span></span> <span data-ttu-id="97ceb-132">在此情況下，NapAgent 會對 [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh)執行位元組取向的比較。</span><span class="sxs-lookup"><span data-stu-id="97ceb-132">In this case, the NapAgent performs a byte-wise comparison on the [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="requirements"></a><span data-ttu-id="97ceb-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="97ceb-133">Requirements</span></span>



| <span data-ttu-id="97ceb-134">需求</span><span class="sxs-lookup"><span data-stu-id="97ceb-134">Requirement</span></span> | <span data-ttu-id="97ceb-135">值</span><span class="sxs-lookup"><span data-stu-id="97ceb-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97ceb-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97ceb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="97ceb-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97ceb-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="97ceb-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97ceb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="97ceb-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97ceb-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="97ceb-140">標頭</span><span class="sxs-lookup"><span data-stu-id="97ceb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ceb-141"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="97ceb-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="97ceb-142">Idl</span><span class="sxs-lookup"><span data-stu-id="97ceb-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97ceb-143"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="97ceb-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ceb-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97ceb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ceb-145">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="97ceb-145">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> <dt>

[<span data-ttu-id="97ceb-146">**SoH**</span><span class="sxs-lookup"><span data-stu-id="97ceb-146">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





