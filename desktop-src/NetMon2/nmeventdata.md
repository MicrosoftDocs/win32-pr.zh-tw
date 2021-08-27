---
description: NMEVENTDATA 結構包含事件條件的相關資訊，該條件會傳遞給網路監視器，以在專家檢視器中插入一行。
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: 'NMEVENTDATA 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: af2a4775be7d9e123974fbab865a8171d9bc9dec7dacae7692054bc6db0d3085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037038"
---
# <a name="nmeventdata-structure"></a>NMEVENTDATA 結構

**NMEVENTDATA** 結構包含事件條件的相關資訊，該條件會傳遞給網路監視器，以在專家檢視器中插入一行。

## <a name="syntax"></a>語法


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

**NMEVENTDATA** 結構的版本號碼。 版本號碼必須為零。 網路監視器的未來版本可能會支援較高的版本號碼。

</dd> <dt>

**EventIdent**
</dt> <dd>

事件的識別項。 **EventIdent** 對每個專家都是唯一的，並參考 [事件參考頁面](event-reference-page.md)。

</dd> <dt>

**旗標**
</dt> <dd>

一組旗標，描述傳送事件資料的物件，以及事件的顯示方式。



| 值                                                                                                                                                                                                                                              | 意義                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**事件 \_ 旗標 \_ 專家**</dt> </dl>                                                                         | 活動來自專家。 <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 嚴重性**</dt> </dl>                 | 不要顯示事件的嚴重性層級。 <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 來源**</dt> </dl>                       | 不要顯示事件的來源名稱。 <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 事件 \_ 名稱**</dt> </dl>          | 不要顯示事件的事件名稱。 <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 描述**</dt> </dl>        | 不要顯示事件的描述。 <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 電腦**</dt> </dl>                    | 不要顯示事件的電腦名稱稱。 <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 時間**</dt> </dl>                             | 不顯示事件的時間 <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 固定 \_ 的資料行**</dt> </dl> | 不要顯示 [嚴重性]、[來源]、[事件名稱]、[描述]、[電腦] 或 [時間] 欄。 這不是單一旗標，但它是前六個旗標的聯集。 <br/> |



 

</dd> <dt>

**嚴重性**
</dt> <dd>

事件的嚴重性層級。 嚴重性層級可以具有下列其中一個值：

NMEVENT \_ 嚴重性 \_ 資訊 NMEVENT \_ 嚴重性 \_ 警告 NMEVENT \_ 嚴重性 \_ 強烈 \_ 警告 NMEVENT \_ 嚴重性 \_ 錯誤 NMEVENT \_ 嚴重性 \_ 嚴重 \_ 錯誤 NMEVENT \_ 嚴重性 \_ 嚴重 \_ 錯誤

</dd> <dt>

**NumColumns**
</dt> <dd>

目前結構中所指定的資料行數目。

</dd> <dt>

**szSourceName**
</dt> <dd>

顯示之專家的名稱。

</dd> <dt>

**szEventName**
</dt> <dd>

顯示之事件的名稱。

</dd> <dt>

**szDescription**
</dt> <dd>

所顯示事件的描述。

</dd> <dt>

**szMachine**
</dt> <dd>

已淘汰，應為 **Null**。

</dd> <dt>

**理由**
</dt> <dd>

事件檢視器的第二個視窗中顯示的資訊。 **理由** 成員可以是 **Null**。 如果是 **Null**，則不會顯示第二個視窗。

</dd> <dt>

**szUrl**
</dt> <dd>

保護此成員必須是 **Null**。

</dd> <dt>

**SysTime**
</dt> <dd>

發生事件條件的時間。 時間是相對於捕捉的開頭來測量。

</dd> <dt>

**資料行**
</dt> <dd>

出現在事件檢視器上方窗格中的資料行結構資料表。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




