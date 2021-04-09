---
title: 控制點 API 的基本動作是什麼
description: 所有控制點都會執行下列工作。
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252e2db09aa8283034da20dc1bd2dc877bf0e5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675219"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>控制點 API 的基本動作為何？

所有控制點都會執行下列工作：

-   尋找網路上可用的 UPnP 型裝置。
-   判斷哪些裝置有興趣。
-   對感興趣的裝置發出控制權要求，並接收裝置所產生的事件。

應用程式必須先執行搜尋，以在網路上尋找可用的 UPnP 型裝置。 由於 UPnP 架構所定義的搜尋準則相當廣泛，因此應用程式可能會發現比所需更多的裝置。 因此，應用程式必須檢查找到的裝置特性，以判斷哪一種裝置最符合搜尋準則。 然後，應用程式就可以對這些裝置發出控制權要求。

下列各節說明如何使用具有 UPnP 技術的控制點 API 來執行這些作業：

-   [尋找裝置](finding-devices.md)
-   [描述裝置](describing-devices.md)
-   [控制裝置](controlling-devices.md)

如需控制點 API 中每個介面的詳細檔，請參閱 [控制點 Api 參考](control-point-api-with-upnp-technology-reference.md)。

 

 




