---
description: 指定預設啟用內容
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: 指定預設啟用內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1598e0a111b358a783b940a5c036d63eef348740ff2467d3ed78720c6a5210
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977138"
---
# <a name="specifying-a-default-activation-context"></a>指定預設啟用內容

當您的應用程式或元件建立新的處理常式時，Windows 會搜尋預設的應用程式資訊清單。 請注意，在應用程式中包含為資源的資訊清單優先于外部資訊清單。 預設啟用內容是啟用任何其他啟動內容之前的第一個啟用內容。 除非您啟用其他內容，否則此啟用內容一律為使用中狀態。 如果您在 \_ \_ 編譯應用程式或元件時定義啟用隔離感知，則像是 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)、 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)和 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 的呼叫可以執行自動內容管理。

載入器可讓應用程式透過兩種方法來指定其預設啟用內容。 您可以將資訊清單檔案放入可執行檔的資源中，而載入器會找到它。 這等同于將資訊清單檔案放入可執行檔的資源資料表中。 您可以將資訊清單放在名為 *Myapp*.exe 的檔案中。資訊清單位於與 *myapp*.exe 相同的目錄中，而載入器會在尋找 *myapp*.exe 時找到該檔案。

如果您不使用上述任何一種方法，應用程式就會從系統預設啟用內容開始，其中包含最基本的元件集。

使用自動內容管理的較佳方式是編譯已定義隔離感知的應用程式 \_ \_ 。 建議的方法是在編譯器的命令列上針對正在建立的整個專案進行設定，而不是在個別原始程式檔或標頭中設定此選項。 這使得大部分的 Win32 Api 都知道啟用內容以及如何管理它們。 不需要自行進行啟用內容管理，您只需要在資源識別碼 ISOLATIONAWARE 資訊清單資源識別碼的資源識別碼 \_ 資訊清單 \_ 資源 \_ 識別碼 (數值 2) ，其類型為 RT \_ 資訊清單 (數值24。 ) 的函式（例如， [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)、 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)和 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) ）則會在進行實際呼叫之前自動啟動此內容。

請注意，如果您 \_ 已定義啟用隔離感知的編譯 \_ ，您也不能自行進行啟用內容管理。 若已 \_ 定義隔離感知 \_ ，Windows 會忽略您的應用程式可能會嘗試在 [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)和 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)呼叫之間進行的任何動態啟用內容建立。 這表示當您的應用程式使用隔離 \_ 感知功能時， \_ 您必須確定資訊清單包含元件所需之所有元件的完整清單。

 

 
