---
description: 表示處理重複事件的事件種類類別。
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: ObHandleDuplicateEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973716"
---
# <a name="obhandleduplicateevent-class"></a>ObHandleDuplicateEvent 類別

表示處理重複事件的事件種類類別。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a>成員

**ObHandleDuplicateEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ObHandleDuplicateEvent** 類別具有這些屬性。

<dl> <dt>

**Object**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**指標**](event-tracing-mof-qualifiers.md)， [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) 
</dt> </dl>

物件。

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (5) 
</dt> </dl>

物件類型。

</dd> <dt>

**SourceHandle**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) 
</dt> </dl>

來源物件的控制碼。

</dd> <dt>

**TargetHandle**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) 
</dt> </dl>

目標物件的控制碼。

</dd> <dt>

**TargetProcessId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) 
</dt> </dl>

目標的處理序識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore mof</dt> </dl> |



 

 




