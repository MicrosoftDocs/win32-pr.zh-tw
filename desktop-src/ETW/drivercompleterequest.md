---
description: 此類別是驅動程式完成要求事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: DriverCompleteRequest 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ef20d7bf097c35e03e94ee9bb80e7fd74ad93d3f28830c66b155b3cacf400b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151629"
---
# <a name="drivercompleterequest-class"></a>DriverCompleteRequest 類別

此類別是驅動程式完成要求事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>成員

**DriverCompleteRequest** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**DriverCompleteRequest** 類別具有這些屬性。

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

**RoutineAddr**
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

可唯一識別要求的識別碼。 您可以使用這個識別碼，將其他驅動程式事件相互關聯，例如 [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) 事件。

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

 

 




