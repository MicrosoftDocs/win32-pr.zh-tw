---
description: 使用 MS Shell Dlg 和 MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: 使用 MS Shell Dlg 和 MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad43f972e776151551fa312ce2bd8ed6d19be58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975540"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>使用 MS Shell Dlg 和 MS Shell Dlg 2

Windows 提供許多語言的當地語系化版本。 但是，英文版也可以用來執行以英文以外的語言撰寫的應用程式。 即使用於這些語言的腳本不同，這也是如此，因為應用程式是以希臘文或日文撰寫的。 這些應用程式需要具有對話方塊、圖示與公用程式的使用者介面，以提供應用程式語言的資訊，這可能與目前 Windows 使用者介面中使用的語言不同。

選取使用者介面字型的問題很明顯。 例如，shell 字型也稱為「系統」或「預設字型」（英文） (美國) Windows 98 是 MS Sans Serif，而希臘文 (希臘的 shell 字型則) Windows 98 是 MS Sans Serif 希臘文。 針對日文 (日本) Windows 98，shell 字型是 MS UI Mt。 這些字元集無法直接彼此對應。 當地區設定設定為希臘文時，將 MS sans Serif 取代為 MS Sans Serif 希臘文 (希臘) 不允許現有的應用程式適當地執行，或在系統功能表、對話方塊和編輯控制項中顯示希臘文字元。

Windows 會使用 MS Shell Dlg 和 MS Shell Dlg 2 邏輯字型，讓您選取適當的字型來顯示腳本，以解決這個問題。 本節說明使用邏輯字型來實作為對話方塊、功能表，以及在所有支援的 Windows 作業系統上以及所有語言都能妥善顯示的彈性使用者介面等的一些程式設計考慮。 如需詳細資訊，請參閱 [建立和選取字型](../gdi/font-creation-and-selection.md)。 另請參閱 [多語系消費者介面](multilingual-user-interface.md) ，以瞭解如何使用多語系消費者介面 (MUI) 技術來建立多語系應用程式的使用者介面。

## <a name="about-the-logical-fonts"></a>關於邏輯字型

MS Shell Dlg 和 MS Shell Dlg 2 邏輯字型基本上是用來對應的臉部名稱，可支援具有不包含在字碼頁1252（美國和西歐的 Windows 字元集）中之字元的地區設定/文化特性。 MS Shell Dlg 對應至與目前文化特性/地區設定相關聯的預設 Shell 字型，並支援傳統 Windows 桌面外觀。 MS Shell Dlg 2 臉部名稱是在 Windows 2000 中引進，以支援 Windows 2000 所引進的外觀。

例如，如果您的應用程式在其對話方塊中使用 MS Shell Dlg 或 MS Shell Dlg 2，則為您的應用程式建立希臘文語言資源的當地語系化小組可專注于翻譯文字。 他們不必擔心 MS Sans Serif 和 MS Sans Serif 希臘文等問題。

> [!Note]  
> 在不同的 Windows 版本上，MS Shell Dlg 和 MS Shell Dlg 2 所產生的字型會不同。 因此，您應該確定您的使用者介面元素在所有平臺上都能正常顯示。

 

## <a name="handle-hard-coded-font-names"></a>處理 Hard-Coded 字型名稱

使用 Unicode 可讓應用程式處理數千個不同的字元，但大部分的字型都不會涵蓋所有的 Unicode 字元集。 您的應用程式不應將字型名稱硬式編碼。 其中一個原因是，對顯示一種語言字元的字型名稱進行硬式編碼，而不是另一種語言的字元，則會導致第二種語言的所有當地語系化文字都不正確地顯示。 另一個不是以硬式編碼字型名稱的原因是，所需的字型可能不會在顯示應用程式文字的作業系統上載入。

處理字型名稱的最佳方式是將它們視為可當地語系化的資源。 使用邏輯字型可解決使用任何語言在 Windows NT 或 Windows 2000 上使用任何語言執行介面的問題。 將字型名稱設定為可當地語系化的資源，可以讓您的當地語系化人員變更當地語系化使用者介面的字型。

## <a name="handle-hard-coded-font-sizes"></a>處理 Hard-Coded 字型大小

有些腳本很複雜，而且需要大量的圖元才能正確顯示。 例如，大部分的英文字元都會顯示在5x7 方格中，但日文字元至少需要16格才能清楚看到。 雖然中文需要24x24 格線，但泰文只需要8圖元的寬度，但至少需要22圖元的高度。 很容易瞭解，某些字元可能無法以小型字型大小來辨認。

您的應用程式使用者介面應該將字型大小視為可當地語系化的資源。 使用邏輯字型可解決使用任何語言在 Windows NT 或 Windows 2000 上使用任何語言執行介面的問題。 將字型大小設定為可當地語系化的資源，可讓您的當地語系化人員變更當地語系化使用者介面的字型。

