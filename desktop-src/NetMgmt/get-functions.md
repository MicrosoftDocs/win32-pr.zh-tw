---
title: 取得函式
description: 網路管理取得函式會取出網域的相關資訊。 您也可以呼叫這些函式來取得本機、全域、工作站和伺服器使用者帳戶的相關資訊。
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507292"
---
# <a name="get-functions"></a>取得函式

網路管理取得函式會取出網域的相關資訊。 您也可以呼叫這些函式來取得本機、全域、工作站和伺服器使用者帳戶的相關資訊。

網路管理取得功能如下所示。



| 函式                                                               | 描述                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | 傳回指定伺服器直接信任之網域的任何網域控制站的名稱。                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | 針對指定的網域，傳回網域主控站 (PDC) 的名稱。                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | 傳回第一個顯示資訊專案的索引，其名稱開頭為指定的字串或依字母順序排列在字串後面。 |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | 傳回使用者、電腦或通用群組帳戶資訊。                                                                             |



 

[**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)函數所傳回的資訊可在下列層級取得：

-   [**NET \_ 顯示 \_ 群組**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [**淨 \_ 顯示器 \_ 電腦**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [**NET \_ DISPLAY \_ 使用者**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




