---
description: 此類別是驅動程式完整常式事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: DriverCompletionRoutine 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac1329c60f38ebfb4597b85ec251e074babd2c1fde7e58fee2423b6a11be92f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814886"
---
# <a name="drivercompletionroutine-class"></a>DriverCompletionRoutine 類別

此類別是驅動程式完整常式事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>成員

**DriverCompletionRoutine** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**DriverCompletionRoutine** 類別具有這些屬性。

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

IO 要求封包。

</dd> <dt>

**常規**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

要呼叫的驅動程式函式的位址。

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

可唯一識別要求的識別碼。 您可以使用這個識別碼，將其他驅動程式事件相互關聯，例如 [**DriverCompleteRequest**](drivercompleterequest.md) 事件。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




