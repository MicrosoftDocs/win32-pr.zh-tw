---
description: 定義處理 ITablet 介面事件的方法。
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: ITabletEventSink 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195111"
---
# <a name="itableteventsink-interface"></a>ITabletEventSink 介面

定義處理 [**ITablet 介面**](itablet.md) 事件的方法。

## <a name="members"></a>成員

**ITabletEventSink** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITabletEventSink** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITabletEventSink** 介面具有這些方法。



| 方法                                                        | 描述                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**CoNtextCreate**](itableteventsink-contextcreate.md)       | 建立新的平板電腦內容時發生。<br/>                                          |
| [**CoNtextDestroy**](itableteventsink-contextdestroy.md)     | 當 tablet 內容終結時發生。<br/>                                      |
| [**CursorDown**](itableteventsink-cursordown.md)             | 手寫筆提示接觸到數位化的平板電腦介面時發生。<br/>                    |
| [**CursorInRange**](itableteventsink-cursorinrange.md)       | 手寫筆進入數位板的偵測範圍內時發生。<br/>                 |
| [**CursorMove**](itableteventsink-cursormove.md)             | 發生于游標移至 tablet 數位化板上時。<br/>                               |
| [**CursorNew**](itableteventsink-cursornew.md)               | 當新的手寫筆新增至系統時發生。<br/>                                      |
| [**CursorOutOfRange**](itableteventsink-cursoroutofrange.md) | 手寫筆離開 tablet 的實體偵測範圍 (近) 時發生。<br/> |
| [**CursorUp**](itableteventsink-cursorup.md)                 | 發生于使用者從 tablet 數位板介面引發手寫筆時。<br/>         |
| [**封包**](itableteventsink-packets.md)                   | 手寫筆在數位板上移動時發生。<br/>                                    |
| [**SystemEvent**](itableteventsink-systemevent.md)           | 發生于可用的系統事件時。<br/>                                              |



 

## <a name="remarks"></a>備註

開發人員不應使用此介面。

下列程式碼說明如何定義 **ITabletEventSink** 介面。

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

