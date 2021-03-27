---
description: 這個類別是效能計數器事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: PerfInfo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972225"
---
# <a name="perfinfo-class"></a>PerfInfo 類別

這個類別是效能計數器事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**PerfInfo** 類別不會定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用延遲程序呼叫 (DPC) 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函式時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ DPC** 旗標。 您也可以指定下列一或多個旗標：

-   **事件 \_ 追蹤 \_ 旗標 \_ 中斷**
-   **事件 \_ 追蹤 \_ 旗標 \_ 設定檔**
-   **事件 \_ 追蹤 \_ 旗標 \_ SYSTEMCALL**

事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**PerfInfoGuid**](nt-kernel-logger-constants.md) 指定為 *PGUID* 參數，來執行 DPC 事件的特殊處理。 使用下列事件種類來識別使用事件時的實際事件。



| 事件類型           | 描述                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| 事件種類值，46 | 取樣設定檔事件。 [**SampledProfile**](sampledprofile.md) MOF 類別會定義此事件的事件資料。 |
| 事件種類值，51 | 系統呼叫進入事件。 [**SysCallEnter**](syscallenter.md) MOF 類別會定義此事件的事件資料。   |
| 事件種類值，52 | 系統呼叫離開事件。 [**SysCallExit**](syscallexit.md) MOF 類別會定義此事件的事件資料。      |
| 事件種類值，66 | 執行緒 DPC 事件。 [**DPC**](dpc.md) MOF 類別會定義此事件的事件資料。                          |
| 事件種類值，67 | 插斷服務常式 (ISR) 事件。 [**ISR**](isr.md) MOF 類別會定義此事件的事件資料。       |
| 事件種類值，68 | DPC 事件。 [**DPC**](dpc.md) MOF 類別會定義此事件的事件資料。                                   |
| 事件種類值，69 | DPC 計時器事件。 [**DPC**](dpc.md) MOF 類別會定義此事件的事件資料。                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 
