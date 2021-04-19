---
description: SendNMEvent 方法會將事件提交給 Windows Management Instrumentation (WMI) 。
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'IMonitorEventer：： SendNMEvent 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988679"
---
# <a name="imonitoreventersendnmevent-method"></a>IMonitorEventer：： SendNMEvent 方法

**SendNMEvent** 方法會將事件提交給 WINDOWS MANAGEMENT INSTRUMENTATION (WMI) 。

## <a name="syntax"></a>語法


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNMEventData* \[在\]
</dt> <dd>

提交至 WMI 的事件指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK。

如果此方法不成功，傳回值就會 \_ 從記憶體中 NMERR 出來 \_ \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




