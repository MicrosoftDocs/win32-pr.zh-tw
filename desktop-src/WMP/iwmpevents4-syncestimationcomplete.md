---
title: IWMPEvents4 SyncEstimationComplete 方法
description: SyncEstimationComplete 事件會在 IWMPSyncDevice3 estimateSyncSize 之前起始的大小估計完成時發生。
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- SyncEstimationComplete 方法 Windows Media Player
- SyncEstimationComplete 方法 Windows Media Player，IWMPEvents4 介面
- IWMPEvents4 介面 Windows Media Player，SyncEstimationComplete 方法
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681380"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a><span data-ttu-id="7edac-106">IWMPEvents4：： SyncEstimationComplete 方法</span><span class="sxs-lookup"><span data-stu-id="7edac-106">IWMPEvents4::SyncEstimationComplete method</span></span>

<span data-ttu-id="7edac-107">**SyncEstimationComplete** 事件會在先前由 [**IWMPSyncDevice3：： estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)起始的大小估計完成時發生。</span><span class="sxs-lookup"><span data-stu-id="7edac-107">The **SyncEstimationComplete** event occurs when a size estimation, previously initiated by [**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="7edac-108">語法</span><span class="sxs-lookup"><span data-stu-id="7edac-108">Syntax</span></span>


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a><span data-ttu-id="7edac-109">參數</span><span class="sxs-lookup"><span data-stu-id="7edac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7edac-110">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7edac-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7edac-111">[**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)介面的指標，代表起始大小估計的裝置。</span><span class="sxs-lookup"><span data-stu-id="7edac-111">Pointer to the [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) interface that represents the device for which the size estimation was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="7edac-112">*hrResult* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7edac-112">*hrResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7edac-113">值，指出估計的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="7edac-113">A value that indicates the success or failure of the estimation.</span></span>



| <span data-ttu-id="7edac-114">值</span><span class="sxs-lookup"><span data-stu-id="7edac-114">Value</span></span>                                                                                                                                       | <span data-ttu-id="7edac-115">意義</span><span class="sxs-lookup"><span data-stu-id="7edac-115">Meaning</span></span>                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="7edac-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7edac-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7edac-117">估計成功。</span><span class="sxs-lookup"><span data-stu-id="7edac-117">The estimation succeeded.</span></span><br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <span data-ttu-id="7edac-118"><dt>**E \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="7edac-118"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="7edac-119">估計已中止。</span><span class="sxs-lookup"><span data-stu-id="7edac-119">The estimation was aborted.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7edac-120">*lEstimatedUsedSpace* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7edac-120">*lEstimatedUsedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7edac-121">將在裝置上使用的預估空間 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="7edac-121">The estimated space (in bytes) that would be used on the device.</span></span>

</dd> <dt>

<span data-ttu-id="7edac-122">*lEstimatedSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7edac-122">*lEstimatedSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7edac-123">估計的大小 (以位元組為單位) 要同步處理的資料。</span><span class="sxs-lookup"><span data-stu-id="7edac-123">The estimated size (in bytes) of the data to be synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7edac-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="7edac-124">Return value</span></span>

<span data-ttu-id="7edac-125">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7edac-125">This method does not return a value.</span></span>

## <a name="see-also"></a><span data-ttu-id="7edac-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7edac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7edac-127">**IWMPEvents4 介面**</span><span class="sxs-lookup"><span data-stu-id="7edac-127">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[<span data-ttu-id="7edac-128">**IWMPSyncDevice3::estimateSyncSize**</span><span class="sxs-lookup"><span data-stu-id="7edac-128">**IWMPSyncDevice3::estimateSyncSize**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





