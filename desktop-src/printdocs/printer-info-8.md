---
description: 印表機 \_ 資訊 \_ 8 結構會指定全域預設印表機設定。
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: 'PRINTER_INFO_8 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852224"
---
# <a name="printer_info_8-structure"></a>印表機 \_ 資訊 \_ 8 結構

**印表機 \_ 資訊 \_ 8** 結構會指定全域預設印表機設定。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a>成員

<dl> <dt>

**pDevMode**
</dt> <dd>

用來定義全域預設印表機資料的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標，例如紙張方向和解析度。

</dd> </dl>

## <a name="remarks"></a>備註

全域預設值是由可供任何人使用之印表機的系統管理員所設定。 相反地，每個使用者的預設值將會影響特定使用者或使用該設定檔的其他人。 針對每個使用者預設，請使用 [**印表機 \_ 資訊 \_ 9**](printer-info-9.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 資訊 \_ 8W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 8A** (ANSI) <br/>                           |



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

[**印表機 \_ 資訊 \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




