---
description: 資訊清單會描述 Windows 並存元件。
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: 關於並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e38ee058965b45c3094888aa34351114aa93e595e4e8b893889daaa685410a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142594"
---
# <a name="about-side-by-side-assemblies"></a>關於並存元件

[資訊清單](manifests.md)會描述 Windows 並存元件。 並存元件包含一組資源（一組 dll、Windows 類別、COM 伺服器、類型程式庫或介面）的集合，這些資源一律會同時提供給應用程式。 這些會在組件資訊清單中描述。

通常，並存元件是單一 DLL。 例如，Microsoft comctl32.dll 元件是具有資訊清單的單一 DLL，而 Microsoft Visual C++ 開發系統執行時間程式庫元件包含多個檔案。 資訊清單包含描述並存元件和並存元件相依性的 [*中繼資料*](m-sbscs-gly.md) 。

作業系統會使用並存元件做為命名、系結、版本控制、部署和設定的基礎單位。 每個並存元件都有唯一的身分識別。 元件身分識別的其中一個屬性是其版本。 如需詳細資訊，請參閱 [元件版本](assembly-versions.md)。

從 Windows XP 開始，在相同時間執行的應用程式可以使用多個並存元件版本。 資訊清單和元件版本號碼會由載入器用來判斷正確的元件版本系結至應用程式。 並存元件和資訊清單可與應用程式和並存管理員一起運作，如下圖所示。

![一般並存元件的標記法](images/sxsman.png)

在上述範例中，Comctl32.DLL 6.0 版和 Comctl32.DLL 5.0 版都位於並存的組件快取中，而且可供應用程式使用。 當應用程式呼叫載入 DLL 時，並存管理員會決定應用程式是否具有資訊清單中所述的版本相依性。 如果沒有相關的資訊清單，系統會載入元件的預設版本。 針對 Windows XP，Comctl32.DLL 的5.0 版是系統預設值。 如果並存管理員找到資訊清單中所述版本6.0 的相依性，則該版本會載入以與應用程式一起執行。

Microsoft 提供數個重要的系統元件，做為並存元件。 如需詳細資訊，請參閱 [支援的 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)。 應用程式開發人員也可以建立自己的並存元件。 如需詳細資訊，請參閱 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md)。 在許多情況下，您可以將現有的應用程式更新為使用並存元件，而不需要變更應用程式程式碼。

我們鼓勵開發人員使用並存元件來建立 [隔離的應用程式](isolated-applications.md)，並將現有的應用程式更新為隔離的應用程式，原因如下：

-   並存元件可以減少 DLL 版本衝突的可能性。
-   並存元件共用可讓多個 COM 或 Windows 元件版本同時執行。
-   應用程式和系統管理員可以在部署之後，以 [全域](publisher-configuration.md) 或個別 [應用程式](per-application-configuration.md) 的設定來更新元件設定。 例如，您可以將應用程式更新為使用並存元件（包含更新），而不需要重新安裝應用程式。

 

 



