---
description: 印表機 \_ 資訊 \_ 9 結構會指定每位使用者的預設印表機設定。
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: 'PRINTER_INFO_9 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980673"
---
# <a name="printer_info_9-structure"></a>印表機 \_ 資訊 \_ 9 結構

**印表機 \_ 資訊 \_ 9** 結構會指定每位使用者的預設印表機設定。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a>成員

<dl> <dt>

**pDevMode**
</dt> <dd>

用來定義每個使用者預設印表機資料的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標，例如紙張方向和解析度。 **DEVMODE** 會儲存在使用者的登錄中。

</dd> </dl>

## <a name="remarks"></a>備註

每個使用者預設值只會影響特定使用者或使用此設定檔的任何人。 相反地，全域預設值是由可供任何人使用的印表機管理員設定。 若為全域預設值，請使用 [**印表機 \_ 資訊 \_ 8**](printer-info-8.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 資訊 \_ 9W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 9A** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




