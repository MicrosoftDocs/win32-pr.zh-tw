---
description: 本主題將協助您開始建立可供使用的應用程式，方法是指定必要條件、摘要技術，以及引入入門教學課程。
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: 使用國際 Windows 開發開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c346f03717b5f50c27911891daaea8aa4ed55ce199e7ca807690d2f3185d8114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949427"
---
# <a name="getting-started-with-international-windows-development"></a>使用國際 Windows 開發開始使用

本主題將協助您開始建立可供使用的應用程式，方法是指定必要條件、摘要技術，以及引入入門教學課程。

## <a name="getting-started"></a>開始使用

如果您為使用者撰寫單一地區設定的應用程式，即使您使用地區設定特定的假設來設計這些應用程式，也可以成功，例如以特定格式呈現日期，或以特定順序排序字串。 但現在您必須確保應用程式可以在多個國家（地區）使用不同語言和不同文化特性的使用者使用。 若要在多個地區設定中成功，應用程式必須調整為執行所在的地區設定。 無論您是將它新增至現有的應用程式，或是將它設計成新的應用程式，這種彈性都很重要。

本節可協助您開始進行國際開發。 其中提供的主題連結可提供國際化的先決條件。 其中摘要說明 SDK 提供的技術，以支援全球客戶。 最後，本節提供的範例應用程式可解決您在撰寫全域軟體時經常遇到的問題。

## <a name="prerequisites"></a>必要條件

您應該熟悉針對 Windows 開發國際軟體所產生的問題。 請從這些總覽著手。

-   [瞭解國際化](understanding-internationalization.md) 可解釋開發全球化應用程式的額外困難，並定義重要詞彙。
-   「 [取得全球可用](https://msdn.microsoft.com/goglobal/bb895995.aspx) 」主題將引導您瞭解您可以流覽的指導方針和最佳作法，或視需要深入探討。
-   [國際化檢查清單](internationalization-checklist.md)摘要說明建立全球化應用程式所應採取的動作。
-   安全性一直是軟體發展的問題，但是您必須在開發國際軟體時考慮其他問題。 請參閱 [安全性考慮：國際功能](security-considerations--international-features.md)。

也請留意更廣泛的文章，請參閱全球[化逐步](https://msdn.microsoft.com/globalization/mt642951)章節的「[全球開發人員中心](https://msdn.microsoft.com/globalization/mt613165)」。 當您開發國際軟體時，您會想要查閱可在該處找到的其他總覽和詳細文章。

## <a name="learning-paths"></a>學習路徑

您接下來在學習中建立國際軟體時所遵循的路徑，取決於您所面對的案例。 下列案例是根據主要區段主題（國際化）在[Windows 應用程式](international-support.md)中所引進。

-   **建立可部署至多個語言之多個區域的應用程式。**

    挑戰在於開發不需要針對每種語言或文化特性重寫的應用程式。

    -   請參閱[瞭解多語系消費者介面 (MUI) ](./about-multilingual-user-interface.md)的文章。
    -   探索[多語系消費者介面](multilingual-user-interface.md)的檔。
    -   開始使用 [HELLO MUI](#the-hello-mui-application) 應用程式。

-   **支援不同語言、字元集和字型的輸入和顯示。**

    您的應用程式可能需要支援多個字元集、支援複雜的腳本 (例如，用來代表希伯來文、阿拉伯文、泰文和印度文的語言) 、允許使用者從國際字型中選取，或允許使用者使用標準鍵盤來輸入字元和符號，例如日文漢字。

    -   閱讀下列文章：

        -   [Windows 中的腳本與字型支援](https://msdn.microsoft.com/globalization/mt791278)
        -   [輸入語言：鍵盤和 Ime](https://msdn.microsoft.com/globalization/mt662332)

    -   探索以下檔：

        -   [Unicode 和字元集](unicode-and-character-sets.md)
        -   [國際字型和文字顯示](international-fonts-and-text-display.md)
        -   [輸入方法管理員](input-method-manager.md)

-   **以適當的格式顯示文化特性相依物件。**

    國際應用程式應該使用地區設定來正確地排序字串，以及顯示區分文化特性的資訊，例如時間、日期和貨幣。

    -   探索「 [國家語言支援知識中心](./national-language-support-reference.md)」。
    -   查看 [ (NLS) 的國家語言支援 ](national-language-support.md)檔。

-   **探索使用者使用的語言或腳本，並將其套用至應用程式的其他服務。**

    如果您的應用程式可以決定撰寫文字和使用者輸入的語言，它可以在可理解的語言中顯示提示或協助等內容。

    -   閱讀[Windows： Windows 的擴充語言服務中撰寫可供世界各地的應用程式](./using-extended-linguistic-services.md)文章。
    -   探索 [ (ELS) 擴充語言服務 ](extended-linguistic-services.md)的檔。

## <a name="internationalization-technologies-in-the-sdk"></a>SDK 中的國際化技術

SDK 的國際開發支援區段提供可讓應用程式列舉語言、地區設定和地區設定特定格式的技術。 您可以在使用 C 或 c + + 撰寫的 Microsoft Win32 應用程式中使用它們。

[擴充的語言服務](extended-linguistic-services.md)會提供 Microsoft 專利技術，以文字識別語言和腳本。 您的應用程式可以根據類別以及輸入和輸出語言、腳本和內容類型，判斷可用的服務。

[國際字型和文字顯示](international-fonts-and-text-display.md)提供有關國際字型、複雜字集和圖像的資訊，以及在 Windows 平臺上進行印刷印刷的詳細資訊。

[輸入方法管理員 (的輸出) ](input-method-manager.md) 是一種技術，可協助應用程式從輸入法編輯器中接收輸入 (輸入法) 軟體，進而允許使用標準鍵盤來輸入字元和符號，例如日文漢字的字元和符號。

## <a name="the-hello-mui-application"></a>Hello MUI 應用程式

國際開發中的一項常見工作，是從單一語言應用程式開始，您必須將該應用程式做好準備。 您需要新增其他語言的支援，但不需要為每個新的語言或文化特性重寫程式碼。

這項工作可讓您有機會提供教學課程，讓您逐步建立 Hello MUI 應用程式，並使用[多語系消費者介面 (的 mui) ](multilingual-user-interface.md)資源模型以及 Windows 中提供的相關支援。

本教學課程採用熟悉的 Hello World 應用程式的概念，示範如何使用 MUI 來建立基本的多語系應用程式。

您可以在[將多語系消費者介面支援新增至應用程式](creating-a-multilingual-user-interface-application.md)時，開始 Hello MUI 教學課程。

 

 