## <a name="map-the-logical-fonts"></a>對應邏輯字型

每個邏輯字型都是由登錄中的專案對應到目前作用中地區設定的適當 shell 字型。 當使用其中一個邏輯字型時，Windows 會在執行時間切換到目前所選地區設定的字型。 這項作業可讓您正確地顯示英文 (美國) Windows 使用者介面，以及不在字碼頁1252中的字元。 因此，目前交付當地語系化的應用程式可以在英文 (的 Windows) 版本的 Windows 上執行，而不需要修改。

每一部 Windows 電腦都會根據 [NLS 術語](nls-terminology.md)中所述的非 Unicode 程式所定義的語言，將 Ms shell DLG 和 Ms shell dlg 2 對應到適當的實體字型。 實際的對應會儲存在登錄機碼中 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ 目前 \\ 的版本 FontSubstitutes。

### <a name="font-mapping-on-windows-me9895"></a>Windows Me/98/95 的字型對應

MS Shell Dlg 通常會對應至字碼頁特定版本的 MS Sans Serif。

### <a name="font-mapping-on-windows-nt-40"></a>Windows NT 4.0 上的字型對應

使用斯拉夫腳本，MS Shell Dlg 可對應至適用于西方和歐洲西部的 MS Sans Serif、希臘文、土耳其文、波羅的海文和語言;MS UI Mt （日文）;適用于韓文的 Gulim;適用于簡體中文的 Simsun;繁體中文的 PMinglu;等。

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Windows 2000、Windows XP、Windows Server 2003、Windows Vista 和 Windows 7 上的字型對應

這兩個邏輯字型都對應至以 Unicode 為基礎的 TrueType 字型。 只要安裝語言不是日文，MS Shell Dlg 就會使用 Microsoft Sans Serif (有別于 MS Sans Serif) 。 如果安裝語言為日文，則 MS Shell Dlg 會對應至 MS UI Mt。

在 Windows XP MUI 系統上，只有當系統地區設定和 UI 語言設定為日文時，MS Shell Dlg 才會對應至 MS UI。 否則，MS Shell Dlg 會對應至 Microsoft Sans Serif。

在 Windows Vista 和 Windows 7 上，如果電腦預設的 UI 語言設定為日文 (（不論安裝語言) 為何），MS Shell Dlg 會對應至 MS UI Mt。 如果電腦預設 UI 語言設定為日文以外的語言，則 MS Shell Dlg 會對應至 Microsoft Sans Serif。

無論語言為何，MS Shell Dlg 2 都只會使用 Tahoma 字型。 Tahoma over Microsoft Sans Serif 的主要優點是，Tahoma 具有原生粗體字型。 它的主要缺點是，較舊的作業系統可能尚未安裝，而且可能會替代較不吸引人的字型。

未在 Tahoma 或 Microsoft Sans Serif 中執行的字元，可能會在用於使用者介面文字顯示的其他 Windows 字型中執行。 根據用來顯示文字的控制項或 Api 而定，系統可能會使用各種機制（例如 [字型連結](https://msdn.microsoft.com/globalization/mt662331) ）來自動選取這類字型來顯示這些字元。

應用程式可以明確地使用 Microsoft Sans Serif 或 Tahoma，並儲存與使用 MS Shell Dlg 或 MS Shell Dlg 2 相關的間接取值層級。 由於字型連結的原因，指定 Microsoft Sans Serif 或 Tahoma 可提供適用于所有語言的適當字型。

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>在 Windows Me/98/95 上針對非英文應用程式使用 MS Shell Dlg

在 Windows Me/98/95 上，MS Shell Dlg 不適合搭配靜態的非英文使用者介面應用程式使用，此應用程式會在使用者選擇具有不同 Windows 基底字元集的地區設定時執行。 在這種情況下，應用程式使用者介面語言可能不支援使用以 MS Shell Dlg 取代的字型。

例如，如果使用者使用德文版的 Windows，而且想要安裝非 Unicode 希臘文語言的應用程式，則使用者會嘗試將地區設定變更為希臘文 (希臘) 。 此動作會將 MS Shell Dlg 重設為希臘文字型，但這個字型未包含以德文顯示的所有必要字元。 因此，德文語言使用者介面中的任何非 ASCII 字元都不會正確顯示。 若要支援這種情況，應用程式必須將 MS Shell Dlg 設定為包含西歐和希臘文字元的字型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[國際字型列舉和選取](using-international-fonts-and-text.md)
</dt> <dt>

[多語系使用者介面](multilingual-user-interface.md)
</dt> </dl>

 

 
