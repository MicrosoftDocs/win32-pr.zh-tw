---
title: ADSI 範例提供者元件
description: Active Directory 服務介面提供者寫入器將會發現這是特別感興趣的部分，因為它說明了 ADSI 範例提供者元件的深度。
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ff1d998a9db620c6dc6fb4402f126f556c95a45d589410800ea9c4b335a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023896"
---
# <a name="adsi-example-provider-component"></a>ADSI 範例提供者元件

Active Directory 服務介面提供者寫入器將會發現這是特別感興趣的部分，因為它說明了 ADSI 範例提供者元件的深度。 ADSI 提供者寫入器可以安裝範例提供者，並使用程式碼架構作為基礎來建立自己的實作為基礎。 我們將討論下列主題：

[安裝範例提供者元件](installing-the-example-provider-component.md) 會說明如何安裝 ADSI 範例提供者和其 mock 目錄。 本節包含登錄設定的清單。

[目錄定義](directory-definition.md) 描述範例提供者元件所定義的目錄專案。

[架構管理](schema-management.md) 描述如何以特定類型的 Active Directory 物件來表示範例提供者元件目錄服務中的每個元素。

系結[至 Active Directory 物件](binding-to-an-active-directory-object.md)會描述如何在給定 ADsPath 字串、範例提供者元件識別該專案、為其建立適當的 Active Directory 物件類型，以及在該物件上抓取要求的介面指標類型，以傳回到 ADs 用戶端軟體。

列舉值[物件](enumerator-objects.md)會列出由範例提供者元件提供的特定列舉型別，以及可以在其中找到執行程式碼的原始程式碼。

程式[代碼總覽](code-overview.md)提供範例提供者元件中每個部分的工作層級描述。

程式[代碼詳細資料](code-details.md)會列出軟體模組及其內容。

 

 




