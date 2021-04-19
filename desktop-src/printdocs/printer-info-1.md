---
description: 印表機 \_ 資訊 \_ 1 結構會指定一般印表機資訊。
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: 'PRINTER_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975759"
---
# <a name="printer_info_1-structure"></a>印表機 \_ 資訊 \_ 1 結構

**印表機 \_ 資訊 \_ 1** 結構會指定一般印表機資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**旗標**
</dt> <dd>

指定傳回之資料的相關資訊。 以下是這個成員的值。



| 值                    | 意義                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 印表機 \_ 列舉 \_ 展開    | 如果已啟用預設展開，列印提供者可以將此旗標設定為呼叫應用程式的提示，以進一步列舉此物件。 例如，列舉網域時，列印提供者可能會藉由設定此旗標來指出使用者的網域。 |
| 印表機 \_ 列舉 \_ 容器 | 如果設定此旗標，印表機物件可能會包含可列舉的物件。 例如，物件可能是包含印表機的列印伺服器。                                                                                                             |
| 印表機 \_ 列舉 \_ ICON1     | 表示在適當的情況下，應用程式應該會顯示將物件識別為最上層網路名稱（例如 Microsoft Windows Network）的圖示。                                                                                           |
| 印表機 \_ 列舉 \_ ICON2     | 表示在適當的情況下，應用程式應該會顯示將物件識別為網路網域的圖示。                                                                                                                                  |
| 印表機 \_ 列舉 \_ ICON3     | 表示在適當的情況下，應用程式應該會顯示將物件識別為列印伺服器的圖示。                                                                                                                                    |
| 印表機 \_ 列舉 \_ ICON4     | 保留的。                                                                                                                                                                                                                                                 |
| 印表機 \_ 列舉 \_ ICON5     | 保留的。                                                                                                                                                                                                                                                 |
| 印表機 \_ 列舉 \_ ICON6     | 保留的。                                                                                                                                                                                                                                                 |
| 印表機 \_ 列舉 \_ ICON7     | 保留的。                                                                                                                                                                                                                                                 |
| 印表機 \_ 列舉 \_ ICON8     | 表示在適當的情況下，應用程式應該會顯示將物件識別為印表機的圖示。                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

描述結構內容之以 null 結束的字串指標。

</dd> <dt>

**pName**
</dt> <dd>

以 null 結束的字串指標，該字串會命名結構的內容。

</dd> <dt>

**pComment**
</dt> <dd>

以 null 結束的字串指標，其中包含描述結構的其他資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 1a** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**>enumprinters**](enumprinters.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 3**](printer-info-3.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




