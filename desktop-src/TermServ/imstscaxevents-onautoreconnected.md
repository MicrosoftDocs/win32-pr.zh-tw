---
title: IMsTscAxEvents OnAutoReconnected 方法
description: 當用戶端控制項自動重新連接到遠端會話時呼叫。 |IMsTscAxEvents OnAutoReconnected 方法
ms.assetid: 50307002-33F9-453C-A880-AF4111412854
ms.tgt_platform: multiple
keywords:
- OnAutoReconnected 方法遠端桌面服務
- OnAutoReconnected 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAutoReconnected 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29f0e9a498a727614bdfda621c214199918e2ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106975627"
---
# <a name="imstscaxeventsonautoreconnected-method"></a>IMsTscAxEvents：： OnAutoReconnected 方法

當用戶端控制項自動重新連接到遠端會話時呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT OnAutoReconnected();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

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

 

 





