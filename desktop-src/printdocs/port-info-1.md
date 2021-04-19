---
description: 埠 \_ 資訊 \_ 1 結構會識別支援的印表機埠。
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: 'PORT_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981566"
---
# <a name="port_info_1-structure"></a>埠 \_ 資訊 \_ 1 結構

**埠 \_ 資訊 \_ 1** 結構會識別支援的印表機埠。

## <a name="syntax"></a>語法


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**pName**
</dt> <dd>

識別支援之印表機埠 (以 null 終止的字串指標，例如 "LPT1：" ) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 埠 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 埠 \_ 資訊 \_ 1a** (ANSI) <br/>                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




