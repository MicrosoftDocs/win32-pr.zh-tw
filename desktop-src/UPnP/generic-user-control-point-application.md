---
title: 一般使用者控制點應用程式
description: 一般使用者控制點 (UCP) 應用程式可讓您探索裝置、控制這些探索到的裝置，以及查看相關的事件資訊，全都使用圖形化介面。
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0bbf454da2bf36becb3c8b0aff2babc87925df7ac658fc9dc7963ba9182fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655730"
---
# <a name="generic-user-control-point-application"></a>一般使用者控制點應用程式

一般使用者控制點 (UCP) 應用程式可讓您探索裝置、控制這些探索到的裝置，以及查看相關的事件資訊，全都使用圖形化介面。

**若要啟動泛型 UCP 應用程式**

1.  建立並設定範例 \\ netds \\ upnp \\ GenericUCP \\ CPPdevtype.txt 檔 \\ (或 \\ \\ 使用裝置資訊) 的devtype.txt 檔。 此檔案可讓您針對「依類型尋找」和「非同步尋找」搜尋設定泛型 UCP。 檔案的每一行都必須包含裝置類型和相關的描述。 例如：

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    此範例適用于虛構的 media player 裝置。 第二行結尾的「媒體播放機」不是裝置類型的一部分，而是用於一般 UCP 應用程式中的資訊用途。 這同樣適用于第一行中的「所有根裝置」。

    加入一行，其中包含您的特定裝置類型和每個裝置的描述。

2.  建立並設定範例 \\ netds \\ upnp \\ GenericUCP \\ CPPudn.txt 檔 \\ (或 \\ \\ 使用您裝置的 UDN 資訊) 的udn.txt 檔。 此檔案可讓您設定 "find by UDN" 搜尋的一般 UCP。 每一行都會使用下列格式：

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    新增包含每個裝置特定 UDN 的行。

3.  執行 GenericUCP.exe。 [ **一般 UCP** ] 視窗隨即出現。

    ![一般 ucp 視窗](images/generic-ucp.png)

> [!Note]  
> **View Presentation** 和 **view Service Desc。** 功能不會在 c + + 範例程式碼中執行。

 

 

 




