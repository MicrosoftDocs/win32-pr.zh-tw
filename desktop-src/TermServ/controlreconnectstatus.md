---
title: ControlReconnectStatus 列舉
description: 指定 IMsRdpClient8 Reconnect 方法的結果。
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- ControlReconnectStatus 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966291"
---
# <a name="controlreconnectstatus-enumeration"></a>ControlReconnectStatus 列舉

指定 [**IMsRdpClient8：： Reconnect**](imsrdpclient8-reconnect.md) 方法的結果。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**
</dt> <dd>

重新連接作業已啟動。

</dd> <dt>

<span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**
</dt> <dd>

無法啟動重新連接操作。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient8：： Reconnect**](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





