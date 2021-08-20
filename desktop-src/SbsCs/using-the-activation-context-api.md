---
description: 應用程式可以直接呼叫啟用內容函式來管理啟用內容。
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: 使用啟用內容 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c2f3d1c1a6b6202619b9e39df6ee4dc60b9134ebefa9cfe7dea4db9a344bd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073298"
---
# <a name="using-the-activation-context-api"></a>使用啟用內容 API

應用程式可以直接呼叫啟用內容函式來管理 [啟用內容](activation-contexts.md) 。 啟用內容是記憶體中的資料結構。 系統可以使用啟用內容中的資訊，將應用程式重新導向以載入特定 DLL 版本、COM 物件實例或自訂視窗版本。 如需詳細資訊，請參閱 [啟用內容參考](activation-context-reference.md)。

 (API) 的應用程式開發介面可以用來管理啟用內容，並使用 [資訊清單](manifests.md)來建立版本命名的物件。 下列兩個案例說明應用程式如何藉由直接呼叫啟用內容函式來管理啟用內容。 不過，在大部分情況下，啟用內容是由系統所管理。 應用程式開發人員和元件提供者通常不需要對堆疊進行呼叫來管理啟用內容。

-   執行間接取值或分派層的進程和應用程式。

    例如，在事件迴圈中管理啟用內容的使用者。 每次存取視窗時（例如將滑鼠移至視窗上方）都會呼叫 [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) ，以啟動資源目前的啟用內容，如下列程式碼片段所示。

    <dl> 處理 hActCtx;  
    CreateWindow () ;  
    ...  
    GetCurrentActCtx (&ActCtx) ;  
    ...  
    ReleaseActCtx (&ActCtx) ;  
    </dl>

    在下列程式碼片段中，API 函式會先啟用適當的啟用內容，然後再呼叫 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)。 當呼叫 **CallWindowProc** 時，它會使用此內容將訊息傳遞至 Windows。 當所有資源作業都完成時，此函式將會停用內容。

    <dl> ULONG \_ PTR ulpCookie;  
    處理 hActCtx;  
    如果 (ActivateActCtx (hActCtx，&ulpCookie) )   
    {  
    ...  
    CallWindowProc ( ... ) ;  
    ...  
    DeactivateActCtx (0、ulpCookie) ;  
    }  
    </dl>

-   Delegator 分派層。

    此案例適用于使用通用 API 層（例如驅動程式管理員）管理多個實體的管理員。 雖然尚未實作為範例，但這是 ODBC 驅動程式。

    在此案例中，仲介層將能夠處理元件系結。 若要取得版本特定的系結驅動程式，發行者必須提供資訊清單，並指定該資訊清單中特定元件的相依性。 基底應用程式不會動態繫結至元件;在執行時間，驅動程式管理員會管理呼叫。 當根據連接字串呼叫 ODBC 驅動程式時，它會載入適當的驅動程式。 然後，它會使用組件資訊清單檔中的資訊來建立啟用內容。

    如果沒有資訊清單，驅動程式的預設動作會使用與應用程式所指定的相同內容，在此範例中為 MSVCRT.LIB 的第2版。 因為資訊清單存在，所以會建立個別的啟用內容。 當 ODBC 驅動程式執行時，它會系結至 MSVCRT.LIB 元件的第1版。

    每次驅動程式管理員呼叫分派層時（例如，取得下一組資料），就會根據啟用內容使用適當的元件。 下列程式碼片段說明這一點。

    <dl> 處理 hActCtx;  
    ULONG \_ PTR ulpCookie;  
    ACTCTX ActCtxToCreate = {...};  
    hActCtx = CreateActCtx (&ActCtxToCreate) ;  
    ...;  
    如果 (ActivateActCtx (hActCtx，&ulpCookie) )   
    {  
    ...  
    ConnectDb ( ... ) ;  
    DeactivateActCtx (0、ulpCookie) ;  
    }  
    ...  
    ReleaseActCtx (hActCtx) ;  
    </dl>

 

 
