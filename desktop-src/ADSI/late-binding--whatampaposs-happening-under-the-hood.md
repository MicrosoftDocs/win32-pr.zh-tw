---
title: 在幕後進行的晚期繫結
description: 本主題說明在 ADSI 中晚期繫結的運作方式。
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- 延伸模組 ADSI、晚期繫結、幕後的進展
- binding AD，晚期繫結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c479472a2974f31e8ecdd4308b01cf7c7251eada3f907d5d90ecf152028399b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637888"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>晚期繫結：幕後有什麼進展？

下列清單概述執行晚期繫結的一般程式：

-   某些系結至 ADSI 目錄物件。 例如，"LDAP：//CN = Jeffsmith，OU = Sales，DC = Fabrikam，DC = COM" 使用 COM 晚期繫結來系結。 這會導致 ADSI 在 **IDispatch** 介面上呼叫 [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch)方法。
-   ADSI 會在使用者類別中尋找物件，並建立支援適當介面的物件，例如 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)。
-   ADSI 會在登錄中執行查閱，並尋找使用者的延伸 Clsid。 請注意，ADSI 會快取此資料。
-   它會呼叫 **MyNewMethod** 方法。 ADSI 會查閱其分派識別碼和其他 ADSI 擴充功能的分派識別碼。 ADSI 接著會尋找提供此呼叫的延伸模組，並呼叫該擴充功能的 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) 介面。
-   擴充功能會執行函式。
-   現在，用戶端寫入器會使用目前延伸模組的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面叫用 **YourNewMethod** 方法。 延伸模組的 **idispatch** 執行會委派回 **idispatch** for ADSI。
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)會再次搜尋適當的副檔名或本身，然後使用該延伸模組的 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)介面呼叫適當的延伸模組。

 

 