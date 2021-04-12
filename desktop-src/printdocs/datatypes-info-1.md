---
description: 資料類型 \_ 資訊 \_ 1 結構包含用來記錄列印工作之資料類型的相關資訊。
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: 'DATATYPES_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192725"
---
# <a name="datatypes_info_1-structure"></a>資料類型 \_ 資訊 \_ 1 結構

資料 **類型 \_ 資訊 \_ 1** 結構包含用來記錄列印工作之資料類型的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**pName**
</dt> <dd>

以 null 結束的字串指標，識別用來記錄列印工作的資料類型。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 資料類型 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 資料類型 \_ 資訊 \_ 1a** (ANSI) <br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




