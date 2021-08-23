---
title: IRemoteDesktopClientEvents OnNetworkStatusChanged 方法
description: 在網路狀態變更時呼叫。 |IRemoteDesktopClientEvents OnNetworkStatusChanged 方法
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- OnNetworkStatusChanged 方法遠端桌面服務
- OnNetworkStatusChanged 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnNetworkStatusChanged 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d14519f5da78a0d42b5bd7e52abf790c21406bfe20848235d2639beed2e215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515108"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>IRemoteDesktopClientEvents：： OnNetworkStatusChanged 方法

在網路狀態變更時呼叫。

## <a name="syntax"></a>語法


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*qualityLevel* \[在\]
</dt> <dd>

連接的新品質層級。 品質層級取決於頻寬和來回行程時間 (rtt) 值。

下列其中一個值。



| 值                                                                        | 意義                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 無法判斷品質層級。<br/>       |
| <dl> <dt>1</dt> </dl> | 連接品質很差 (一個橫條) 。<br/>        |
| <dl> <dt>2</dt> </dl> | 連接品質相當 (兩個橫條) 。<br/>       |
| <dl> <dt>3</dt> </dl> | 連接品質很適合 (三個橫條) 。<br/>     |
| <dl> <dt>4</dt> </dl> | 連接品質很棒 (四個橫條) 。<br/> |



 

</dd> <dt>

*頻寬* \[在\]
</dt> <dd>

指定新的連接頻寬，以 kb/秒為單位 (Kbps) 。

</dd> <dt>

*rtt* \[在\]
</dt> <dd>

指定新的連接往返時間 (延遲) （以毫秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                           |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                 |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





