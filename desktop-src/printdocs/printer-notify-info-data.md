---
description: 印表機 \_ 通知 \_ 資訊 \_ 資料結構會識別工作或印表機資訊欄位，並提供該欄位目前的資料。
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: 'PRINTER_NOTIFY_INFO_DATA 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193188"
---
# <a name="printer_notify_info_data-structure"></a>印表機 \_ 通知 \_ 資訊 \_ 資料結構

**印表機 \_ 通知 \_ 資訊 \_ 資料** 結構會識別工作或印表機資訊欄位，並提供該欄位目前的資料。

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函式會傳回 [**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md)結構，其中包含 **印表機 \_ 通知 \_ 資訊 \_ 資料** 結構的陣列。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a>成員

<dl> <dt>

**型別**
</dt> <dd>

指出所提供的資訊類型。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                                      | 意義                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**作業 \_通知 \_ 類型**</dt> <dt>0x01</dt> </dl>             | 指出 **欄位** 成員指定工作 \_ 通知 \_ 欄位 \_ \* 常數。<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**印表機 \_通知 \_ 類型**</dt> <dt>0x00</dt> </dl> | 指出 **欄位** 成員指定印表機 \_ 通知 \_ 欄位 \_ \* 常數。<br/> |



 

</dd> <dt>

**欄位**
</dt> <dd>

表示已變更的欄位。 如需可能值的清單，請參閱「備註」一節。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> <dt>

**識別碼**
</dt> <dd>

指出當 **類型** 成員指定工作通知類型時的工作識別碼 \_ \_ 。 如果 **類型** 成員指定了 [印表機 \_ 通知類型] \_ ，則這個成員是未定義的。

</dd> <dt>

**NotifyData**
</dt> <dd>

以 **類型** 和 **欄位** 成員為基礎之資料資訊的聯集。 如需與每個欄位相關聯之資料類型的描述，請參閱「備註」一節。

<dl> <dt>

**adwData \[ 2\]**
</dt> <dd>

兩個 **DWORD** 值的陣列。 對於只使用單一 **DWORD** 的資訊欄位，資料位於 **adwData** \[ 0 \] 。

</dd> <dt>

**資料**
</dt> <dd> <dl> <dt>

**cbBuf**
</dt> <dd>

指出 **pBuf** 所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

**pBuf**
</dt> <dd>

包含欄位目前資料之緩衝區的指標。

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

如果 **類型** 成員指定 [印表機 \_ 通知 \_ 類型]， **欄位** 成員可以是下列其中一個值。



<table>
<thead>
<tr class="header">
<th>欄位</th>
<th>資料類型</th>
<th>值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SERVER_NAME</td>
<td>不支援。</td>
<td>0x00</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINTER_NAME</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含印表機的名稱。</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，可識別印表機的共用點。</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含列印工作將列印到的埠名稱。 如果 &quot; 選取 [印表機共用] &quot; ，這是以逗號分隔的埠清單。</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含印表機驅動程式的名稱。</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含新的批註字串，通常是印表機的簡短描述。</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含印表機的新實體位置 (例如 &quot; Bldg。 38，房間 1164 &quot;) 。</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>pBuf</strong> 是 <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> 結構的指標，可定義預設印表機資料，例如紙張方向和解析度。</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，可指定用來建立分隔符號頁面的檔案名。 此頁面是用來分隔傳送至印表機的列印工作。</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，可指定印表機所使用的列印處理器名稱。</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，可指定預設的列印處理器參數。</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>pBuf</strong> 是以 null 結束的字串指標，可指定用來記錄列印工作的資料類型。</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>pBuf</strong> 是印表機 <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> 結構的指標。 如果沒有安全描述項，指標可能會是 <strong>Null</strong> 。</td>
<td>0x0C</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwData</strong> [0] 指定印表機屬性，它可以是下列其中一個值：<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0D</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwData</strong> [0] 指定多工緩衝處理器用來路由列印工作的優先順序值。</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwData</strong> [0] 指定指派給每個列印工作的預設優先權值。</td>
<td>0x0F</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwData</strong> [0] 指定印表機要列印工作的最早時間。  (此值指定的時間，在 12:00 A.M. 之後經過的時間 ) </td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwData</strong> [0] 會指定印表機列印工作的最晚時間。  (此值指定的時間，在 12:00 A.M. 之後經過的時間 ) </td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwData</strong> [0] 指定印表機的狀態。 如需可能值的清單，請參閱 <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> 結構。</td>
<td>0x12</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>不支援。</td>
<td>0x13</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_CJOBS</td>
<td><strong>adwData</strong> [0] 指定印表機已排入佇列的列印工作數目。</td>
<td>0x14</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_AVERAGE_PPM</td>
<td><strong>adwData</strong> [0] 指定印表機上每分鐘列印的平均頁數。</td>
<td>0x15</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_PAGES</td>
<td>不支援。</td>
<td>0x16</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PAGES_PRINTED</td>
<td>不支援。</td>
<td>0x17</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_BYTES</td>
<td>不支援。</td>
<td>0x18</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_BYTES_PRINTED</td>
<td>不支援。</td>
<td>0x19</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_OBJECT_GUID</td>
<td>這是在物件 GUID 變更時設定。</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>如果印表機連接已重新命名，就會設定此設定。</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

如果 **類型** 成員指定了工作 \_ 通知 \_ 類型， **欄位** 成員可以是下列其中一個值。



