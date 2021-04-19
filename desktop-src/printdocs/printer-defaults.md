---
description: 印表機 \_ 預設結構會指定印表機的預設資料類型、環境、初始化資料和存取權限。
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: 'PRINTER_DEFAULTS 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998304"
---
# <a name="printer_defaults-structure"></a>印表機 \_ 預設結構

**印表機 \_ 預設** 結構會指定印表機的預設資料類型、環境、初始化資料和存取權限。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a>成員

<dl> <dt>

**pDatatype**
</dt> <dd>

以 null 結束的字串指標，指定印表機的預設資料類型。

</dd> <dt>

**pDevMode**
</dt> <dd>

用來識別印表機預設環境和初始化資料的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標。

</dd> <dt>

**DesiredAccess**
</dt> <dd>

指定印表機所需的存取權限。 [**OpenPrinter**](openprinter.md)函式會使用這個成員來設定印表機的存取權限。 這些許可權可能會影響 [**SetPrinter**](setprinter.md) 和 [**DeletePrinter**](deleteprinter.md) 函數的操作。 存取權限可以是下列其中一項。



| 值                                       | 意義                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 印表機 \_ 存取 \_ 管理                 | 執行管理工作，例如 [**SetPrinter**](setprinter.md)所提供的工作。                                                                                                 |
| 印表機 \_ 存取 \_ 使用                        | 執行基本列印工作。                                                                                                                                                        |
| 印表機 \_ 存取 \_ 管理 \_ 受限            | 執行管理工作，例如 [**SetPrinter**](setprinter.md) 和 [**SetPrinterData**](setprinterdata.md)所提供的工作。 從 Windows 8.1 開始，可以使用這個值。 |
| 印表機 \_ 所有 \_ 存取                        | 若要執行所有管理工作和基本列印工作，除了同步處理 (請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) ) 。                                   |
| 一般安全性值，例如寫入 \_ DAC | 允許特定的控制存取權限。 請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ DEFAULTSW** (Unicode) 和 **\_ 印表機 \_ DEFAULTSA** (ANSI) <br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**版**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

