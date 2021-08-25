---
title: 尋找裝置
description: UPnP 架構是一種動態網路架構，可讓裝置隨時加入並離開網路。
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5626f7d941d9e3fa73b6d3d46ef9f51ef256ee8371e7594c312d225bba865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867588"
---
# <a name="finding-devices"></a>尋找裝置

UPnP 架構是一種動態網路架構，可讓裝置隨時加入並離開網路。 由於這個動態架構，應用程式無法依賴特定的 UPnP 型裝置在任何指定時間都可供使用。 基於這個理由，應用程式 (或控制點) 搜尋網路，找出最符合指定準則的裝置。 應用程式也會等待裝置通告訊息，指出已將新的裝置新增至網路。

以下是以 UPnP 為基礎之裝置的有效搜尋準則：

-   裝置類型
-   服務類型
-   唯一的裝置名稱 (UDN) 
-   所有根裝置

裝置類型和服務類型搜尋通常用來尋找具有一般特性的裝置類別。 UDN 搜尋可用來尋找特定裝置。

若要搜尋裝置，應用程式必須先具現化裝置搜尋工具物件。 此物件會公開 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) 介面;其方法會執行先前所述的搜尋。

下列各節說明尋找裝置的程式：

-   [建立裝置搜尋工具](creating-the-device-finder.md)
-   [非同步搜尋](asynchronous-searching.md)
-   [同步搜尋](synchronous-searching.md)
-   [同步搜尋所傳回的裝置集合](device-collections-returned-by-synchronous-searches.md)

 

 




