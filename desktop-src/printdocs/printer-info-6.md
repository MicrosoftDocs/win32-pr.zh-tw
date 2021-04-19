---
description: 印表機 \_ 資訊 \_ 6 會指定印表機的狀態值。
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: 'PRINTER_INFO_6 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984723"
---
# <a name="printer_info_6-structure"></a>印表機 \_ 資訊 \_ 6 結構

**印表機 \_ 資訊 \_ 6** 會指定印表機的狀態值。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a>成員

<dl> <dt>

**dwStatus**
</dt> <dd>

印表機狀態。 這個成員可以是下列值的任何合理組合。



| 值                               | 意義                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 印表機 \_ 狀態 \_ 忙碌中               | 印表機忙碌中。                                                                                          |
| 印表機 \_ 狀態 \_ 門 \_ 開啟         | 印表機門已開啟。                                                                                     |
| 印表機 \_ 狀態 \_ 錯誤              | 未使用。                                                                                                     |
| 印表機 \_ 狀態 \_ 初始化       | 印表機初始化中。                                                                                  |
| 印表機 \_ 狀態 \_ IO 使用中 \_         | 印表機處於作用中的輸入/輸出狀態                                                                |
| 印表機 \_ 狀態 \_ 手動 \_ 饋送       | 印表機處於手動摘要狀態。                                                                        |
| 印表機 \_ 狀態 \_ 無 \_ 墨粉          | 印表機的碳粉已用完。                                                                                  |
| 印表機 \_ 狀態 \_ 無法 \_ 使用     | 印表機無法列印。                                                                    |
| 印表機 \_ 狀態 \_ 離線            | 印表機為離線。                                                                                       |
| 印表機 \_ 狀態 \_ \_ 記憶體不足 \_    | 印表機的記憶體用盡。                                                                            |
| 印表機 \_ 狀態 \_ 輸出 \_ 紙匣已 \_ 滿  | 印表機的輸出紙匣已滿。                                                                             |
| 印表機 \_ 狀態 \_ 頁面 \_         | 印表機無法列印目前的頁面。                                                                    |
| 印表機 \_ 狀態 \_ 紙 \_ 紙         | 印表機中的紙張已卡住                                                                                |
| 印表機 \_ 狀態 \_ 紙張 \_ 輸出         | 印表機紙張用完。                                                                                  |
| 印表機 \_ 狀態 \_ 紙張 \_ 問題     | 印表機有紙張問題。                                                                              |
| 印表機 \_ 狀態已 \_ 暫停             | 印表機已暫停。                                                                                        |
| 印表機 \_ 狀態 \_ 暫止 \_ 刪除  | 因為呼叫 [**DeletePrinter**](deleteprinter.md) 函式，所以印表機暫止刪除。 |
| 印表機 \_ 狀態 \_ \_ 省電        | 印表機處於省電模式。                                                                            |
| 印表機 \_ 狀態 \_ 列印           | 印表機正在列印。                                                                                      |
| 印表機 \_ 狀態 \_ 處理         | 印表機正在處理來自 [**SetPrinter**](setprinter.md) 函式的命令。                       |
| 印表機 \_ 狀態 \_ 伺服器 \_ 不明    | 印表機狀態不明。                                                                                |
| 印表機 \_ 狀態 \_ 墨粉 \_ 低         | 印表機碳粉不足。                                                                                  |
| 印表機 \_ 狀態 \_ 使用者 \_ 介入 | 印表機有錯誤，需要使用者進行一些動作。                                              |
| 印表機 \_ 狀態 \_ 等候中            | 印表機正在等候。                                                                                       |
| 印表機 \_ 狀態 \_ 預熱 \_        | 印表機準備中。                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 資訊 \_ 6W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 6a** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
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
</dt> <dt>

[**印表機 \_ 資訊 \_ 5**](printer-info-5.md)
</dt> </dl>

 

 




