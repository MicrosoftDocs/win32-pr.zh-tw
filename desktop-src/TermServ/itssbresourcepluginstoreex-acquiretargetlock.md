---
title: ITsSbResourcePluginStoreEx AcquireTargetLock 方法
description: 鎖定目標。
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- AcquireTargetLock 方法遠端桌面服務
- AcquireTargetLock 方法遠端桌面服務，ITsSbResourcePluginStoreEx 介面
- ITsSbResourcePluginStoreEx 介面遠端桌面服務，AcquireTargetLock 方法
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094104"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a><span data-ttu-id="49b11-106">ITsSbResourcePluginStoreEx：： AcquireTargetLock 方法</span><span class="sxs-lookup"><span data-stu-id="49b11-106">ITsSbResourcePluginStoreEx::AcquireTargetLock method</span></span>

<span data-ttu-id="49b11-107">鎖定目標。</span><span class="sxs-lookup"><span data-stu-id="49b11-107">Locks a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b11-108">語法</span><span class="sxs-lookup"><span data-stu-id="49b11-108">Syntax</span></span>


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a><span data-ttu-id="49b11-109">參數</span><span class="sxs-lookup"><span data-stu-id="49b11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49b11-110">*targetName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49b11-110">*targetName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49b11-111">要鎖定之目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="49b11-111">The name of the target to lock.</span></span>

</dd> <dt>

<span data-ttu-id="49b11-112">*dwTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49b11-112">*dwTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49b11-113">作業的執行時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="49b11-113">The timeout for the operation, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="49b11-114">*ppCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="49b11-114">*ppContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49b11-115">傳回鎖定內容的指標。</span><span class="sxs-lookup"><span data-stu-id="49b11-115">Returns a pointer to the context of the lock.</span></span> <span data-ttu-id="49b11-116">若要釋放鎖定，請提供此指標給 [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) 方法。</span><span class="sxs-lookup"><span data-stu-id="49b11-116">To release the lock, supply this pointer to the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49b11-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="49b11-117">Return value</span></span>

<span data-ttu-id="49b11-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="49b11-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49b11-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="49b11-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49b11-120">備註</span><span class="sxs-lookup"><span data-stu-id="49b11-120">Remarks</span></span>

<span data-ttu-id="49b11-121">取得鎖定之後，會假設呼叫的執行緒具有目標物件的獨佔存取權，因此不會在同一部機器內 (其他執行緒) 可以更新它。</span><span class="sxs-lookup"><span data-stu-id="49b11-121">After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it.</span></span> <span data-ttu-id="49b11-122">因此，呼叫的執行緒必須在對目標物件進行必要的更新時，立即呼叫 [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) 方法。</span><span class="sxs-lookup"><span data-stu-id="49b11-122">Therefore the calling thread must call the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method as soon as it has made the necessary updates to the target object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49b11-123">如果部署中有一個以上的連接代理程式，此鎖定並不會完全防止外部修改目標物件。</span><span class="sxs-lookup"><span data-stu-id="49b11-123">this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment.</span></span> <span data-ttu-id="49b11-124">呼叫執行緒必須做好準備，才能正常地處理失敗，然後重試目標更新。</span><span class="sxs-lookup"><span data-stu-id="49b11-124">The calling thread must be prepared to handle a failure gracefully and retry the target update.</span></span>

 

<span data-ttu-id="49b11-125">此方法可在已安裝 [KB3091411](https://support.microsoft.com/kb/3091411) 的 Windows Server 2012 R2 上使用，並安裝在 [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) 介面中。</span><span class="sxs-lookup"><span data-stu-id="49b11-125">This method is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="49b11-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="49b11-126">Requirements</span></span>



| <span data-ttu-id="49b11-127">需求</span><span class="sxs-lookup"><span data-stu-id="49b11-127">Requirement</span></span> | <span data-ttu-id="49b11-128">值</span><span class="sxs-lookup"><span data-stu-id="49b11-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="49b11-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49b11-129">Minimum supported client</span></span><br/> | <span data-ttu-id="49b11-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="49b11-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="49b11-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49b11-131">Minimum supported server</span></span><br/> | <span data-ttu-id="49b11-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="49b11-132">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="49b11-133">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="49b11-133">End of server support</span></span><br/>    | <span data-ttu-id="49b11-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="49b11-134">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="49b11-135">Idl</span><span class="sxs-lookup"><span data-stu-id="49b11-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49b11-136"><dt>SbTsV .idl</dt></span><span class="sxs-lookup"><span data-stu-id="49b11-136"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="49b11-137">IID</span><span class="sxs-lookup"><span data-stu-id="49b11-137">IID</span></span><br/>                      | <span data-ttu-id="49b11-138">IID \_ ITsSbResourcePluginStoreEx 定義為80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="49b11-138">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49b11-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49b11-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b11-140">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="49b11-140">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





