---
title: TaskNamedValuePair 物件
description: 用來建立名稱/值組的腳本物件，其名稱與值相關聯。
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- TaskNamedValuePair 物件工作排程器
- TaskNamedValuePair 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965477"
---
# <a name="tasknamedvaluepair-object"></a>TaskNamedValuePair 物件

用來建立名稱/值組的腳本物件，其名稱與值相關聯。

## <a name="members"></a>成員

**TaskNamedValuePair** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TaskNamedValuePair** 物件具有這些屬性。



| 屬性                                             | 描述                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Name**](tasknamedvaluepair-name.md)<br/>   | 取得或設定與名稱/值配對中的值相關聯的名稱。<br/> |
| [**值**](tasknamedvaluepair-value.md)<br/> | 取得或設定與名稱/值配對中的名稱相關聯的值。<br/> |



 

## <a name="remarks"></a>備註

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) 元素來指定名稱/值組。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TaskNamedValueCollection**](tasknamedvaluecollection.md)
</dt> </dl>

 

 





