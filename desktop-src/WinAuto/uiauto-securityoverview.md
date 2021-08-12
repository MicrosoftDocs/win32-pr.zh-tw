---
title: 輔助技術的安全性考慮
description: 輔助技術是在 Windows 桌面上執行的應用程式，可協助協助工具使用者與作業系統和電腦上執行的其他應用程式（包括新的 Windows UI 中的應用程式）互動。
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- uiAccess 屬性
- 消費者介面自動化，uiAccess 屬性
- security、uiAccess 屬性
- 並無 requestedexecutionlevel 標記
- 消費者介面自動化，並無 requestedexecutionlevel 標記
- 消費者介面自動化，安全性考慮
- 消費者介面自動化，資訊清單檔
- 資訊清單檔
- 使用者帳戶控制
- 安全性，使用者帳戶控制
- 安全性，資訊清單檔
- 安全性，並無 requestedexecutionlevel 標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88ba97be98795be3725efaf76cf01297d7a00a2bb0112b0211581b3e0e4035f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563961"
---
# <a name="security-considerations-for-assistive-technologies"></a>輔助技術的安全性考慮

輔助技術是在 Windows 桌面上執行的應用程式，可協助協助工具使用者與作業系統和電腦上執行的其他應用程式互動，包括新的 Windows UI 中的應用程式。 輔助技術應用程式的運作方式是從作業系統和其他應用程式中取出資訊，然後以使用者可存取的方式來呈現資訊。 輔助技術應用程式也可以根據使用者的輸入，以程式設計方式「驅動」作業系統和其他應用程式。

輔助技術應用程式的本質需要它們跨進程界限，而且它們可以存取以較高完整性層級執行的進程， (IL) 。  (在中 IL 執行的輔助技術應用程式。 ) 例如，當使用者嘗試執行需要系統管理許可權的工作時，Windows 會顯示對話方塊，詢問使用者是否同意繼續進行。 此對話方塊會在較高的 IL 上執行，以保護它免于跨進程通訊，讓惡意軟體無法模擬使用者輸入。 同樣地，桌面登入畫面會在較高的 IL 上執行，以防止其他進程存取。

輔助技術應用程式通常需要存取受保護的系統 UI 元素或其他可能以較高許可權層級執行的進程。 因此，輔助技術應用程式必須受系統信任，且必須以特殊許可權執行。

若要取得更高 IL 程式的存取權，輔助技術應用程式必須在應用程式資訊清單中設定 UIAccess 旗標，並由具有系統管理員許可權的使用者啟動。

> [!NOTE]
> 存取權限的限制如下：
>
> - 在資訊清單中沒有 UIAccess 的應用程式是以 medium IL 開頭，且無法存取提升的 ( "medium +" IL) 進程 UI。
> - 在資訊清單中具有 UIAccess 的應用程式，以及不在 administrators 群組中的使用者啟動的應用程式，會以「中 +」 IL 的形式啟動，而且無法存取提升許可權的 UI (不會以「高」 IL 的形式執行，例如透過以 **滑鼠右鍵按一下 > 以系統管理員身分執行的** 應用程式) 。
> - 應用程式具有 UI 存取權，且由系統管理員使用者啟動為「高」 IL，並且可以存取提高許可權的 UI，因為它具有相同的 IL。
>
> UIAccess 沒有足夠的進程，無法在 IL 界限中向上移動。

除了可以存取更高 IL 程式之外，具有這些許可權的輔助技術應用程式可以隨時以 z 順序的最上層應用程式執行，這表示在使用者需要時，可以看到輔助技術應用程式並可供使用。

> [!Important]
> 先前所列的案例都沒有提供在 system IL 下執行之 UI 的存取權。 只有在使用者帳戶控制中啟動進程時，才可能這樣做， (在 SYSTEM (和 system IL) 下的 UAC) desktop。 在此情況下，設定 UIAccess 沒有任何作用。

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>輔助技術應用程式的 UIAccess 需求

輔助技術應用程式是一種 Windows Windows 桌面應用程式，可與桌面上和新的 Windows UI 中執行的其他進程互動，以取得系統和應用程式的資訊。 輔助技術應用程式接著可以提供資訊給協助工具使用者。

輔助技術應用程式會在應用程式資訊清單中設定 UIAccess 旗標，以取得其他進程的存取權。 若要使用 UIAccess 旗標，輔助技術應用程式必須符合下列需求。

-   需要顯示、與其他應用程式互動或反映資訊，以提供協助工具案例的資訊，以及/或
-   需要以最上層視窗的形式執行，才能取得或顯示此資訊。

若要使用 UIAccess，輔助技術應用程式必須：

-   使用憑證進行簽署，以與以較高許可權層級執行的應用程式互動。
-   由系統信任。 應用程式必須安裝在需要使用者帳戶控制 (UAC) 提示進行存取的安全位置。 例如，[Program Files] 資料夾。
-   使用包含 uiAccess 旗標的資訊清單檔來建立。

不應使用 UIAccess：

-   不是輔助技術的應用程式。
-   由輔助技術應用程式顯示與其目標的協助工具案例無關的資訊或 UI。
-   由只想顯示新的 Windows UI 中其他應用程式的應用程式。
    > [!Note]  
    > 針對新的 Windows UI 開發的應用程式沒有 UIAccess 作為可用的選項。

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>在應用程式資訊清單檔中設定 UIAccess

若要取得受保護系統 UI 的存取權，您必須使用資訊清單檔案來建立應用程式，而資訊清單檔中必須包含特殊屬性。 此 **uiAccess** 屬性包含在 **並無 requestedexecutionlevel** 標記中，如下列程式碼範例所示。


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



此程式碼中的 **level** 屬性值僅為範例。

**UIAccess** 預設為 "false"。 如果省略此屬性，或沒有資訊清單，應用程式將無法取得受保護 UI 的存取權。

如需有關 Windows 安全性、簽署應用程式以及建立資訊清單的詳細資訊，請參閱[Windows Vista 和 Windows Server 2008 開發人員故事： Windows MSDN 上的使用者帳戶控制 (的 vista 應用程式開發需求) UAC](/previous-versions/aa905330(v=msdn.10)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 自動化基礎](entry-uiautocore-overview.md)
</dt> </dl>

 

 