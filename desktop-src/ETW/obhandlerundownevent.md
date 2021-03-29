---
description: 表示與資料收集開始和結束相關之物件控制碼事件的事件種類類別。
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: ObHandleRundownEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973432"
---
# <a name="obhandlerundownevent-class"></a>ObHandleRundownEvent 類別

表示與資料收集開始和結束相關之物件控制碼事件的事件種類類別。 此事件涉及在執行取消時列舉所有控制碼。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a>成員

**ObHandleRundownEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ObHandleRundownEvent** 類別具有這些屬性。

<dl> <dt>

**Handle**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) 
</dt> </dl>

物件控制碼。

</dd> <dt>

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

**ObjectName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "w" ) 、 [**StringTermination**](event-tracing-mof-qualifiers.md) ( "NullTerminated" ) 、 [**WmiDataId**](event-tracing-mof-qualifiers.md) (5) 
</dt> </dl>

物件名稱。

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) 
</dt> </dl>

物件類型。

</dd> <dt>

**進程**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) 
</dt> </dl>

處理序識別項。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore mof</dt> </dl> |



 

 




