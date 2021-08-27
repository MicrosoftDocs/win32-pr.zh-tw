---
description: 這個類別是系統呼叫 exit 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: SysCallExit 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: aa297ced8f6c0d17c0c01da9ce11705d30fe7448c8bc2f2ae6358ddc85f653be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102058"
---
# <a name="syscallexit-class"></a>SysCallExit 類別

這個類別是系統呼叫 exit 事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>成員

**SysCallExit** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SysCallExit** 類別具有這些屬性。

<dl> <dt>

**SysCallNtStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，格式 ( "x" ) 
</dt> </dl>

NT 系統呼叫所傳回的狀態碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 




