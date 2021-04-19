---
description: 印表機 \_ 通知 \_ 選項結構會指定監視印表機或列印伺服器之變更通知物件的選項。
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: 'PRINTER_NOTIFY_OPTIONS 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987584"
---
# <a name="printer_notify_options-structure"></a>印表機 \_ 通知 \_ 選項結構

**印表機 \_ 通知 \_ 選項** 結構會指定監視印表機或列印伺服器之變更通知物件的選項。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

此結構的版本。 將這個成員設定為2。

</dd> <dt>

**旗標**
</dt> <dd>

位旗標。 如果您在 FindNextPrinterChangeNotification 函式的呼叫中設定 [印表機通知選項重新整理] 旗標，此函式會 \_ \_ \_ 為所有受監視的印表機資訊欄位提供目前的資料。 [](findnextprinterchangenotification.md) [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函式會忽略 **旗標** 成員。

</dd> <dt>

**Count**
</dt> <dd>

**PTypes** 陣列中的元素數目。

</dd> <dt>

**pTypes**
</dt> <dd>

[**印表機 \_ 通知 \_ 選項 \_ 類型**](printer-notify-options-type.md)結構的陣列指標。 使用這個陣列的一個專案來指定要監視的印表機資訊欄位，以及一個專案來指定要監視的作業資訊欄位。 您可以監視印表機資訊、作業資訊或兩者。

</dd> </dl>

## <a name="remarks"></a>備註

使用此結構搭配 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) 函式來指定要監視變更的印表機或作業資訊欄位集。

使用此結構搭配 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函式，以要求所有受監視印表機和作業資訊欄位目前的資料。 在此情況下， **旗標** 成員會指定印表機通知選項的重新整理旗標，而函式會 \_ \_ \_ 忽略其他結構成員。

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 選項 \_ 類型**](printer-notify-options-type.md)
</dt> </dl>

 

 




