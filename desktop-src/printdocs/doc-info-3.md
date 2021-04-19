---
description: DOC \_ 資訊 \_ 3 結構描述將列印的檔。
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: 'DOC_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987515"
---
# <a name="doc_info_3-structure"></a>DOC \_ 資訊 \_ 3 結構

**DOC \_ 資訊 \_ 3** 結構描述將列印的檔。

## <a name="syntax"></a>語法


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
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

**dwFlags**
</dt> <dd>

標誌。 目前，它可以是 **Null** 或下列值。



| 旗標                 | 意義                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| DI \_ MEMORYMAP \_ 寫入 | 讓 [**StartDocPrinter**](startdocprinter.md) 不會使用 [**system.printing.printqueue.addjob**](addjob.md) 和 [**ScheduleJob**](schedulejob.md) 進行本機列印。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

\_ \_ **DOC \_ 資訊 \_ 3** 中的 DI MEMORYMAP 寫入設定是一項優化。 這可讓 GDI 在應用程式中對應多工緩衝處理檔案，並加速錄製。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ Doc \_ 資訊 \_ 3w 法** (Unicode) 和 **\_ doc \_ 資訊 \_ 3a** (ANSI) <br/>                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**System.printing.printqueue.addjob**](addjob.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




