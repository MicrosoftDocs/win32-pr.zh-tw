---
title: IMsTscAxEvents OnDevicesButtonPressed 方法
description: 當按下連接列中的 [裝置] 按鈕時呼叫。
ms.assetid: E2B1780F-EDD9-4C11-A887-10586145240E
ms.tgt_platform: multiple
keywords:
- OnDevicesButtonPressed 方法遠端桌面服務
- OnDevicesButtonPressed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnDevicesButtonPressed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDevicesButtonPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7846dfefa7d093e52cad58fa13335a6b633c82b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508376"
---
# <a name="imstscaxeventsondevicesbuttonpressed-method"></a>IMsTscAxEvents：： OnDevicesButtonPressed 方法

當按下連接列中的 [裝置] 按鈕時呼叫。

## <a name="syntax"></a>語法


```C++
void OnDevicesButtonPressed();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當用戶端和伺服器上同時啟用 USB 重新導向時，[裝置] 按鈕會顯示在連接列中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





