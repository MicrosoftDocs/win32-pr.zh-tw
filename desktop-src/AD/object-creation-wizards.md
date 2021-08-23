---
title: 物件建立的嚮導
description: 在 Active Directory Domain Services 的管理 MMC 嵌入式管理單元中，使用者可以開啟建立新物件之容器的內容功能表，選擇 [新增]，然後選擇要建立之物件的類別，藉以在目錄中建立新的物件。 建立物件的新實例時，會啟始物件建立 wizard。 每個物件類別都可以指定使用特定的建立嚮導，也可以使用一般建立 wizard。 針對一般類別（例如 user 和 organizationalUnit），Active Directory 消費者和電腦嵌入式管理單元提供一組標準的建立嚮導。有兩種方式可以擴充建立嚮導取代現有的 wizard，或是如果類別不存在，則會藉由建立主要物件建立延伸模組來取代現有的 wizard。 主要建立延伸模組會提供第一組頁面，並以與原生頁面相同的方式來主控。 主要建立延伸模組也支援擴充性機制，因此可以叫用其他建立嚮導擴充功能。 如需主要延伸模組的範例，請參閱平臺軟體發展工具組中的 scpwizard 範例 (SDK) 。擴充現有的 wizard：您可以使用次要物件建立延伸模組來擴充現有的 wizard。 次要建立延伸模組會將 wizard 頁面新增至原生頁面或主要延伸模組。 如需次要建立延伸模組的詳細資訊和範例，請參閱 Platform SDK 中的 userwizard 範例。
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- 物件廣告，建立嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97c5c8f1b521d28c926d53830135dbb1b1fc907758e7047bc91c68856eedc70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025583"
---
# <a name="object-creation-wizards"></a>物件建立的嚮導

在 Active Directory Domain Services 的管理 MMC 嵌入式管理單元中，使用者可以開啟建立新物件之容器的內容功能表，選擇 [ **新增**]，然後選擇要建立之物件的類別，藉以在目錄中建立新的物件。 建立物件的新實例時，會啟始物件建立 wizard。 每個物件類別都可以指定使用特定的建立嚮導，也可以使用一般建立 wizard。 針對一般類別（例如 [**user**](/windows/desktop/ADSchema/c-user) 和 [**organizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit)），Active Directory 消費者和電腦嵌入式管理單元提供一組標準的建立嚮導。

有兩種方式可以擴充建立嚮導：

-   取代現有的 wizard，或如果類別不存在，請提供一個：現有的 wizard 會藉由建立 *主要物件建立延伸* 模組來取代。 主要建立延伸模組會提供第一組頁面，並以與原生頁面相同的方式來主控。 主要建立延伸模組也支援擴充性機制，因此可以叫用其他建立嚮導擴充功能。 如需主要延伸模組的範例，請參閱平臺軟體發展工具組中的 scpwizard 範例 (SDK) 。
-   擴充現有的 wizard：您可以使用 *次要物件建立延伸* 模組來擴充現有的 wizard。 次要建立延伸模組會將 wizard 頁面新增至原生頁面或主要延伸模組。 如需次要建立延伸模組的詳細資訊和範例，請參閱 Platform SDK 中的 userwizard 範例。

## <a name="developer-audience"></a>開發人員讀者

本檔假設讀者已熟悉使用 c + + 的 COM 作業和元件開發。 目前無法使用 Visual Basic 建立 Active Directory 物件建立嚮導的擴充功能。

## <a name="creating-an-active-directory-object-creation-extension"></a>建立 Active Directory 物件建立延伸模組

主要和次要物件建立延伸模組都是 COM 的內部進程伺服器，這些伺服器會執行特定介面並向 Active Directory Domain Services 註冊。

**建立和安裝物件建立延伸模組**

1.  建立物件建立延伸模組 DLL。 物件建立延伸模組是 COM 的內部伺服器伺服器，至少會執行 [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) 介面。 如需詳細資訊，請參閱 [執行物件建立延伸模組 COM 物件](implementing-the-object-creation-extension-com-object.md)。
2.  在要使用建立延伸模組的電腦上安裝建立延伸模組。 若要這樣做，請建立建立延伸模組 DLL 的 Microsoft Windows Installer 套件，並使用群組原則適當地部署套件。 如需詳細資訊，請參閱散發 [消費者介面元件](distributing-user-interface-components.md)。
3.  在 Windows 登錄和 Active Directory Domain Services 中註冊建立延伸模組。 如需詳細資訊，請參閱 [註冊物件建立延伸](registering-the-object-creation-extension.md)模組。

## <a name="using-an-object-creation-wizard"></a>使用物件建立嚮導

物件建立 wizard 也可以從 Active Directory Domain Services 的管理 MMC 嵌入式管理單元以外的應用程式叫用。 如需詳細資訊，請參閱 [從您的應用程式叫用建立嚮導](invoking-creation-wizards-from-your-application.md)。

如果未針對物件類別註冊建立嚮導，則系統管理嵌入式管理單元會提供一般建立嚮導。 一般建立嚮導是在執行時間根據所建立物件之類別的強制屬性清單所建立。 針對每個必要的屬性，會將頁面加入至 UI。 一般建立嚮導是不可延伸的。 如果需要擴充性，必須將它取代為主要物件建立延伸模組。

 

 