---
description: 代表印表機選項。
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: 'PRINTER_OPTIONS 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993196"
---
# <a name="printer_options-structure"></a>印表機 \_ 選項結構

代表印表機選項。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

**印表機 \_ 選項** 結構的大小。

</dd> <dt>

**dwFlags**
</dt> <dd>

一組 [**印表機 \_ 選項 \_ 旗標**](printer-option-flags.md) ，指定其他函式將如何使用 [**OpenPrinter2**](openprinter2.md) 所傳回之印表機的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**印表機 \_ 選項 \_ 旗標**](printer-option-flags.md)
</dt> </dl>

 

 




