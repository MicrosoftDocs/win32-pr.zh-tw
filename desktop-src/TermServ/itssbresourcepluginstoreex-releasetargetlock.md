---
title: ITsSbResourcePluginStoreEx ReleaseTargetLock 方法
description: 釋放目標的鎖定。
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- ReleaseTargetLock 方法遠端桌面服務
- ReleaseTargetLock 方法遠端桌面服務，ITsSbResourcePluginStoreEx 介面
- ITsSbResourcePluginStoreEx 介面遠端桌面服務，ReleaseTargetLock 方法
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104298"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a><span data-ttu-id="c6153-106">ITsSbResourcePluginStoreEx：： ReleaseTargetLock 方法</span><span class="sxs-lookup"><span data-stu-id="c6153-106">ITsSbResourcePluginStoreEx::ReleaseTargetLock method</span></span>

<span data-ttu-id="c6153-107">釋放目標的鎖定。</span><span class="sxs-lookup"><span data-stu-id="c6153-107">Releases a lock on a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6153-108">語法</span><span class="sxs-lookup"><span data-stu-id="c6153-108">Syntax</span></span>


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="c6153-109">參數</span><span class="sxs-lookup"><span data-stu-id="c6153-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6153-110">*pCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6153-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6153-111">[**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)方法所傳回之內容的指標。</span><span class="sxs-lookup"><span data-stu-id="c6153-111">A pointer to the context returned by the [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6153-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6153-112">Return value</span></span>

<span data-ttu-id="c6153-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c6153-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6153-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c6153-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6153-115">備註</span><span class="sxs-lookup"><span data-stu-id="c6153-115">Remarks</span></span>

<span data-ttu-id="c6153-116">只有在已安裝 [KB3091411](https://support.microsoft.com/kb/3091411) 的 Windows Server 2012 R2 上，才可在 [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) 介面中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="c6153-116">This method is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span> <span data-ttu-id="c6153-117">從 Windows Server 2016 開始， [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) 介面上可以使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="c6153-117">This method is available on the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface starting with Windows Server 2016.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6153-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6153-118">Requirements</span></span>



| <span data-ttu-id="c6153-119">需求</span><span class="sxs-lookup"><span data-stu-id="c6153-119">Requirement</span></span> | <span data-ttu-id="c6153-120">值</span><span class="sxs-lookup"><span data-stu-id="c6153-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6153-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6153-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c6153-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="c6153-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c6153-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6153-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c6153-124">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c6153-124">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="c6153-125">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c6153-125">End of server support</span></span><br/>    | <span data-ttu-id="c6153-126">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c6153-126">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="c6153-127">Idl</span><span class="sxs-lookup"><span data-stu-id="c6153-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6153-128"><dt>SbTsV .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6153-128"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="c6153-129">IID</span><span class="sxs-lookup"><span data-stu-id="c6153-129">IID</span></span><br/>                      | <span data-ttu-id="c6153-130">IID \_ ITsSbResourcePluginStoreEx 定義為80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="c6153-130">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6153-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6153-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6153-132">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="c6153-132">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





