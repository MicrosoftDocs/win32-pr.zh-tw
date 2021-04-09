---
title: 編輯 Windows 95 登錄
description: 您可以使用 REGEDIT 來編輯 Windows 95 登錄，以指定 NSP。
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840656"
---
# <a name="editing-the-windows-95-registry"></a>編輯 Windows 95 登錄

您可以使用 REGEDIT 來編輯 Windows 95 登錄，以指定 NSP。

**為 Windows 95 指定 Microsoft 定位器名稱服務提供者**

1.  選取

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Rpc**

2.  建立稱為的新機碼

    **NameService**

3.  選取 **NameService** 索引鍵時，請建立新的 **StringValue** 名稱，並將其修改為包含下表所示的資料。

    

    | Name                     | 資料                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                                |
    | **通訊協定**             | ncacn \_ np<br/>                                                        |
    | **端點**             | \\管道 \\ 定位器<br/>                                                  |
    | **Networkaddress.cache.ttl**       | myserver (其中 myserver 是 Windows NT 電腦的名稱) <br/> |
    | **ServerNetworkAddress** | myserver<br/>                                                         |

    

     

您可以使用 REGEDIT 來編輯 Windows 95 登錄，以指定 DCE CD NSP。

**為 Windows 95 指定 DCE CD 名稱服務提供者**

1.  選取

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Rpc**

2.  建立稱為的新機碼

    **NameService**

3.  選取 **NameService** 索引鍵時，請建立新的 **StringValue** 名稱，並將其修改為包含下表所示的資料。

    

    | Name                     | 資料                                                             |
    |--------------------------|------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                     |
    | **通訊協定**             | ncacn \_ ip \_ tcp<br/>                                        |
    | **端點**             | "" (空字串) <br/>                                  |
    | **Networkaddress.cache.ttl**       | myserver (執行 nsid 的主電腦名稱稱) <br/> |
    | **ServerNetworkAddress** | myserver (執行 nsid 的主電腦名稱稱) <br/> |

    

     

    > [!Note]  
    > 您必須具有數位設備公司的 DCE Cell Directory 服務產品，才能將 DCE CD 設定為您的名稱服務提供者。 請參閱數位設備公司提供的檔，以取得 DCE CD 的相關資訊。

     

 

 





