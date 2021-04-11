---
description: PF \_ PARSERDLLINFO 結構會定義位於剖析器 DLL 中的剖析器。
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: 'PF_PARSERDLLINFO 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944639"
---
# <a name="pf_parserdllinfo-structure"></a>PF \_ PARSERDLLINFO 結構

**PF \_ PARSERDLLINFO** 結構會定義位於剖析器 DLL 中的剖析器。

## <a name="syntax"></a>語法


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**nParsers**
</dt> <dd>

剖析器 DLL 中的剖析器數目。

</dd> <dt>

**ParserInfo**
</dt> <dd>

[PF \_ PARSERINFO](pf-parserinfo.md)結構的陣列，描述剖析器 DLL 中的每個剖析器。

</dd> </dl>

## <a name="remarks"></a>備註

在剖析器 DLL 中執行的 [ParserAutoInstallInfo](parserautoinstallinfo.md)匯出函數會傳回 **PF \_ PARSERDLLINFO** 結構。 **ParserAutoInstallInfo** 函式會識別 DLL 中的剖析器數目，並使用 [PF \_ PARSERINFO](pf-parserinfo.md)結構的陣列來描述每個剖析器。

您 \_ 必須使用 **HeapAlloc** 來配置 PF PARSERDLLINFO 結構。



| 如需相關資訊                                               | 請參閱                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。        | [解析 器](parsers.md)                                                      |
| 剖析器 DLL 中包含的進入點。               | [剖析器 DLL 架構](parser-dll-architecture.md)                      |
| 如何執行 **ParserAutoInstallInfo**  包含範例。 | [執行 ParserAutoIstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> </dl>

 

 




