---
description: 這個類別是插斷服務常式的事件種類類別， (ISR) 事件。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973309"
---
# <a name="isr-class"></a>ISR 類別

這個類別是插斷服務常式的事件種類類別， (ISR) 事件。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a>成員

**ISR** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ISR** 類別具有這些屬性。

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，副檔名 ( "WmiTime" ) 
</dt> </dl>

ISR 進入時間。

</dd> <dt>

**已保留**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) ，指標
</dt> </dl>

保留的。

</dd> <dt>

**ReturnValue**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

布林值，指出是否已宣告中斷 (如果已宣告中斷) ，則為 True。

</dd> <dt>

**常規**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

ISR 常式的位址。 使用具有影像事件的位址，以找出已啟動的映射。

</dd> <dt>

**向量**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

從中斷描述中繼資料表中指派了 ISR 常式的向量。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




