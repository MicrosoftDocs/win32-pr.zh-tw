---
description: MUI 應用程式的資源準備支援 Win32 PE 和非 Win32 PE 模型。
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: 準備資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef40453ca6db40bed1c07bad80f7e21cb7adaa7ea48ae8ee5ce2a2a5c657ba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040668"
---
# <a name="preparing-resources"></a>準備資源

MUI 應用程式的資源準備支援 Win32 PE 和非 Win32 PE 模型。 Win32 PE 資源是在以 PE 為基礎的檔案中提供，例如 .dll、.exe 或 .sys 檔。 非 Win32 PE 資源是由您選擇的自訂模組所提供。

> [!Note]  
> 強烈建議您對 Win32 MUI 應用程式使用 Win32 PE 資源，因為這些資源完全受到 MUI 資源技術的支援。 您可以藉由呼叫 [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) 函式（如 [尋找非 win32 pe 資源](locating-non-win32-pe-resources.md)中所述）來找出非 win32 pe 資源檔，但應用程式必須提供自己的功能來尋找和載入所需的資源。

 

本節包含下列主題：

-   [建立基礎語言資源檔](creating-the-base-language-resource-file.md)
-   [使用登錄字串重新導向](using-registry-string-redirection.md)
-   [準備資源設定檔](preparing-a-resource-configuration-file.md)

 

 



