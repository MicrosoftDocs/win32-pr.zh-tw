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
# <a name="iwmpevents4syncestimationcomplete-method"></a>IWMPEvents4：： SyncEstimationComplete 方法

**SyncEstimationComplete** 事件會在先前由 [**IWMPSyncDevice3：： estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)起始的大小估計完成時發生。

## <a name="syntax"></a>語法


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

[**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)介面的指標，代表起始大小估計的裝置。

</dd> <dt>

*hrResult* \[在\]
</dt> <dd>

值，指出估計的成功或失敗。



| 值                                                                                                                                       | 意義                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ 確定**</dt> </dl>          | 估計成功。<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**E \_ 中止**</dt> </dl> | 估計已中止。<br/> |



 

</dd> <dt>

*lEstimatedUsedSpace* \[在\]
</dt> <dd>

將在裝置上使用的預估空間 (位元組) 。

</dd> <dt>

*lEstimatedSize* \[在\]
</dt> <dd>

估計的大小 (以位元組為單位) 要同步處理的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPEvents4 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





