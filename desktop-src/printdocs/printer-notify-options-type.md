---
description: 印表機 \_ 通知 \_ 選項 \_ 類型結構會指定印表機變更通知物件所要監視的印表機或作業資訊欄位集。FindFirstPrinterChangeNotification 函式的呼叫會指定印表機 \_ 通知 \_ 選項結構，其中包含印表機 \_ 通知 \_ 選項類型結構的陣列 \_ 。
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: 'PRINTER_NOTIFY_OPTIONS_TYPE 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987585"
---
# <a name="printer_notify_options_type-structure"></a>印表機 \_ 通知 \_ 選項 \_ 類型結構

**印表機 \_ 通知 \_ 選項 \_ 類型** 結構會指定印表機變更通知物件所要監視的印表機或作業資訊欄位集。

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函式的呼叫會指定 [**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)結構，其中包含 **印表機 \_ 通知 \_ 選項 \_ 類型** 結構的陣列。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a>成員

<dl> <dt>

**型別**
</dt> <dd>

要監看的型別。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                                      | 意義                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**作業 \_通知 \_ 類型**</dt> <dt>0x01</dt> </dl>             | 指出 **pFields** 陣列中指定的欄位是工作 \_ 通知 \_ 欄位 \_ \* 常數。<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**印表機 \_通知 \_ 類型**</dt> <dt>0x00</dt> </dl> | 指出 **pFields** 陣列中指定的欄位是印表機 \_ 通知 \_ 欄位 \_ \* 常數。<br/> |



 

</dd> <dt>

**Reserved0**
</dt> <dd>

保留的。

</dd> <dt>

**Reserved1**
</dt> <dd>

保留的。

</dd> <dt>

**Reserved2**
</dt> <dd>

保留的。

</dd> <dt>

**Count**
</dt> <dd>

**PFields** 陣列中的元素數目。

</dd> <dt>

**pFields**
</dt> <dd>

值陣列的指標。 陣列的每個元素都會指定相關的作業或印表機資訊欄位。 如需支援的印表機和作業資訊欄位清單，請參閱 [**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md) 結構。

</dd> </dl>

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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)
</dt> </dl>

 

 




