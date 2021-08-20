---
description: 具有系統管理許可權的使用者和應用程式可以使用 Windows Installer 函式來清查系統上所安裝的 Windows Installer 應用程式、功能、元件和修補程式。從 Windows Installer&\# 160; 3.0 開始，具有系統管理員許可權的使用者和應用程式可以列舉所有使用者在系統上安裝的 Windows Installer 應用程式、功能、元件和修補程式。 系統管理員和應用程式可以針對特定使用者或系統中的所有使用者，取得產品或修補程式的相關資訊。 應用程式可以取得特定使用者的功能狀態或元件狀態。從 Windows Installer 開始可用的清查功能&\# 160; 3.0 可以限制安裝內容和使用者內容所能找到的專案範圍。 有三種可能的安裝內容：每位使用者、每部電腦，以及每位使用者管理。 使用者內容可以是系統中的特定使用者或所有使用者。 早于 Windows Installer&160 的 Windows Installer 清查函式版本，只能 \# 列舉電腦內容中的系統上所安裝的專案，或目前使用者的每個使用者內容中所安裝的專案。 這項限制可防止目前使用者以外的使用者在系統中安裝的所有 Windows Installer 產品和修補程式的完整清查。列舉 ProductsEnumerating PatchesObtaining 產品 InformationObtaining 修補程式 InformationObtaining 元件狀態 InformationObtaining 功能狀態資訊
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: 使用 Windows Installer 清查產品和修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9406d0984e58efdb8344fbf8974234690e3a6aaeb1cc697b5a76e6af940554e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013226"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>使用 Windows Installer 清查產品和修補程式

具有系統管理許可權的使用者和應用程式可以使用 Windows Installer 函式來清查系統上所安裝的 Windows Installer 應用程式、功能、元件和修補程式。

從 Windows Installer 3.0 開始，具有系統管理員許可權的使用者和應用程式可以列舉所有使用者在系統上安裝的 Windows Installer 應用程式、功能、元件和修補程式。 系統管理員和應用程式可以針對特定使用者或系統中的所有使用者，取得產品或修補程式的相關資訊。 應用程式可以取得特定使用者的功能狀態或元件狀態。

從 Windows Installer 3.0 開始可用的清查函式，可以限制安裝內容和使用者內容所能找到的專案範圍。 有三種可能的安裝內容：每位使用者、每部電腦，以及每位使用者管理。 使用者內容可以是系統中的特定使用者或所有使用者。

早于 Windows Installer 3.0 的 Windows Installer 清查函式版本，只能列舉電腦內容或目前使用者的每個使用者內容中所安裝的專案。 這項限制可防止目前使用者以外的使用者在系統中安裝的所有 Windows Installer 產品和修補程式的完整清查。

