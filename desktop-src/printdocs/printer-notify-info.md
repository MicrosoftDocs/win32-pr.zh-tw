---
description: 印表機 \_ 通知 \_ 資訊結構包含 FindNextPrinterChangeNotification 函式所傳回的印表機資訊。 在滿足印表機變更通知物件的等候作業之後，此函數會傳回此資訊。
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: 'PRINTER_NOTIFY_INFO 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 26c7fca07eda8638bf657055691d72c78bccdbec6ef2b9a8c76ee7cf830bc767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091848"
---
# <a name="printer_notify_info-structure"></a>印表機 \_ 通知 \_ 資訊結構

**印表機 \_ 通知 \_ 資訊** 結構包含 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函式所傳回的印表機資訊。 在滿足印表機變更通知物件的等候作業之後，此函數會傳回此資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

此結構的版本。 將這個成員設定為2。

</dd> <dt>

**旗標**
</dt> <dd>

指出通知結構狀態的位旗標。 如果設定了 [印表機 \_ 通知 \_ 資訊 \_ 已捨棄] 位，則表示必須捨棄某些通知。

</dd> <dt>

**Count**
</dt> <dd>

**AData** 陣列中的 [**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)元素數目。

</dd> <dt>

**aData**
</dt> <dd>

[**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)結構的陣列。 陣列的每個元素都會識別單一作業或印表機資訊欄位，並提供該欄位目前的資料。

</dd> </dl>

## <a name="remarks"></a>備註

如果 **旗標** 成員具有已設定的印表機 \_ 通知 \_ 資訊 \_ ，則表示發生溢位或錯誤，而且通知可能已遺失。 在此情況下，您必須呼叫 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) ，並指定 [印表機通知選項重新整理] \_ 旗標 \_ \_ ，以取得所有目前的資訊。 在您要求此重新整理作業之前，系統不會傳送此變更通知物件的其他通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)
</dt> </dl>

 

 




