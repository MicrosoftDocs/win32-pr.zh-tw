---
description: 印表機 \_ 資訊 \_ 2 結構會指定詳細的印表機資訊。
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: 'PRINTER_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1f7a2b871cc0181fbceab56e4ac14170bf46fa1b31081f4b4365ad7296ec2e85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600608"
---
# <a name="printer_info_2-structure"></a>印表機 \_ 資訊 \_ 2 結構

**印表機 \_ 資訊 \_ 2** 結構會指定詳細的印表機資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a>成員

<dl> <dt>

**pServerName**
</dt> <dd>

以 null 結束的字串指標，識別控制印表機的伺服器。 如果這個字串是 **Null**，則會在本機控制印表機。

</dd> <dt>

**pPrinterName**
</dt> <dd>

指定印表機名稱之以 null 結束的字串指標。

</dd> <dt>

**pShareName**
</dt> <dd>

以 null 結束的字串指標，可識別印表機的共用點。  (只有在 \_ \_ 已設定 **屬性** 成員的印表機屬性共用常數時，才會使用此字串。 ) 

</dd> <dt>

**pPortName**
</dt> <dd>

以 null 結束的字串指標，識別用來將資料傳輸至印表機的埠 (s) 。 如果印表機連線到一個以上的埠，每個埠的名稱必須以逗號分隔 (例如，"LPT1：，LPT2：，LPT3：" ) 。

</dd> <dt>

**pDriverName**
</dt> <dd>

以 null 結束的字串指標，指定印表機驅動程式的名稱。

</dd> <dt>

**pComment**
</dt> <dd>

以 null 結束的字串指標，提供印表機的簡短描述。

</dd> <dt>

**pLocation**
</dt> <dd>

以 null 結束的字串指標，指定印表機 (的實體位置，例如 "Bldg"。 38，房間1164」 ) 。

</dd> <dt>

**pDevMode**
</dt> <dd>

用來定義預設印表機資料的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標，例如紙張方向和解析度。

</dd> <dt>

**pSepFile**
</dt> <dd>

以 null 結束的字串指標，指定用來建立分隔符號頁面的檔案名。 此頁面是用來分隔傳送至印表機的列印工作。

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

以 null 結束的字串指標，指定印表機所使用的列印處理器名稱。 您可以使用 [**EnumPrintProcessors**](enumprintprocessors.md) 函數來取得伺服器上所安裝之列印處理器的清單。

</dd> <dt>

**pDatatype**
</dt> <dd>

以 null 結束的字串指標，指定用來記錄列印工作的資料類型。 您可以使用 [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) 函數來取得特定列印處理器所支援的資料類型清單。

</dd> <dt>

**pParameters**
</dt> <dd>

指定預設列印處理器參數之以 null 結束的字串指標。

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

印表機的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構指標。 這個成員可以是 **Null**。

</dd> <dt>

**屬性**
</dt> <dd>

印表機屬性。 這個成員可以是下列值的任何合理組合。

| 值                                   | 意義                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 印表機 \_ 屬性 \_ 直接              | 作業會直接傳送到印表機 (不會) 。                                                                                                                                |
| 印表機 \_ 屬性 \_ \_ 先完成 \_ | 如果設定和印表機設定為列印時進行列印，則任何已完成的幕後處理作業都會排定在未完成幕後處理的作業之前列印。                          |
| 印表機 \_ 屬性 \_ 啟用 \_ DEVQ        | 如果設定，則會呼叫 **DevQueryPrint** 。 如果檔和印表機的設置不符， **DevQueryPrint** 可能會失敗。 設定此旗標會使不相符的檔保留在佇列中。 |
| 印表機 \_ 屬性 \_ 隱藏              | 保留的。                                                                                                                                                                               |
| 印表機 \_ 屬性 \_ KEEPPRINTEDJOBS     | 如果設定，則會在列印工作之後保留工作。 如果未設定，則會刪除作業。                                                                                                               |
| \_本機印表機屬性 \_               | 印表機是本機印表機。                                                                                                                                                             |
| 印表機 \_ 屬性 \_ 網路             | 印表機是網路印表機連接。                                                                                                                                                |
| \_ \_ 已發佈印表機屬性           | 指出是否要在目錄服務中發佈印表機。                                                                                                                    |
| 印表機 \_ 屬性已 \_ 排入佇列              | 如果設定，印表機會在最後一頁進行多工緩衝處理之後，再開始列印。 如果未設定，且 \_ \_ 未設定印表機屬性 DIRECT，則印表機會在幕後處理時進行幕後處理和列印。      |
| \_ \_ 僅限原始印表機屬性 \_           | 指出只有原始資料類型列印工作可以進行多工緩衝處理。                                                                                                                            |
| 印表機 \_ 屬性 \_ 共用              | 印表機是共用的。                                                                                                                                                                      |



 

在 Windows XP 和更新版本的 Windows 中，也可以使用下列值。

| 值                   | 意義                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 印表機 \_ 屬性 \_ 傳真 | 如果設定，印表機就是傳真印表機。 這只能由 [**interactivesession.addprinter**](addprinter.md)設定，但可由 [**>enumprinters**](enumprinters.md) 和 [**GetPrinter**](getprinter.md)來抓取。 |



 

