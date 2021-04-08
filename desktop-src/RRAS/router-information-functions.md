---
title: 路由器資訊函式
description: 使用下列功能來操作路由器資訊標頭和區塊。 資訊標頭是由私用中繼資料和資訊區塊所組成。 資訊區塊是各種類型之資訊結構的陣列。
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020717"
---
# <a name="router-information-functions"></a>路由器資訊函式

使用下列功能來操作路由器資訊標頭和區塊。 資訊標頭是由私用中繼資料和資訊區塊所組成。 資訊區塊是各種[類型](router-information-enumerations.md)之[資訊結構](router-information-structures.md)的陣列。

下列函式會操作資訊標頭：

-   [**MprInfoCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [**MprInfoDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [**MprInfoDuplicate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [**MprInfoRemoveAll**](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

下列函式會操作資訊標頭中的資訊區塊：

-   [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [**MprInfoBlockQuerySize**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

許多 [路由器管理和設定函數](understanding-mprinfo-functions-and-information-headers.md) 都會使用資訊標頭。

 

 




