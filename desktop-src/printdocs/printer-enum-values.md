---
description: 印表機 \_ 列舉 \_ 值結構會指定 EnumPrinterDataEx 函數所傳回之印表機設定值的值名稱、類型和資料。
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: 'PRINTER_ENUM_VALUES 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974507"
---
# <a name="printer_enum_values-structure"></a>印表機 \_ 列舉 \_ 值結構

**印表機 \_ 列舉 \_ 值** 結構會指定 [**EnumPrinterDataEx**](enumprinterdataex.md)函數所傳回之印表機設定值的值名稱、類型和資料。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a>成員

<dl> <dt>

**pValueName**
</dt> <dd>

以 null 結束的字串指標，指定抓取值的名稱。

</dd> <dt>

**cbValueName**
</dt> <dd>

**PValueName** 成員中的位元組數目，包括結束的 Null 字元。

</dd> <dt>

**dwType**
</dt> <dd>

表示 **.pdata** 成員所指向之資料類型的代碼。 如需可能的類型代碼清單，請參閱登錄 [數值型別](/windows/desktop/SysInfo/registry-value-types)。

</dd> <dt>

**.Pdata**
</dt> <dd>

緩衝區的指標，其中包含抓取值的資料。

</dd> <dt>

**cbData**
</dt> <dd>

在 **.pdata** 緩衝區中取出的位元組數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 列舉 \_ VALUESW** (Unicode) 和 **\_ 印表機 \_ 列舉 \_ VALUESA** (ANSI) <br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> </dl>

 

