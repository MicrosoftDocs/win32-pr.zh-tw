---
description: 管理程式庫的總覽，以及使用 Tablet PC 平臺受管理程式庫的附注。
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: 使用受管理的程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1241787b680045d6c84b440717ced5426e4352d8c280ef58c1bb7f75c9fc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449242"
---
# <a name="using-the-managed-library"></a>使用受管理的程式庫

Common language runtime 是 Microsoft .NET Framework 的基礎。 您可以將 common language runtime 視為在運行時間管理程式碼的代理程式，提供核心服務，例如記憶體管理、執行緒管理和遠端處理，同時強制執行嚴格的程式碼安全性。 事實上，程式碼管理的概念是 common language runtime 的基本原則。 以 common language runtime 為目標的程式碼稱為 managed 程式碼。 不是以 common language runtime 為目標的程式碼稱為機器碼。

Framework 類別庫是一組完整的物件導向集合，可供您用來開發應用程式，範圍從傳統的命令列或圖形化使用者介面， (GUI) 應用程式，再到 ASP.NET 和 Web 服務所提供的最新創新。

Tablet PC Managed 程式庫包含一組受管理的物件，可延伸架構，以支援 Tablet PC 的手寫輸入和輸出，以及與其他電腦的資料交換。

## <a name="exceptions"></a>例外狀況

Tablet PC API 中的 managed 程式庫物件會包裝 COM 程式庫的實現。 當基礎 COM 程式庫物件或控制項傳回錯誤時，managed API 會擲回 ThrowExceptionForHR 例外狀況，以提供內部 COM 例外狀況的詳細資料。 您可以參考 COM 程式庫參考中的 HRESULT 值，以取得可能傳回之可能錯誤的詳細資料。

## <a name="object-comparison"></a>物件比較

針對 Tablet PC 平臺 Managed 程式庫中的所有物件，不會覆寫 [**Equals**](/previous-versions/windows/) 以正確地比較兩個相同的物件。 Managed 應用程式開發介面 (API) 不支援透過 **equals** 函式或 equals (= =) 運算子來比較物件是否相等。

## <a name="binding-to-the-latest-microsoftinkdll"></a>系結至最新的 Microsoft.Ink.dll

最新的 Microsoft.Ink.dll 元件是 Microsoft.Ink.dll 1.0 版和 Microsoft.Ink.15.dll 的相容取代。 在大部分情況下，您不需要對使用舊版元件所散發的應用程式進行任何變更。 不過，在某些情況下，您需要指示 common language runtime 載入器使用較新的動態連結程式庫， (DLL) 參考較舊的 Dll 的任何地方。

您必須使用下列技巧明確地系結至新元件的唯一時機，就是您的應用程式所使用的 1.5 1.0 元件，與參考較新版本元件的元件（例如1.7）以及這些元件可能交換資料的元件組合使用。

指示 common language runtime 載入器使用較新 DLL 的最佳方式，就是在應用層級重新導向元件版本。 您可以藉由將元件系結資訊放在應用程式的設定檔中，指定您的應用程式使用較新版本的元件。 如需在應用層級重新導向元件版本的詳細資訊，請參閱重新導向 [元件版本](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)，尤其是「在設定檔中指定元件系結」一節。

您將需要在與可執行檔相同的目錄中建立設定檔。 設定檔的名稱必須與可執行檔的名稱相同，後面接著 .config 的副檔名。 例如，MyApp.exe 的應用程式中，設定檔必須是 MyApp.exe.config 的檔案。 設定檔會使用 [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) 專案來強制所有先前的版本對應至最新版本，如下列範例所示：

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

如需設定檔的詳細資訊，包括如何為設定檔建立可延伸標記語言 (XML)  (XML) 的範例，請參閱 [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) 和重新導向 [元件版本](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)。

