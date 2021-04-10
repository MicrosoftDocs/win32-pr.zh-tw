---
title: 重新命名已編譯的資源檔
description: 根據預設，在編譯資源時，RC 會將編譯過的資源命名 ( .res) 檔案中，並以 .rc 檔的基底名稱取代，並將它放在與 .rc 檔案相同的目錄中。
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183060"
---
# <a name="renaming-the-compiled-resource-file"></a>重新命名已編譯的資源檔

根據預設，在編譯資源時，RC 會將編譯過的資源命名 ( .res) 檔案中，並以 .rc 檔的基底名稱取代，並將它放在與 .rc 檔案相同的目錄中。 接著，必須叫用 CVTRES，將 .res 檔轉換成二進位資源 (. rbj) 格式，可供連結器理解。 下列範例會編譯 MyApp，並在 MyApp. rc 的相同目錄中建立名為 MyApp 的已編譯資源檔：

**rc myapp .rc**

**/Fo** 選項提供產生的 .res 檔名稱，與對應 .rc 檔的名稱不同。 例如，若要將產生的 .res 檔 NewFile 命名為 .res，請使用下列命令：

**rc-fo 的 newfile myapp .rc**

**/Fo** 選項也可以將 .res 檔案放在不同的目錄中。 例如，下列命令會將已編譯的資源檔 MyApp. .res 放置於目錄 C： \\ Source \\ 資源：

**rc-fo c： \\ 來源 \\ 資源 \\ myapp. .res myapp**

 

 




