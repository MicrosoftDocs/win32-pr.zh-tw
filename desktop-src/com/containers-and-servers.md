---
title: 容器和伺服器
description: 容器和伺服器
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840788"
---
# <a name="containers-and-servers"></a>容器和伺服器

複合檔案應用程式有兩種基本類型：容器應用程式和伺服器應用程式。 OLE 容器應用程式可讓使用者建立、編輯、儲存和取出複合檔案。 OLE 伺服器應用程式會提供使用者方法來建立檔和其他資料表示，以連結或內嵌的形式包含在容器應用程式中。 OLE 應用程式可以是容器應用程式、伺服器應用程式或兩者。

OLE server 應用程式的執行方式也不同，因為它們是實作為同 *進程伺服器* 或 *本機伺服器*。 同進程伺服器是在容器應用程式的進程空間中執行 (DLL) 的動態連結程式庫。 您只能從容器應用程式內執行同進程伺服器。

> [!Note]  
> 未來的 OLE 版本會啟用跨電腦界限的連結和內嵌，讓一部電腦上的容器應用程式能夠使用由另一部電腦上執行的 *遠端伺服器* 所提供的複合檔案物件。 從容器應用程式的觀點來看，在它自己的進程空間中執行的任何 OLE 伺服器應用程式（不論是在同一部電腦或遠端電腦上）都是 *processÂ伺服器*。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複合檔案](compound-documents.md)
</dt> <dt>

[同進程伺服器](in-process-servers.md)
</dt> </dl>

 

 




