---
title: 使用 ADSI 擴充功能的優點
description: 擴充方法的執行方式視擴充功能寫入器而定。
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a680e1eefbc05dac84b3420bee23287eda2bd02325274532109544b04ff73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018141"
---
# <a name="benefits-of-using-adsi-extensions"></a>使用 ADSI 擴充功能的優點

擴充方法的執行方式視擴充功能寫入器而定。 延伸模組寫入器甚至可以完整地在目錄範圍之外執行方法。 例如，備份和還原軟體的開發人員計畫擴充稱為「 **電腦**」的物件。 開發人員必須建立兩個方法： **備份** 和 **還原**。 這些方法會從遠端在目錄中的 **電腦** 物件所指向的實體電腦上操作。 藉由作為擴充功能，此元件會存取 ADSI 基礎結構，而且 ADSI 用戶端會將其視為物件的整數部分。

下列案例描述建立 ADSI 延伸模組的情況很有利：

-   建立延伸模組，以將元件與目錄物件整合。 因為目錄中有一個 **使用者** 物件，所以 HR 開發人員可能會想要建立 ADSI 擴充功能，以在建立 **使用者** 時填入目錄中的其他資料。
-   如果元件需要目錄查閱，請建立延伸模組。 元件可能需要目錄做為查閱的起點。 例如，建立新的應用程式時。 應用程式物件 **ToolApp** 可以在目錄中發行。 您的應用程式可能會支援郵件伺服器集合上的狀態通知。 您決定將此應用程式設為 ADSI 擴充功能。

    現在，使用者可以在目錄中搜尋 **ToolApp** 的所有實例。 針對傳回的每個物件，使用者可能會發出對 **NotifyNow ()** 的呼叫。 應用程式或延伸模組可以在目錄中取得更多目前的物件資料，並以非同步方式通知每部伺服器。

-   建立擴充功能做為命名空間與程式設計模型之間的連接點。 例如，ISV invents 了列印服務的新物件模型。 目錄中已定義了 **列印佇列** 物件。 ISV 可以建立 ADSI 擴充功能，並將它與 **列印佇列** 物件產生關聯。 ADSI 使用者可以系結至 **列印佇列** 物件，並開始使用 ISV 的物件模型。 從 ADSI 用戶端的觀點來看，這個連接點是透明的。
-   建立延伸模組以簡化工作。 您可以藉由搜尋和設定物件或多個物件中的多個屬性，來完成目錄中的許多工。 藉由建立單一函式來操作多個屬性，它可簡化應用程式和腳本寫入器的開發工作。

針對 ADSI 用戶端，擴充功能以數種方式擴充 ADSI 程式設計環境：

-   建立 ADSI 用戶端的開發人員不需要學習新的程式設計模型。 延伸模組是 ADSI 的一部分。 它們會使用相同的架構來搜尋、資料操作以及保護物件的安全。
-   系統管理員可以使用擴充功能來管理已啟用目錄的相關應用程式。
-   擴充功能取用者可以將 ADSI 物件和延伸模組視為一個整合物件來查看。
-   現有的元件可以與 ADSI 整合，讓擴充功能得以利用現有的投資，並在元件之間建立協力功能。

ADSI 擴充功能的設計具有下列目標：

-   易於實行。 使用目前現有的 Microsoft 技術、Microsoft Visual C++ 開發系統，以及 Active Template Library，您可以快速建立擴充功能。
-   用戶端會看到一個 IDispatch。 從腳本和自動化寫入器的觀點來看，擴充方法和屬性會以透明的方式混合成一個 ADSI 物件。
-   獨立。 延伸模組寫入器可以獨立擴充 ADSI，而不需要事先瞭解現有的延伸模組。

請考慮此案例：公司開發人員或 ISV 需要開發備份程式。 此備份應用程式可讓系統管理員備份組織單位中的所有電腦。 使用 ADSI 擴充功能時，可以使用下列腳本。


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



**LastBackUp** 是一個屬性，而 **BackUpNow** 是延伸模組寫入器所提供的方法。 此程式碼會顯示擴充取用者和提供者的優點。 延伸模組寫入器不需要建立新的方式來篩選、搜尋及存取目錄。 擴充取用者不需要破解新的程式設計範例。 延伸模組寫入器所提供的新方法和屬性會視為 ADSI 的一部分。

 

 




