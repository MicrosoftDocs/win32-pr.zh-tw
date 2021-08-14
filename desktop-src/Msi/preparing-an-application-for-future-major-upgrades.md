---
description: 安裝套件的作者應該包含升級 .msi 檔案中的資訊，以確保其安裝套件可以利用 Microsoft Windows Installer 所提供的完整升級功能。
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: 準備應用程式以進行未來的主要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c38adc97fce578b48bc721b4265696486351097771cf936efc1e667752a7a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377349"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>準備應用程式以進行未來的主要升級

安裝套件的作者應該包含升級 .msi 檔案中的資訊，以確保其安裝套件可以利用 Microsoft Windows Installer 所提供的完整升級功能。

每個應用程式或應用程式套件都應該指派 [**UpgradeCode**](upgradecode.md) 屬性、 [**ProductVersion**](productversion.md) 屬性和 [**ProductLanguage**](productlanguage.md) 屬性。 [**UpgradeCode**](upgradecode.md)屬性指出由相同產品的不同版本和不同語言版本所組成的一系列相關應用程式。 如需使用 [**UpgradeCode**](upgradecode.md) 屬性的詳細資訊，請參閱 [使用 UpgradeCode](using-an-upgradecode.md)。

**準備應用程式以進行未來的主要升級**

1.  判斷應用程式的新套件代碼值。 如需封裝程式碼的詳細資訊，請參閱 [封裝程式碼](package-codes.md)。 在 [摘要資訊資料流程](summary-information-stream.md)的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性中，輸入新的封裝程式碼。
2.  判斷應用程式的新 [**ProductCode**](productcode.md) 屬性。 如需詳細資訊，請參閱 [變更產品代碼](changing-the-product-code.md) 。 在 [屬性資料表](property-table.md)中輸入 [**ProductCode**](productcode.md)和其值。
3.  判斷應用程式的版本與 [**ProductVersion**](productversion.md) 屬性。 [**ProductVersion**](productversion.md)應該會隨著應用程式的每個新版本而增加。 請注意，安裝程式只會使用產品版本的前三個欄位。 如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。 在屬性資料表中輸入 [**ProductVersion**](productversion.md) 和其值。
4.  判斷封裝的語言與 [**ProductLanguage**](productlanguage.md) 屬性。 這個屬性的值必須是數位語言識別項 (LANGID) 。 在 [屬性資料表](property-table.md)中輸入 [**ProductLanguage**](productlanguage.md)和其值。 請注意， [FindRelatedProducts 動作](findrelatedproducts-action.md) 會使用 [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)所傳回的語言。 若要讓 FindRelatedProducts 正常運作，封裝作者必須確定在屬性工作表中，將 [**ProductLanguage**](productlanguage.md) 屬性設定為 [ [**範本摘要**](template-summary.md) ] 屬性中也列出的語言。
5.  如果您要撰寫產品第一版的安裝套件，請使用新的 [**UpgradeCode**](upgradecode.md)。 如果您的套件適用于現有產品的較新版本，或與不同語言的現有產品版本相同，請使用現有產品的相同 [**UpgradeCode**](upgradecode.md) 。 沒有兩個具有相同 [**ProductVersion**](productversion.md) 和相同 [**ProductLanguage**](productlanguage.md) 的產品可以有相同的 [**UpgradeCode**](upgradecode.md)，除非其中一個是另一個的 [小型更新](small-updates.md) 。
6.  [**UpgradeCode**](upgradecode.md)具有 [GUID](guid.md)的格式。 在屬性資料表中輸入 [**UpgradeCode**](upgradecode.md) GUID。

如需詳細資訊，請參閱 [防止舊套件安裝在較新的版本上](preventing-an-old-package-from-installing-over-a-newer-version.md)。

 

 



