---
description: DOC \_ INFO \_ 2 結構描述將列印的檔。
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: 'DOC_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987729"
---
# <a name="doc_info_2-structure"></a>DOC \_ INFO \_ 2 結構

**DOC \_ INFO \_ 2** 結構描述將列印的檔。

## <a name="syntax"></a>語法


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a>成員

<dl> <dt>

**pDocName**
</dt> <dd>

指定檔案名稱之以 null 結束的字串指標。

</dd> <dt>

**pOutputFile**
</dt> <dd>

指定輸出檔名稱之以 null 結束的字串指標。

</dd> <dt>

**pDatatype**
</dt> <dd>

以 null 結束的字串指標，識別用來記錄檔的資料類型。

</dd> <dt>

**dwMode**
</dt> <dd>

通知「列印多工緩衝處理器」所要遵循的資料本質。 如果這個值為零，列印多工緩衝處理器會將後續呼叫 [**WritePrinter**](writeprinter.md) 所傳送的資料視為一般列印工作， (是否要將它進行多工緩衝處理，取決於印表機屬性) 。 如果此值為 DI \_ 通道，則只會開啟通道。 在此情況下，傳遞至 **WritePrinter** 後續呼叫的資料會傳送至印表機，或後續對 [**ReadPrinter**](readprinter.md) 的呼叫會從印表機取出資料。 這個模式會維持有效，直到呼叫 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) 為止。

</dd> <dt>

**JobId**
</dt> <dd>

保留供內部使用;應為零。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ Doc \_ 資訊 \_ 2w** (Unicode) 和 **\_ DOC \_ 資訊 \_ 2a** (ANSI) <br/>                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**ReadPrinter**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




