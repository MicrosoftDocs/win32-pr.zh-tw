---
description: 本節說明 Windows 中的技術，可讓您在 C 或 c + + 型 Microsoft Win32 應用程式中支援國際市場的許多文化特性和書寫語言。
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Windows 應用程式的國際化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f6e4952c94af3b14dc0e8f4f135c1cc0cebafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690844"
---
# <a name="internationalization-for-windows-applications"></a>Windows 應用程式的國際化

之前稱為「國際支援」 () 

本節說明 Windows 中的技術，可讓您在 C 或 c + + 型 Microsoft Win32 應用程式中支援國際市場的許多文化特性和書寫語言。

Windows 已成為全球客戶的基本平臺。 國際使用者期待的解決方案是針對其在世界各地的語言和區域進行調整。 在本節中，您將找到開發多語系、多重文化和多網站解決方案所需的資訊。 Windows 內建的國際支援可讓您以比以往更少的工程額外負荷來實行許多案例。

開發全球化應用程式需要使用許多服務和工具。 Windows 包含的功能可讓您開發下列解決方案：

- 支援世界各地使用者的不同語言特定和地區設定特有的需求 (包括特製化文字支援、排序行為、日期和時間格式，以及鍵盤配置) 。  (需詳細資訊，請參閱 [國家語言支援知識中心](./national-language-support-reference.md)。 ) 
- 全球化 (可從單一二進位影像部署) ，而且可以當地語系化 (可以針對特定的當地市場) 進行調整。  (需詳細資訊，請參閱 [多語系消費者介面](./multilingual-user-interface.md)。 ) 
- 顯示國際字型和文字，並允許使用者指定所需的字型。  (需詳細資訊，請參閱 [Windows 中的腳本與字型支援](/globalization/input/font-support)) 。
- 允許使用者使用標準鍵盤輸入複雜的字元和符號。
- 透過 Unicode 和傳統字元集，提供許多不同書寫語言的支援。
- 探索使用者的語言輸入，並量身打造您的應用程式所提供的使用者體驗。  (需詳細資訊，請參閱 [在 windows 中撰寫可供世界用的應用程式： windows 中的擴充語言服務](./using-extended-linguistic-services.md)。 ) 

## <a name="in-this-section"></a>本章節內容

本章節記載了下列國際支援技術。 這些應用程式可使用這些主要案例來列出它們。

- [使用國際 Windows 開發開始使用](getting-started-with-international-development.md)

    說明如何開始建立可供使用的全球應用程式，並提供教學課程來說明撰寫全域軟體的一般工作。

    常見案例：

    - 判斷要採取的途徑，以瞭解如何開發國際軟體。
    - 探索 Microsoft Windows 軟體開發套件 (SDK) 提供的國際化技術。
    - 遵循採用現有單一語言應用程式的教學課程，並新增其他語言的支援。

- [全球化服務](globalization-services.md)

    描述 [ (ELS) 的擴充語言服務 ](extended-linguistic-services.md)，這可讓您探索撰寫文字和使用者輸入的語言，以及 [ (NLS) 的國家語言支援 ](national-language-support.md)，這可讓應用程式使用地區設定資訊來顯示區分文化特性的資訊 (例如時間、日期和貨幣) ，以及正確地排序字串。

    常見案例：

    - 探索使用者輸入的語言，以便能以可理解的語言來顯示說明內容。
    - 探索要顯示之文字中所使用的腳本。 如果是簡體或繁體中文，請提供使用者將文字從一個文字轉譯成另一個的選項。
    - 允許使用者選取地區設定 () 的語言相關使用者喜好設定資訊的集合。
    - 以適當的語言和格式顯示時間、日期、行事曆資訊、貨幣和其他許多文化特性相依物件。
    - 依給定地區設定的使用者所預期的順序來排序字串。

- [輸入方法管理員](input-method-manager.md)

    描述應用程式用來與輸入方法編輯器通訊的技術 (IME) 。 IME 可讓電腦使用者使用標準鍵盤來輸入複雜的字元和符號。

    常見案例：

    - 允許使用者使用標準鍵盤來輸入日文中文字元。

- [國際字型和文字顯示](international-fonts-and-text-display.md)

    描述 Windows 平臺針對國際字型提供的支援、國際文字，以及精細的印刷樣式。

    常見案例：

    - 允許使用者根據字元集選取國際字型。
    - 顯示國際文字。
    - 處理複雜的腳本，包括雙向轉譯、內容成形，以及連 (Uniscribe) 的連字。
    - 針對精細的印刷樣式， (Uniscribe) 提供高度的控制。

- [多語系使用者介面](multilingual-user-interface.md)

    描述應用程式如何將語言相依的資源與語言中立的程式碼分開，以提供支援的使用者介面語言。

    常見案例：

    - 建立應用程式的區域或全球單一部署映射。
    - 藉由更新應用程式資源來當地語系化方案，而不需要變更應用程式原始程式碼。
    - 允許使用者在執行時間從某個 UI 語言切換至另一種語言。

- [Unicode 和字元集](unicode-and-character-sets.md)

    描述應用程式如何利用 Unicode，也就是使用16位程式碼值的全球字元編碼標準，來代表新式運算中使用的所有字元，包括用於發佈的技術符號和特殊字元。

    常見案例：

    - 透過 Unicode 支援國際 marketplace 的許多不同語言。
    - 必要時，將 Unicode 字元轉換成其他字元集或從中轉換。

- [安全性考慮：國際功能](security-considerations--international-features.md)

    提供與國際開發支援功能相關之安全性考慮的資訊。

    安全性資訊適用于所有案例。

## <a name="related-international-technologies"></a>相關的國際技術

國際開發支援也適用于以 managed 程式碼撰寫的應用程式。 如果您正在針對 .NET Framework 進行開發，您將需要下列部分或全部：

- 「 [全球化」命名空間](/dotnet/api/system.globalization) 包含類別，這些類別會定義與文化特性相關的資訊，並提供先進的全球化函數。
- System.string [命名空間](/dotnet/api/system.text) 包含代表字元編碼、轉換字元區塊，以及操作和格式化字串物件的類別。
