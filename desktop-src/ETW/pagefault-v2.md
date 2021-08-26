---
description: 這個類別是分頁錯誤事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd8adfa698975f7661abdbd849136d04049b5539ff3fed3b52b61660791add0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900748"
---
# <a name="pagefault_v2-class"></a>PageFault \_ V2 類別

這個類別是分頁錯誤事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**PageFault \_ V2** 類別未定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用所有分頁錯誤事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 記憶體 \_ 頁面 \_ 錯誤** 旗標。 您也可以指定下列旗標：

-   **事件 \_ 追蹤 \_ 旗標 \_ 記憶體 \_ 硬性 \_ 錯誤**
-   **事件 \_ 追蹤 \_ 旗標 \_ 虛擬 \_ 分配**

事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**PageFaultGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以針對所有分頁錯誤事件執行特殊處理。 使用下列事件種類來識別使用事件時的實際記憶體事件。



| 事件類型                                                     | 描述                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 事件 \_ 追蹤 \_ 類型 \_ MM \_ 牛 (事件種類值為 12) <br/> | 複製時寫入事件。 [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。 在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。     |
| 事件 \_ 追蹤 \_ 類型 \_ MM \_ DZF (事件種類值為 11) <br/> | 要求零錯誤事件。 [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。 在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。 |
| 事件 \_ 追蹤 \_ 類型 \_ MM \_ GPF (事件種類值為 13) <br/> | 防護分頁錯誤事件。 [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。 在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。  |
| 事件 \_ 追蹤 \_ 類型 \_ MM \_ HPF (事件種類值為 14) <br/> | 硬分頁錯誤事件。 [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。 在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。   |
| 事件 \_ 追蹤 \_ 類型 \_ MM \_ TF (事件種類值為 10) <br/>  | 轉換錯誤事件。 [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。 在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。  |
| 事件 \_ 追蹤 \_ 類型 \_ MM \_ AV (事件種類值為 15) <br/>  | 存取違規事件。 [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                           |
| 事件種類值，32                                           | 硬分頁錯誤事件。 [**PageFault \_ HardFault**](pagefault-hardfault.md) MOF 類別會定義此事件的事件資料。                                                                                                                               |
| 事件種類值，105                                          | 分頁檔案事件中的影像載入。 [**PageFault \_ ImageLoadBacked**](pagefault-imageloadbacked.md) MOF 類別會定義此事件的事件資料。                                                                                                          |
| 事件種類值，98                                           | 虛擬配置事件。 [**VirtualAlloc**](pagefault-virtualalloc.md) MOF 類別會定義此事件的事件資料。                                                                                                                                |
| 事件種類值，99                                           | 虛擬釋放事件。 [**VirtualAlloc**](pagefault-virtualalloc.md) MOF 類別會定義此事件的事件資料。                                                                                                                                      |



 

您可以使用 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員，找出錯誤的進程或執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



 

 
