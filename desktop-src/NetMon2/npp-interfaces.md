---
description: 網路封包提供者 (NPPs) 提供 NPP 應用程式所呼叫的 COM 介面，以及網路監視器。
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: NPP 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986383"
---
# <a name="npp-interfaces"></a>NPP 介面

網路封包提供者 (NPPs) 提供 NPP 應用程式所呼叫的 COM 介面，以及網路監視器。 當您呼叫 [CreateNPPInterface](createnppinterface.md)時，請記住，每個 NPP 都會表示為單一同進程 COM 物件。 應用程式可以將任意數目的 NPP 物件具現化。 不過，每個具現化的物件都只能使用五個 NPP 介面的一個（且只有一個）。

另外也請注意，不同的 NPP 介面會以各種形式提供網路資料。 例如，網路監視器會使用 **IDelaydC** 介面來捕捉網路流量，並將其儲存至 capture 檔案;監視器會使用 **IRTC** 介面來捕捉即時網路流量。 下表描述網路監視器的 NPP 介面。



| 介面                | 描述                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | 捕捉儲存在捕獲檔案中的網路流量。 網路監視器和 NPP 應用程式會使用此介面。                                          |
| [IESP](iesp.md)         | 會捕捉儲存在 capture 檔案中的網路流量，並以特殊的 ESP 檔案格式提供增強的統計資料。 NPP 應用程式會使用此介面 |
| [IRTC](irtc.md)         | 會在事件發生時，捕獲即時網路流量並觸發事件。 [*監視器*](m.md)和 NPP 應用程式會使用此介面。     |
| [IStats](istats.md)     | 以原始資料（而不是框架）形式抓取統計資料。 此介面是由 NPP 應用程式（例如 [*Perfmon*](p.md)）所使用。                     |



 

 

 



