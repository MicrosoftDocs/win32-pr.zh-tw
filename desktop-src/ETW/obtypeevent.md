---
description: 表示與資料收集開始和結束相關之物件類型事件的事件種類類別。
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: ObTypeEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115765"
---
# <a name="obtypeevent-class"></a>ObTypeEvent 類別

表示與資料收集開始和結束相關之物件類型事件的事件種類類別。 此事件牽涉到型別索引值與型別名稱的對應。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a>成員

**ObTypeEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ObTypeEvent** 類別具有這些屬性。

<dl> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) 
</dt> </dl>

物件類型。

</dd> <dt>

**已保留**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) 
</dt> </dl>

保留的。

</dd> <dt>

**TypeName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "w" ) 、 [**StringTermination**](event-tracing-mof-qualifiers.md) ( "NullTerminated" ) 、 [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) 
</dt> </dl>

類型名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore mof</dt> </dl> |



 

 




