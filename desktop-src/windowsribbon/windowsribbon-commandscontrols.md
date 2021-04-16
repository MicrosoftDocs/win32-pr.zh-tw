---
title: 瞭解命令和控制項
description: 將邏輯與展示分開的設計原理，就是激勵 Windows 功能區架構 \ 郵件的命令呈現系統的設計原理，這是以設計模式為基礎的系統，其中的功能和行為會與公開這項功能的控制項分開執行。
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Windows 功能區，命令總覽
- 功能區，命令總覽
- Windows 功能區，控制項總覽
- 功能區、控制項總覽
- Windows 功能區的命令系統
- Windows 功能區的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104571519"
---
# <a name="understanding-commands-and-controls"></a>瞭解命令和控制項

將邏輯與展示分開的設計原理，就是激勵 Windows 功能區架構的命令呈現系統的設計原理，也就是以設計模式為基礎的系統，其中的功能和行為會與公開這項功能的控制項分開執行。

-   [簡介](#introduction)
-   [Windows 功能區命令系統](#the-windows-ribbon-command-system)
    -   [控制項](#understanding-commands-and-controls)
    -   [命令](#understanding-commands-and-controls)
    -   [作用中的命令體驗](#the-command-experience-in-action)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

本文討論功能區架構命令系統的設計。 它描述命令和控制項的概念，並探索它們如何一起運作，以提供豐富的命令體驗，並提供主機新的 UI 功能。

## <a name="the-windows-ribbon-command-system"></a>Windows 功能區命令系統

在功能區架構中，命令和控制項都是獨立的實體。 命令是一個不含標記法條件約束的抽象結構，表示特定工作或功能類別。 另一方面，控制項是透過功能區 UI 公開命令功能的實體物件。

這項區別能讓您定義無 UI 詳細資料的命令，並能夠在動作意圖上執行，而不需要管理叫用動作的方式。

### <a name="controls"></a>控制項

控制項是命令呈現所需的 UI 物件。 架構會根據使用者互動以及一組固有的屬性和行為，在執行時間呈現和管理它們。

也稱為彈性配置，架構管理的 UI 彈性是功能區的最大優點之一。 功能區控制項可透過架構相依或開發人員定義的版面配置範本，自動自行重新設定，而這些範本可以回應各種執行時間需求，而不需要撰寫任何一行簡報程式碼。 如需詳細資訊，請參閱 [透過大小定義自訂功能區和調整原則](windowsribbon-templates.md)。

除了調適型配置的優點之外，許多複雜的功能區控制項都能為特定的 UI 問題空間提供獨立的解決方案。 藉由提供精密的互動模型，功能區控制項（例如 FontControl 或 ColorPicker）可讓您透過實際字型或色彩屬性的屬性包，以更抽象的詞彙來運算元據，而不是透過標準 Windows 控制項的各種子控制項、列舉和索引值。

### <a name="commands"></a>命令

鬆散結合功能區控制項來公開其功能，命令執行是主應用程式的網域，並採用事件接聽程式、命令處理常式和各種命令屬性的形式。

命令會在具有唯一識別碼的功能區標記中宣告，或在編譯時指派標記編譯器產生的識別碼。 命令會透過命令名稱與控制項相關聯，但不同于控制項，其實際功能是在程式碼中定義，而這些程式碼會透過命令識別碼系結至特定的命令處理常式。

> [!Note]  
> 在編譯時，此識別碼會儲存在識別碼定義標頭檔中，該檔案會在功能區主應用程式中公開命令至其對應的命令處理常式。

 

每個命令都有一種基礎命令類型，在 [**UI \_ COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) 列舉中有詳細的述。

### <a name="the-command-experience-in-action"></a>作用中的命令體驗

功能區快速存取工具列會示範此命令模型的功能 (QAT) 。 QAT 可讓使用者輕鬆地針對功能區 UI 中的任何控制項定義自己的快捷方式。 當使用者在功能區控制項上按一下滑鼠右鍵，並從內容功能表選取 [ **加入至快速存取] 工具列** 時，會在執行時間將快捷方式動態加入至 QAT。

下圖顯示從命令的 [ **貼** 上] 和 [ **貼** 上] 命令（以 [**SplitButton**](windowsribbon-element-splitbutton.md) 控制項表示）在 Windows 7 繪圖的功能區中。

![microsoft 油漆功能區中 [貼上] splitbutton 的圖片。](images/overviews/paint-paste-splitbutton-ribbon.png)

下圖顯示來自命令的相同 **貼** 上和 **貼** 上，在 Windows 7 的功能區 QAT 中仍以 [**SplitButton**](windowsribbon-element-splitbutton.md) 控制項表示。

![microsoft 油漆 qat 中 [貼上] splitbutton 的圖片。](images/overviews/paint-paste-splitbutton-qat.png)

當控制項由 QAT 主控時，控制項的新實例會維護原始控制項的所有功能，而不需要其他事件接聽程式和命令處理常式來支援它。 這兩個控制項都透過共用命令識別碼系結至相同的功能區命令處理常式。 如此一來，無論叫用哪一個控制項，架構都會將兩者視為一個。

> [!Note]  
> 在設計階段將命令合併到 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 時，也會實現相同的優點。 在此情況下，不論 [**SplitButton**](windowsribbon-element-splitbutton.md) 控制項是否出現在功能區、QAT 或 **CoNtextPopup** 中，都可以使用貼入命令處理常式。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構簡介](windowsribbon-introduction.md)
</dt> <dt>

[建立功能區應用程式](windowsribbon-stepbystep.md)
</dt> <dt>

[使用功能區標記宣告命令和控制項](windowsribbon-schema.md)
</dt> </dl>

 

 