---
description: 啟用內容是記憶體中的資料結構，其中包含系統可用來將應用程式重新導向以載入特定 DLL 版本、COM 物件實例或自訂視窗版本的資訊。
ms.assetid: 5416f8c0-d99b-4a5d-a689-a47bd0cf1a88
title: 啟用內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21aaf2c4d2e4fc0f3ef691406e663dc5efac44a9d0b34880596d21cac8a5f621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142541"
---
# <a name="activation-contexts"></a>啟用內容

[*啟用*](a-sbscs-gly.md) 內容是記憶體中的資料結構，其中包含系統可用來將應用程式重新導向以載入特定 DLL 版本、COM 物件實例或自訂視窗版本的資訊。 啟用內容的其中一個區段可能包含 dll 載入器所使用的 DLL 重新導向資訊;另一個區段可能包含 COM 伺服器資訊。 啟用內容函式會使用、建立、啟動和停用啟用內容。 啟用函式可以將應用程式的系結重新導向至指定特定 DLL 版本、視窗類別、COM 伺服器、類型程式庫和介面的版本命名物件。 如需啟用內容函式和結構的詳細資訊，請參閱 [啟用內容參考](activation-context-reference.md)。

從 Windows XP 開始，啟用內容函數可讓 Windows 使用[資訊清單](manifests.md)中的資訊來建立版本命名的物件。 如果應用程式藉由呼叫 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)來建立進程，Windows 會檢查 [應用程式資訊清單](application-manifests.md)是否存在。 如果資訊清單存在，Windows 會使用資訊清單中的資訊來填入啟用內容。 因為資訊清單會描述應用程式對 [並存元件](about-side-by-side-assemblies-.md) 版本的相依性，所以在資訊清單中指定沒有版本的物件會對應至版本命名的物件。 例如，資訊清單可能會描述 Dll、檔案、視窗類別、COM 伺服器、類型程式庫和介面。

當全域物件是在啟用內容中建立時，系統會透過查閱資訊清單，自動為物件提供特定版本的名稱。 當應用程式執行並要求命名物件時，它會取得版本命名的物件。 這可讓程式碼模組的多個版本在系統上同時執行，而不會干擾彼此。 例如， [Windows Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85))會使用資訊清單來描述6.0 版 comctl32.dll 的相依性，以及建立視窗類別的版本。

如果應用程式藉由呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)來建立資源，進程會指定該函式的類別名稱。 對 [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx) 的呼叫會取得目前的啟用內容，並檢查指定類別名稱是否存在對應。 如果有對應存在，則會使用該版本的呼叫進程來解析對應，並提供版本特定的類別名稱。 Windows 使用視窗程式、樣式和其他與該類別名稱和版本相關聯的屬性來建立視窗。

在大部分情況下，啟用內容是由系統所管理。 應用程式開發人員和元件提供者通常不需要對堆疊進行呼叫。 應用程式可以直接呼叫啟用內容來管理啟用內容。 如需詳細資訊，請參閱 [使用啟用內容 API](using-the-activation-context-api.md)。

 

 
