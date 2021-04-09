---
title: 'TriggerCollection 物件 (]) '
description: 腳本物件，用來新增、移除及取出工作的觸發程式。
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- 觸發程式工作排程器，觸發程式集合物件
- TriggerCollection 物件工作排程器
- TriggerCollection 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094223"
---
# <a name="triggercollection-object"></a>TriggerCollection 物件

腳本物件，用來新增、移除及取出工作的觸發程式。

## <a name="members"></a>成員

**TriggerCollection** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**TriggerCollection** 物件有這些方法。



| 方法                                     | 描述                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**清楚**](triggercollection-clear.md)   | 清除集合中的所有觸發程式。<br/>                                        |
| [**建立**](triggercollection-create.md) | 為工作建立新的觸發程式。<br/>                                             |
| [**移除**](triggercollection-remove.md) | 從工作所用的觸發程式集合中移除指定的觸發程式。<br/> |



 

### <a name="properties"></a>屬性

**TriggerCollection** 物件具有這些屬性。



| 屬性                                            | 存取類型          | Description                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**計數**](triggercollection-count.md)<br/> | 唯讀<br/> | 取得集合中的觸發程式數目。<br/>  |
| [**項目**](triggercollection-item.md)<br/>   | 唯讀<br/> | 從集合中取得指定的觸發程式。<br/> |



 

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，工作的觸發程式會在工作排程器架構的 [**觸發**](taskschedulerschema-triggers-tasktype-element.md) 程式元素中指定。

如需每個觸發程式類型的詳細資訊，請參閱 [觸發程式類型](trigger-types.md)。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>App.xaml.。h</dt> </dl> |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**觸發**](trigger.md)
</dt> </dl>

 

 





