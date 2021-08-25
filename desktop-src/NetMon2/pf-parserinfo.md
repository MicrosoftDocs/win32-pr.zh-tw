---
description: PF \_ PARSERINFO 結構會一次定義一個剖析器。 在 PF \_ PARSERINFO 結構中，剖析器會由剖析器偵測到之通訊協定的相關資訊定義。
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: 'PF_PARSERINFO 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533e8dae6a009488998acd3232b062b423553b9df10f14ec97ef9ae2f8c55bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889938"
---
# <a name="pf_parserinfo-structure"></a>PF \_ PARSERINFO 結構

**PF \_ PARSERINFO** 結構會一次定義一個剖析器。 在 **PF \_ PARSERINFO** 結構中，剖析器會由剖析器偵測到之通訊協定的相關資訊定義。

## <a name="syntax"></a>語法


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**szProtocolName**
</dt> <dd>

剖析器偵測到的通訊協定名稱。

</dd> <dt>

**szComment**
</dt> <dd>

通訊協定的簡短描述。

</dd> <dt>

**szHelpFile**
</dt> <dd>

通訊協定說明檔的名稱（如果有的話）。

</dd> <dt>

**pWhoCanPrecedeMe**
</dt> <dd>

[Pf \_ FOLLOWSET](pf-followset.md)結構的指標，此結構會列出在 **PF \_ PARSERINFO** 結構所描述的通訊協定之前可以使用的通訊協定。 網路監視器將剖析器通訊協定新增至集合中所有通訊協定的 [*下列集合*](f.md) 。

</dd> <dt>

**pWhoCanFollowMe**
</dt> <dd>

[Pf \_ FOLLOWSET](pf-followset.md)結構的指標，此結構會列出可遵循 **PF \_ PARSERINFO** 結構所描述之通訊協定的通訊協定。 網路監視器將設定的通訊協定新增至剖析器通訊協定的 [*下列集合*](f.md) 。

</dd> <dt>

**pWhoHandsOffToMe**
</dt> <dd>

指向 pf [ \_ HANDOFFSET](pf-handoffset.md) 結構的指標，該結構會實際操作到 **pf \_ PARSERINFO** 結構所描述的通訊協定。 網路監視器會將剖析器通訊協定新增至集合中所有通訊協定的 [*遞交集*](h.md) 。

</dd> <dt>

**pWhoDoIHandOffTo**
</dt> <dd>

[PF \_ HANDOFFSET](pf-handoffset.md)結構的指標，此結構會列出剖析器通訊協定所用的通訊協定。 網路監視器將此集合的通訊協定新增至剖析器通訊協定的 [*遞交集*](h.md) 。

</dd> </dl>

## <a name="remarks"></a>備註

Pf **\_ PARSERINFO** 結構是在 **pf \_ PARSERDLLINFO** 結構中使用，以提供剖析器的描述。 網路監視器使用剖析器描述來更新 [*Parser.ini*](p.md) 檔和剖析器的 INI 檔案，其位於 **PF \_ PARSERINFO** 結構中所述的通訊協定之前和之後。

下列集合會指定遵循通訊協定的通訊協定。 當剖析器無法從通訊協定實例中的資料識別下一個通訊協定時，網路監視器會使用下列資料集。 下列集合會儲存在 [*Parser.ini*](p.md) 檔案中。 第一次安裝剖析器時，網路監視器會更新 **pWhoCanPrecedeMe** 和 **pWhoCanFollowMe** 中列出的下列剖析器通訊協定集。

遞交集會指定遵循通訊協定的通訊協定。 只有當剖析器可以從通訊協定實例中的資料識別下一個通訊協定時，剖析器才會使用一組遞交集。 每個剖析器的 INI 檔案中都會儲存一個遞交集。 第一次安裝剖析器時，網路監視器會更新 **pWhoHandsOffToMe** 和 **pWhoDoIHandOffTo** 中所列之剖析器通訊協定的遞交集。



| 如需相關資訊                                               | 請參閱                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。        | [解析 器](parsers.md)                                                       |
| 接下來的集合包含。                                        | [指定追蹤集](specifying-a-follow-set.md)                       |
| 哪些遞交集包含。                                       | [指定遞交集](specifying-a-handoff-set.md)                     |
| 剖析器 DLL 中包含了哪些進入點。                | [剖析器 DLL 架構](parser-dll-architecture.md)                       |
| 如何執行 **ParserAutoInstallInfo**  包含範例。 | [執行 ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




