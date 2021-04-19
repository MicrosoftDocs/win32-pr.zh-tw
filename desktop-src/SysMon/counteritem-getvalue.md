---
title: CounterItem. GetValue 方法
description: 抓取計數器的最後一個值。
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- GetValue 方法 SysMon
- GetValue 方法 SysMon，CounterItem 類別
- CounterItem 類別 SysMon、GetValue 方法
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999820"
---
# <a name="counteritemgetvalue-method"></a>CounterItem. GetValue 方法

抓取計數器的最後一個值。

## <a name="syntax"></a>語法


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

計數器的上次取樣值。

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

指出值是否有效。



| 值                                                                                              | 意義                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl>                       | 值有效。<br/>     |
| <dl> <dt>0xC0000BBA (3221228474) </dt> </dl> | 值無效。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果計數器資料的來源來自記錄檔，則此值會是記錄檔中的最後一個計數器值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem.GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**CounterItem。值**](counteritem-value.md)
</dt> </dl>

 

 





