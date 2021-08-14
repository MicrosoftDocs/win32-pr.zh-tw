---
description: 說明如何使用 PenInputPanel 物件來編寫系統層級的 Tablet PC 輸入面板。
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: 使用 PenInputPanel 類別來設計輸入面板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d430b002fb967652aea046919ec7341a984f420f756fd936e8c68dbfce8c055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449380"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>使用 PenInputPanel 類別來設計輸入面板

\[[**PenInputPanel**](peninputpanel-class.md) 已被 [>textinput](/previous-versions/ms581554(v=vs.100))取代。 請參閱程式 [設計文字輸入面板](programming-the-text-input-panel.md)。\]

說明如何使用 [**PenInputPanel**](peninputpanel-class.md) 物件來編寫系統層級的 Tablet PC 輸入面板。

## <a name="input-panel-vs-the-peninputpanel-object"></a>輸入面板與 PenInputPanel 物件

在 Microsoft Windows XP Tablet pc Edition 1.0 版中，系統層級的 tablet pc 輸入面板會提供通用機制來完成跨 Windows 平臺的文字輸入，但不會提供程式設計的存取。 在 Windows XP Tablet PC Edition 軟體發展工具組 (SDK) 1.5 版和更新版本中， [**PenInputPanel**](peninputpanel-class.md)物件可讓您將文字輸入工具直接整合到您的應用程式，並提供先前未提供的控制層級。 從 Windows XP Tablet PC Edition 2005 開始，系統層級的輸入面板已升級為包含 **PenInputPanel** 物件提供的就地輸入功能，以及更多。

下圖顯示透過 [ [自動宣告表單範例](auto-claims-form-sample.md) ] 範例顯示的輸入面板。

![輸入面板會顯示在用於汽車宣告的表單上](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

輸入面板會將相同的就地輸入功能提供給 Windows XP Tablet PC Edition 2005 或更新版本上執行的任何應用程式，而不需要額外的程式碼，藉此取代 [**PenInputPanel**](peninputpanel-class.md) 。 本文說明如何使用 **PenInputPanel** 物件來提供回溯相容性。 已使用 **PenInputPanel** 物件的應用程式運作相同，不同之處在于應用程式是在 Windows XP Tablet PC Edition 2005 或更新版本上執行時，將會顯示輸入面板而不是 **PenInputPanel** 。

如果您正在開發 Tablet PC 的新應用程式，而且想要擁有就地使用者輸入解決方案，輸入面板會在 Windows XP Tablet PC Edition 2005 或更新版本上自動提供此應用程式。 不需要具現化 [**PenInputPanel**](peninputpanel-class.md) 物件。

## <a name="disabling-the-input-panel"></a>停用輸入面板

在某些情況下，您可能會想要停用輸入面板。 有兩種方法可達成這個目標。 您可以用程式設計的方式完成這項工作，或設定一個登錄專案來停用整個應用程式的輸入面板。

### <a name="disabling-input-panel-programmatically"></a>以程式設計方式停用輸入面板

若要以程式設計的方式停用輸入面板，請具現化 [**PenInputPanel**](peninputpanel-class.md) ，並 [**將其自動**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)**值** 屬性設定為


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



若要在單一應用程式中停用多個控制項的輸入面板，請為每個控制項具現化 [**PenInputPanel**](peninputpanel-class.md) 物件，並將每個控制項 [**的 [自動**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)] 屬性設定為 **False** ，或具現化單一 **PenInputPanel** ，並將其從控制項移至控制項，作為輸入焦點變更。 如需這兩種技術的詳細資訊，請參閱 [PenInputPanel 範例](peninputpanel-sample.md) 主題。

### <a name="disabling-input-panel-through-the-registry"></a>透過登錄停用輸入面板

您可以設定一個登錄專案，以停用整個應用程式的輸入面板。 不過，這也會對一般對話方塊停用它，例如 [ **開啟** 檔案] 對話方塊、[ **列印** ] 對話方塊和 [ **儲存** 盤案] 對話方塊。 這可能會讓應用程式中的使用者體驗與其他 Tablet PC 應用程式不一致。

將 `DisableInPlace` 登錄機碼設定為零，可避免在應用程式中出現輸入面板使用者介面 (UI) 。 您必須將登錄機 `DisableInPlace` 碼放在 `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` 。 然後，使用您要在其中停用輸入面板的應用程式完整路徑來新增登錄值。 下列範例登錄專案會在名為 MyApp 的應用程式中停用輸入面板：

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

如果您在停用輸入面板 UI 之後仍看到應用程式發生問題，可能需要停用基礎架構，以查詢您的應用程式是否有插入號位置。 例如，輸入面板可能會在應用程式的插入號追蹤程式碼中公開 bug。 關閉插入號追蹤查詢也可防止輸入面板 UI 出現。 若要停用架構，請將登錄機 `EnableCaretTracking` 碼設定為零。 在上找出此金鑰 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` 。

> [!Note]  
> Windows XP 中的協助工具工具和語音技術也會使用此架構，因此停用查詢也會在您的應用程式中停用這些功能。

 

## <a name="the-input-panel-and-web-pages"></a>輸入面板和網頁

為了在網頁上使用 API，它必須在部分信任環境中運作。 所有 [**PenInputPanel**](peninputpanel-class.md) 類別成員都需要完全信任，但下列除外：

-   僅 (managed 程式碼) 的[PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90))函式
-   [Dispose 方法](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (僅限 managed 程式碼) 
-   [AttachedEditControl 屬性](/previous-versions/ms582239(v=vs.100)) (僅限 managed 程式碼) 
-   [**自動屬性**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

這些 Api 會在部分信任環境中運作，例如網頁，可讓您具現化 [**PenInputPanel**](peninputpanel-class.md) 物件、將它附加至控制項，以及停用該控制項的輸入面板。 如需詳細資訊，請參閱使用 [網頁上](ink-on-the-web.md)的 PenInputPanel 類別和筆墨來設計輸入面板。

## <a name="the-peninputpanel-object"></a>PenInputPanel 物件

本主題的其餘部分將說明如何在啟用 Tablet PC 的應用程式中使用 [**PenInputPanel**](peninputpanel-class.md) 物件。 更具體來說，本主題會參考 **PenInputPanel** 物件在討論程式設計物件時，參考 UI 元素時的 [畫筆輸入面板]，而 [電腦輸入面板] (或 [輸入面板]) 參考到 Tablet PC 螢幕側邊的全域輸入面板。

下列各節說明 [**PenInputPanel**](peninputpanel-class.md) 物件和 UI。

-   [關於輸入面板](about-the-input-panel.md)
-   [具現化 PenInputPanel 類別](instantiating-the-peninputpanel-class.md)
-   [模擬支援](factoid-support.md)
-   [Text Services Framework (TSF)](text-services-framework.md)
-   [最佳作法](best-practices.md)

 

 