使用 microsoft Windows XP Tablet PC Edition 開發工具組1.7 和更新版本所建立的應用程式，會自動系結至新版的 microsoft Ink 元件。 如需元件系結的詳細資訊，請參閱 [執行時間如何找出元件](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp)。

> [!Note]  
> 使用 [分割](/previous-versions/ms583616(v=vs.100)) 類別或 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 類別的應用程式無法使用應用程式原則系結至更新的元件。 使用其中一種類別的應用程式必須繼續使用 Microsoft.Ink.15.dll 或在參考更新的元件之後重新編譯。

 

## <a name="working-with-events"></a>使用事件

如果任何 managed 物件的事件處理常式中的程式碼擲回例外狀況，則不會將例外狀況傳遞給使用者。 若要確保傳遞例外狀況，請在事件處理常式中針對 managed 事件使用 try-catch 區塊。

## <a name="managing-forms"></a>管理表單

[Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1)類別和其基類並未定義完成項。 若要清除表單上的資源，請撰寫提供完成項的子類別 (例如， \# 使用 ~) 呼叫 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1)的 C 函式。 若要進行清除，完成項會覆寫 Dispose，然後呼叫基類處置。 當布林值參數為 **FALSE** 時，請不要在 Dispose 方法中參考需要 [Finalize](/previous-versions/windows/)方法的其他物件，因為這些物件可能已經完成。 如需釋放資源的詳細資訊 [，請參閱 Finalize 方法和析構函數](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp)。

## <a name="forms-and-the-recognizercontext"></a>表單和 RecognizerCoNtext

[RecognizerCoNtext](/previous-versions/ms552546(v=vs.100)) 事件會在與表單所線上程不同的執行緒中執行。 Windows Forms 中的控制項系結至特定的執行緒，而且不是安全線程。 因此，您必須使用其中一個控制項的 invoke 方法，將呼叫封送處理至適當的執行緒。 控制項上的四個方法都是安全線程： [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1)、 [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1)、 [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)和 [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) 方法。 針對其他所有方法呼叫，請在從不同的執行緒呼叫時，使用其中一個 invoke 方法。 如需使用這些方法的詳細資訊，請參閱 [從執行緒操作控制項](/previous-versions/757y83z4(v=vs.140))。

## <a name="waiting-for-events"></a>等候事件

Tablet PC 環境為多執行緒。 使用 [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) 函式，而不是其他等候方法，以允許可重複使用的元件物件模型 (COM) 呼叫，以在應用程式等候事件時輸入您的多執行緒單元 (MTA) 。

## <a name="using-ink-strokes-collections"></a>使用筆墨筆劃集合

從[筆墨](/previous-versions/aa515768(v=msdn.10))物件取得之[筆劃](/previous-versions/ms552701(v=vs.100))集合的實例不會進行垃圾收集。 為了避免記憶體流失，每當您使用這些集合的其中一個時，請使用如下所示的 "using" 語句。


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>處置 Managed 物件和控制項

若要避免記憶體流失，您必須在物件或控制項超出範圍之前，于已附加事件處理常式的任何 Tablet PC 物件或控制項上明確呼叫 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法。

若要改善應用程式的效能，請在不再需要下列物件、控制項和集合時，手動處置這些物件、控制項和集合。

-   [分](/previous-versions/ms583616(v=vs.100))
-   [筆跡](/previous-versions/aa515768(v=msdn.10))
-   [InkCollector](/previous-versions/ms583683(v=vs.100))
-   [InkEdit](/previous-versions/ms552265(v=vs.100))
-   [InkOverlay](/previous-versions/ms552322(v=vs.100))
-   [InkPicture](/previous-versions/aa514604(v=msdn.10))
-   [PenInputPanel](/previous-versions/aa514041(v=msdn.10))
-   [RecognizerCoNtext](/previous-versions/ms552546(v=vs.100))
-   [中風](/previous-versions/ms552701(v=vs.100))

下列 C \# 範例示範使用 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法的某些案例。


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 