-   [列舉產品](#enumerating-products)
-   [列舉修補程式](#enumerating-patches)
-   [取得產品資訊](#obtaining-product-information)
-   [取得修補程式資訊](#obtaining-patch-information)
-   [取得元件狀態資訊](#obtaining-component-state-information)
-   [取得功能狀態資訊](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>列舉產品

使用 [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)函式來列舉系統中安裝的 Windows Installer 應用程式。 此函式可尋找應用程式的所有個別電腦安裝和個別使用者安裝 (受控和非受控) ，以供目前使用者和系統中的其他使用者使用。 使用 *dwCoNtext* 參數來指定要尋找的安裝內容。 您可以指定任何一個或任何可能的安裝內容組合。 使用 *szUserSid* 參數來指定要尋找之應用程式的使用者內容。

## <a name="enumerating-patches"></a>列舉修補程式

使用 [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) 函式來尋找應用程式所套用的修補程式。 此函式可以尋找針對特定應用程式或系統中的所有應用程式所套用的修補程式。 此函式可尋找套用至所有每部電腦安裝的修補程式，以及應用程式的每個使用者安裝 (受控和非受控) 給系統中的目前使用者和其他使用者。

您可以使用安裝內容和使用者內容，將修補程式列舉限制為特定內容或跨所有內容。 使用 *dwCoNtext* 參數來指定要尋找的安裝內容。 您可以指定任何一個或任何可能的安裝內容組合。 使用 *szUserSid* 參數來指定要尋找之應用程式的使用者內容。

**列舉適用于系統中所有使用者所公告或安裝之所有產品的修補程式**

-   呼叫 [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) 函數。
    -   使用 **Null** 作為 *szProductCode* 參數的值。
    -   使用 "s-1-1-0" 作為 *szUserSid* 參數的值。
    -   使用 "MSIINSTALLCONTEXT \_ ALL" 作為 *dwCoNtext* 參數的值。

**列舉適用于系統中所有使用者所公告或安裝之所有產品的修補程式**

1.  呼叫 [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) 函數。

    -   使用 **Null** 作為 *szProductCode* 參數的值。
    -   使用 "s-1-1-0" 作為 *szUserSid* 參數的值。
    -   使用 "MSIINSTALLCONTEXT \_ ALL" 作為 *dwCoNtext* 參數的值。

    此函式會針對找到的每個應用程式，提供產品代碼、使用者內容和安裝內容。

2.  針對步驟1中列舉的每個應用程式，呼叫 [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) 來列舉修補程式。

    使用從 [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) 取得的產品代碼、使用者內容和安裝內容，以取得 *szProductCode*、 *szUserSid* 和 *DwCoNtext* 的值，以及每個 **MsiEnumProductsEx** 函式呼叫。

## <a name="obtaining-product-information"></a>取得產品資訊

您可以使用 [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) 函式來取得系統上已公告或已安裝之應用程式的相關資訊，以及可抓取的屬性。 這個函式可以取得除了目前使用者以外的使用者帳戶下所安裝之應用程式實例的資訊，但無法查詢目前使用者以外的使用者帳戶，在個別使用者非受控內容下公告的產品實例。

您可以指定安裝內容和使用者內容，以限制特定內容中所安裝之應用程式的資訊。 使用 *dwCoNtext* 參數來指定要尋找的安裝內容。 您只能指定其中一個可能的安裝內容。 使用 *szUserSid* 參數來指定要尋找之應用程式的使用者內容。

## <a name="obtaining-patch-information"></a>取得修補程式資訊

應用程式可以呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) 函式，以查詢所指定產品實例的修補程式的相關資訊。 您可以使用此函數來抓取 **LocalPackage**、 [**轉換**](transforms.md)和 **狀態** 等屬性。 如果使用者目前未登入電腦，則並非所有的屬性值都能提供給每位使用者的非受控應用程式使用。 您只能指定其中一個可能的安裝內容。

您可以指定安裝內容和使用者內容，將修補程式的資訊限制為套用至安裝在特定內容中的應用程式。 使用 *dwCoNtext* 參數來指定要尋找的安裝內容。 您只能指定其中一個可能的安裝內容。 使用 *szUserSid* 參數來指定要尋找之應用程式的使用者內容。

## <a name="obtaining-component-state-information"></a>取得元件狀態資訊

應用程式可以呼叫 [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) 函數來取得元件的已安裝狀態。 此函式會判斷元件是否安裝在本機或安裝以從來源執行。 此函數可以查詢目前使用者以外的使用者帳戶所安裝之應用程式實例的元件，但前提是該產品不是在目前使用者以外的使用者帳戶的每個使用者非受控內容下進行公告。

您可以指定安裝內容和使用者內容，以取得特定內容中所安裝之應用程式的元件狀態。 使用 *dwCoNtext* 參數來指定要尋找的安裝內容。 您只能指定其中一個可能的安裝內容。 使用 *szUserSid* 參數來指定要尋找之應用程式的使用者內容。

## <a name="obtaining-feature-state-information"></a>取得功能狀態資訊

應用程式可以呼叫 [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) 函數來取得產品功能的已安裝狀態。 此函式會判斷功能是通告、安裝在本機，還是安裝來從來源執行。 函數可用來查詢電腦帳戶下所安裝之應用程式實例的任何功能，或是目前使用者帳戶下的任何內容，或是目前使用者以外的任何使用者帳戶下的每個使用者管理內容的任何內容。 如果使用者帳戶不是目前使用者，則此函式無法查詢針對個別使用者非受控內容所安裝的應用程式。 您只能指定其中一個可能的安裝內容。

您可以指定安裝內容和使用者內容，以取得特定內容中所安裝之應用程式的功能狀態。 使用 *dwCoNtext* 參數來指定要尋找的安裝內容。 您只能指定其中一個可能的安裝內容。 使用 *szUserSid* 參數來指定要尋找之應用程式的使用者內容。

 

 



