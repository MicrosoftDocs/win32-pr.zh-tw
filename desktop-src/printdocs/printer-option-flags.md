---
description: 指定以 OpenPrinter2 開啟之印表機的控制碼快取。
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: 'PRINTER_OPTION_FLAGS 列舉 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b8541ec00f0d53bf58a826ceb7d8b8a821008fb6a66c0fe3917ebc12822e0e5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091798"
---
# <a name="printer_option_flags-enumeration"></a>印表機 \_ 選項 \_ 旗標列舉

指定以 [**OpenPrinter2**](openprinter2.md)開啟之印表機的控制碼快取。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**印表機 \_ 選項 \_ 沒有快取 \_**
</dt> <dd>

控制碼不會被快取。 所有套用至 [**OpenPrinter2**](openprinter2.md) 所傳回之控制碼的函式都會移至遠端電腦。

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**印表機 \_ 選項快取 \_**
</dt> <dd>

會快取控制碼。 所有套用至 [**OpenPrinter2**](openprinter2.md) 所傳回之控制碼的函式都會移至本機快取。

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**印表機 \_ 選項 \_ 用戶端 \_ 變更**
</dt> <dd>

[**SetPrinter**](setprinter.md)會使用 [**OpenPrinter2**](openprinter2.md)傳回的控制碼來重新命名印表機連接。

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

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




