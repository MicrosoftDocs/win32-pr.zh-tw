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
ms.openlocfilehash: d7eb7be8443c6a49c670e0573a79831a7aacfd88087f6ab19de632223b8588c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091748"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |



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

 

 