在 Windows Vista 和更新版本的 Windows 中，也可以使用下列值。

| 值                               | 意義                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| 印表機 \_ 屬性 \_ 易記 \_ 名稱  | 電腦已連線到此印表機，並將其命名為易記名稱。           |
| 印表機 \_ 屬性 \_ 電腦         | 印表機是一台電腦的連線。                                             |
| 已 \_ 推入印表機屬性的 \_ \_ 使用者    | 印表機是使用 [推播印表機連線] 使用者原則安裝的。     |
| 印表機 \_ 屬性已 \_ 推送 \_ 電腦 | 印表機是使用 [推播印表機連線] 電腦原則安裝的。 |



 

在 Windows Server 2003 中，也可以使用下列值。

| 值                  | 意義                                                                 |
|------------------------|-------------------------------------------------------------------------|
| 印表機 \_ 屬性 \_ TS | 指出印表機目前透過終端機伺服器連線。 |



 

</dd> <dt>

**優先順序**
</dt> <dd>

多工緩衝處理器用來路由列印工作的優先順序值。

</dd> <dt>

**DefaultPriority**
</dt> <dd>

指派給每個列印工作的預設優先權值。

</dd> <dt>

**StartTime**
</dt> <dd>

印表機將列印工作的最早時間。 此值的表示方式為自 12:00 AM GMT 起的經過時間， (格林尼治平均時間) 。

</dd> <dt>

**UntilTime**
</dt> <dd>

印表機將列印工作的最新時間。 此值的表示方式為自 12:00 AM GMT 起的經過時間， (格林尼治平均時間) 。

</dd> <dt>

**狀態**
</dt> <dd>

印表機狀態。 這個成員可以是下列值的任何合理組合。



| 值                               | 意義                                                          |
|-------------------------------------|------------------------------------------------------------------|
| 印表機 \_ 狀態 \_ 忙碌中               | 印表機忙碌中。                                             |
| 印表機 \_ 狀態 \_ 門 \_ 開啟         | 印表機門已開啟。                                        |
| 印表機 \_ 狀態 \_ 錯誤              | 印表機處於錯誤狀態。                                |
| 印表機 \_ 狀態 \_ 初始化       | 印表機初始化中。                                     |
| 印表機 \_ 狀態 \_ IO 使用中 \_         | 印表機處於作用中的輸入/輸出狀態                   |
| 印表機 \_ 狀態 \_ 手動 \_ 饋送       | 印表機處於手動摘要狀態。                           |
| 印表機 \_ 狀態 \_ 無 \_ 墨粉          | 印表機的碳粉已用完。                                     |
| 印表機 \_ 狀態 \_ 無法 \_ 使用     | 印表機無法列印。                       |
| 印表機 \_ 狀態 \_ 離線            | 印表機為離線。                                          |
| 印表機 \_ 狀態 \_ \_ 記憶體不足 \_    | 印表機的記憶體用盡。                               |
| 印表機 \_ 狀態 \_ 輸出 \_ 紙匣已 \_ 滿  | 印表機的輸出紙匣已滿。                                |
| 印表機 \_ 狀態 \_ 頁面 \_         | 印表機無法列印目前的頁面。                       |
| 印表機 \_ 狀態 \_ 紙 \_ 紙         | 印表機中的紙張已卡住                                   |
| 印表機 \_ 狀態 \_ 紙張 \_ 輸出         | 印表機紙張用完。                                     |
| 印表機 \_ 狀態 \_ 紙張 \_ 問題     | 印表機有紙張問題。                                 |
| 印表機 \_ 狀態已 \_ 暫停             | 印表機已暫停。                                           |
| 印表機 \_ 狀態 \_ 暫止 \_ 刪除  | 正在刪除印表機。                                    |
| 印表機 \_ 狀態 \_ \_ 省電        | 印表機處於省電模式。                               |
| 印表機 \_ 狀態 \_ 列印           | 印表機正在列印。                                         |
| 印表機 \_ 狀態 \_ 處理         | 印表機正在處理列印工作。                           |
| 印表機 \_ 狀態 \_ 伺服器 \_ 不明    | 印表機狀態不明。                                   |
| 印表機 \_ 狀態 \_ 墨粉 \_ 低         | 印表機碳粉不足。                                     |
| 印表機 \_ 狀態 \_ 使用者 \_ 介入 | 印表機有錯誤，需要使用者進行一些動作。 |
| 印表機 \_ 狀態 \_ 等候中            | 印表機正在等候。                                          |
| 印表機 \_ 狀態 \_ 預熱 \_        | 印表機準備中。                                       |



 

</dd> <dt>

**cJobs**
</dt> <dd>

已排入印表機佇列的列印工作數目。

</dd> <dt>

**AveragePPM**
</dt> <dd>

印表機上每分鐘列印的平均頁數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 2a** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**版**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**>enumprinters**](enumprinters.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 1**](printer-info-1.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 3**](printer-info-3.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)
</dt> <dt>

[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

