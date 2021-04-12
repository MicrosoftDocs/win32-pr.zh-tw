---
description: DOC \_ INFO \_ 1 結構描述將列印的檔。
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: 'DOC_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192604"
---
# <a name="doc_info_1-structure"></a>DOC \_ INFO \_ 1 結構

**DOC \_ INFO \_ 1** 結構描述將列印的檔。

## <a name="syntax"></a>語法


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**pDocName**
</dt> <dd>

指定檔案名稱之以 null 結束的字串指標。

</dd> <dt>

**pOutputFile**
</dt> <dd>

指定輸出檔名稱之以 null 結束的字串指標。 若要列印至印表機，請將此 **值** 設定為 Null。

</dd> <dt>

**pDatatype**
</dt> <dd>

以 null 結束的字串指標，識別用來記錄檔的資料類型。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ Doc \_ 資訊 \_ 1W** (Unicode) 和 **\_ doc \_ info \_ 1a** (ANSI) <br/>                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




