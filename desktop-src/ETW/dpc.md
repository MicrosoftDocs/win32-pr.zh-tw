---
description: 這個類別是 (DPC) 事件之裝置延遲程序呼叫的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: DPC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847776"
---
# <a name="dpc-class"></a>DPC 類別

這個類別是 (DPC) 事件之裝置延遲程序呼叫的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a>成員

**DPC** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**DPC** 類別具有這些屬性。

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，副檔名 ( "WmiTime" ) 
</dt> </dl>

DPC 進入時間。

</dd> <dt>

**常規**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

DPC 常式的位址。 使用具有影像事件的位址，以找出已啟動的映射。

</dd> </dl>

## <a name="remarks"></a>備註

輸入 DPC 時，會記錄這些事件。 您可以使用這些事件來監視和驗證驅動程式和核心模式元件的行為。 例如，您可以使用 DPC、ISR 和 Image 事件來判斷在高中斷層級花費太多時間的元件。 DPC 和 ISR 事件具有進入時間戳記，可用來計算常式的持續時間。 系統會讀取影像事件，以建立對應至特定模組的記憶體區域。 您可以使用對應來找出包含中斷常式的模組。

TimerDPC 事件會記錄當 DPC 過期而引發的 DPC，以及執行緒 DPC 執行時的 ThreadDPC 事件記錄。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




