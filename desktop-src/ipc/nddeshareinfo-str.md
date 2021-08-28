---
description: 包含 NetDDE 共用資料庫管理員所維護的 DDE 共用屬性 (DSDM) 。
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: 'NDDESHAREINFO 結構 (Nddeapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 84d29bcf5e1e4d086ca60da619edf26640c583f238d4fa956b3edd696eceee1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481708"
---
# <a name="nddeshareinfo-structure"></a>NDDESHAREINFO 結構

\[不再支援網路 DDE。 Nddeapi.dll 存在於 Windows Vista 中，但所有的函式呼叫會傳回 NDDE \_ 未 \_ 執行。\]

包含 NetDDE 共用資料庫管理員所維護的 DDE 共用屬性 (DSDM) 。 與每個 DDE 共用相關聯的安全描述項不會透過此結構傳遞，但可透過特定的函式來存取。 NetDDE DSDM API 接受此結構來設定函數;針對取得函式，DSDM 會傳回封裝到所提供緩衝區中的結構，以及成員 **lpszShareName**、 **lpszAppTopicList** 和 **lpszItemList** 所參考的資料。

## <a name="syntax"></a>語法


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**lRevision**
</dt> <dd>

**NDDESHAREINFO** 結構的修訂層級。 目前修訂層級為1。

</dd> <dt>

**lpszShareName**
</dt> <dd>

共用的名稱。 這個字串 \_ 的長度不得超過 NDDESHARENAME 字元數上限。

</dd> <dt>

**lShareType**
</dt> <dd>

一或多個 DDE 共用類型。 這個成員可以是下列受支援之 DDE 共用類型的組合。



| 共用類型                                                                                                                                                                                                                           | 意義                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <dt>**共用 \_輸入 \_ 新**</dt>的 <dt>0x02</dt> </dl>          | 此共用包含 OLE 應用程式/主題配對。<br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <dt>**共用 \_輸入 \_ 舊**</dt>的 <dt>0x01</dt> </dl>          | 此共用包含一個 DDE 應用程式/主題配對。<br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <dt>**共用 \_輸入 \_ 靜態**</dt> <dt>0x04</dt> </dl> | 共用包含靜態應用程式/主題組。<br/> |



 

</dd> <dt>

**lpszAppTopicList**
</dt> <dd>

緩衝區的指標，其中包含 DDE、OLE 和靜態應用程式/主題配對之以 null 結束的字串。 緩衝區應該採用下列格式：

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

**fSharedFlag**
</dt> <dd>

如果這個成員是 **FALSE**，則 dde 共用將不允許遠端使用者透過使用 DDE 來進行通訊。 不過，本機使用者仍可透過 DDE 共用進行通訊。 如果相關聯的 DACL 授與存取權，則一律隱含本機用戶端連結。

</dd> <dt>

**fService**
</dt> <dd>

如果設定此成員，則在允許 DDE 通訊之前，DDE 共用將不會檢查目前的使用者是否已將其設定為受信任。

</dd> <dt>

**fStartAppFlag**
</dt> <dd>

如果已設定此成員，且共用受信任而無法啟動應用程式，則 NetDDE 會嘗試啟動 **lpszAppTopicList** 所指定的應用程式（如果它一開始無法與應用程式進行 DDE 交談）。

</dd> <dt>

**nCmdShow**
</dt> <dd>

當 NetDDE 啟動應用程式以起始 DDE 交談時，會透過 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)函式的 *nCmdShow* 參數，將此值傳送至應用程式。 它會定義要在其中顯示應用程式視窗的慣用模式。 只有在 **fStartAppFlag** 為作用中時，此參數才有意義。 在應用程式啟動時，登入的使用者也可以在將共用升級為受信任狀態時，覆寫此選項。 此成員的預設值為 SW \_ SHOWMAXIMIZED。

</dd> <dt>

**qModifyId**
</dt> <dd>

8位元組的序號，表示 DDE 共用的修改序號。 每當 [**NDdeShareSetInfo**](nddesharesetinfo.md) 或 [**NDdeSetShareSecurity**](nddesetsharesecurity.md) 呼叫修改了 DDE 共用時，就會變更這些值。

</dd> <dt>

**cNumItems**
</dt> <dd>

**LpszItemList** 中列出的專案數。 如果 **cNumItems** 為零，則 **lpszItemList** 是空的，而且共用資訊和相關聯的安全描述項會套用至相關聯應用程式所服務的所有專案。

</dd> <dt>

**lpszItemList**
</dt> <dd>

緩衝區的指標，其中包含以 null 終止的字串，可指定 DDE 交易中的用戶端應用程式可以要求或啟動建議迴圈的專案。 如果未列出任何專案，則 DDE 共用允許使用任何專案。 清單中的專案數必須符合 **cNumItems** 計數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 結構](network-dde-structures.md)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> <dt>

[**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