| 欄位                                    | 資料類型                                                                                                                                                                                                                                            | 值 |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| 作業 \_ 通知 \_ 欄位 \_ 印表機 \_ 名稱        | **pBuf** 是以 null 結束的字串指標，其中包含工作要進行多工緩衝處理的印表機名稱。                                                                                                                                      | 0x00  |
| 作業 \_ 通知 \_ 欄位 \_ 電腦 \_ 名稱        | **pBuf** 是以 null 結束的字串指標，可指定建立列印工作的電腦名稱稱。                                                                                                                                    | 0x01  |
| 作業 \_ 通知 \_ 欄位 \_ 埠 \_ 名稱           | **pBuf** 是以 null 結束的字串指標，可識別用來將資料傳輸至印表機的埠 (s) 。 如果印表機連線到一個以上的埠，埠的名稱會以逗號分隔 (例如，"LPT1：，LPT2：，LPT3：" ) 。 | 0x02  |
| 作業 \_ 通知 \_ 欄位 \_ 使用者 \_ 名稱           | **pBuf** 是以 null 結束的字串指標，可指定傳送列印工作之使用者的名稱。                                                                                                                                           | 0x03  |
| 作業 \_ 通知 \_ 欄位 \_ 通知 \_ 名稱         | **pBuf** 是以 null 結束的字串指標，可指定在列印工作或列印工作時發生錯誤時應通知的使用者名稱。                                                              | 0x04  |
| 作業 \_ 通知 \_ 欄位 \_ 資料類型             | **pBuf** 是以 null 結束的字串指標，可指定用來記錄列印工作的資料類型。                                                                                                                                         | 0x05  |
| 作業 \_ 通知 \_ 欄位 \_ 列印 \_ 處理器     | **pBuf** 是以 null 結束的字串指標，可指定用來列印工作的列印處理器名稱。                                                                                                                           | 0x06  |
| 作業 \_ 通知 \_ 欄位 \_ 參數           | **pBuf** 是以 null 結束的字串指標，可指定列印處理器參數。                                                                                                                                                            | 0x07  |
| 作業 \_ 通知 \_ 欄位 \_ 驅動程式 \_ 名稱         | **pBuf** 是以 null 結束的字串指標，可指定應該用來處理列印工作的印表機驅動程式名稱。                                                                                                           | 0x08  |
| 作業 \_ 通知 \_ 欄位 \_ DEVMODE              | **pBuf** 是 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構的指標，其中包含印表機驅動程式的裝置初始化和環境資料。                                                                                                        | 0x09  |
| 作業 \_ 通知 \_ 欄位 \_ 狀態               | **adwData** \[0 \] 指定工作狀態。 如需可能值的清單，請參閱 [**作業 \_ 資訊 \_ 2**](job-info-2.md) 結構。                                                                                                                        | 0x0A  |
| 作業 \_ 通知 \_ 欄位 \_ 狀態 \_ 字串       | **pBuf** 是以 null 結束的字串指標，可指定列印工作的狀態。                                                                                                                                                           | 0x0B  |
| 作業 \_ 通知 \_ 欄位 \_ 安全 \_ 描述項 | 不支援。                                                                                                                                                                                                                                          | 0x0C  |
| 作業 \_ 通知 \_ 欄位 \_ 檔             | **pBuf** 是以 null 結束的字串指標，可指定列印工作的名稱 (例如 "ms-chap： Review.doc" ) 。                                                                                                                        | 0x0D  |
| 作業 \_ 通知 \_ 欄位 \_ 優先順序             | **adwData** \[0 \] 指定作業優先權。                                                                                                                                                                                                           | 0x0E  |
| 作業 \_ 通知 \_ 欄位 \_ 位置             | **adwData** \[0 \] 指定工作在列印佇列中的位置。                                                                                                                                                                                      | 0x0F  |
| 已 \_ 提交工作通知 \_ 欄位 \_            | **pBuf** 是 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構的指標，可指定提交作業的時間。                                                                                                                          | 0x10  |
| 作業 \_ 通知 \_ 欄位 \_ 開始 \_ 時間          | **adwData** \[0 \] 指定可列印工作的最早時間。  (此值指定的時間，在 12:00 A.M. 之後經過的時間 )                                                                                                                 | 0x11  |
| 作業 \_ 通知 \_ 欄位 \_ 至 \_ 時間          | **adwData** \[0 \] 指定可列印工作的最晚時間。  (此值指定的時間，在 12:00 A.M. 之後經過的時間 )                                                                                                                   | 0x12  |
| 作業 \_ 通知 \_ 欄位 \_ 時間                 | **adwData** \[0 \] 指定自作業開始列印以來經過的總時間（以秒為單位）。                                                                                                                                                  | 0x13  |
| 作業 \_ 通知 \_ 欄位 \_ 總計 \_ 頁面         | **adwData** \[0 \] 指定作業的大小（以頁面為限）。                                                                                                                                                                                             | 0x14  |
| 列印的工作 \_ 通知 \_ 欄位 \_ 頁面 \_       | **adwData** \[0 \] 指定已列印的頁面數目。                                                                                                                                                                                      | 0x15  |
| 作業 \_ 通知 \_ 欄位 \_ 總 \_ 位元組數         | **adwData** \[0 \] 指定作業的大小（以位元組為單位）。                                                                                                                                                                                             | 0x16  |
| 已 \_ 列印工作通知 \_ 欄位 \_ 位元組 \_       | **adwData** \[0 \] 指定在此作業上列印的位元組數目。 針對此欄位，當傳送位元組至印表機時，變更通知物件會收到信號。                                                                      | 0x17  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**版**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**作業 \_ 資訊 \_ 2**](job-info-2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md)
</dt> <dt>

[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

