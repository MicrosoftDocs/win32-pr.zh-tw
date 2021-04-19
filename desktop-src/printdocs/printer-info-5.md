---
description: 印表機 \_ 資訊 \_ 5 結構會指定詳細的印表機資訊。
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: 'PRINTER_INFO_5 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988884"
---
# <a name="printer_info_5-structure"></a>印表機 \_ 資訊 \_ 5 結構

**印表機 \_ 資訊 \_ 5** 結構會指定詳細的印表機資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a>成員

<dl> <dt>

**pPrinterName**
</dt> <dd>

指定印表機名稱之以 null 結束的字串指標。

</dd> <dt>

**pPortName**
</dt> <dd>

以 null 結束的字串指標，識別用來將資料傳輸至印表機的埠 (s) 。 如果印表機連線到一個以上的埠，每個埠的名稱必須以逗號分隔 (例如，"LPT1：，LPT2：，LPT3：" ) 。

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



 

</dd> <dt>

**DeviceNotSelectedTimeout**
</dt> <dd>

不使用這個值。

</dd> <dt>

**TransmissionRetryTimeout**
</dt> <dd>

不使用這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 資訊 \_** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 5a** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**>enumprinters**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 1**](printer-info-1.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 3**](printer-info-3.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




