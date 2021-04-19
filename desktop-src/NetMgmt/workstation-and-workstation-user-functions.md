---
title: 工作站和工作站使用者功能
description: 網路管理工作站功能會在本機或遠端工作站上執行系統管理工作。
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969925"
---
# <a name="workstation-and-workstation-user-functions"></a>工作站和工作站使用者功能

網路管理工作站功能會在本機或遠端工作站上執行系統管理工作。 只有在本機或遠端伺服器上具有系統管理員群組成員資格的使用者或應用程式，才可以在工作站上執行系統管理工作，以控制其作業、使用者存取和資源分享。 如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。

工作站功能如下所示。



| 函式                                   | 描述                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | 傳回工作站設定元素的相關資訊。 |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | 設定工作站。                                               |



 

工作站功能允許存取兩種不同類型的工作站資訊：

-   系統資訊
-   平臺特定資訊

在每一種類型中，資料都會依安全性存取進行分類。 可存取來賓的資料是可供使用者存取的資料子集，也就是系統管理員可存取資料的子集。

下列層級提供工作站資訊：

-   [**WKSTA \_ 資訊 \_ 100**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [**WKSTA \_ 資訊 \_ 101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [**WKSTA \_ 資訊 \_ 102**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

網路管理工作站使用者功能允許存取使用者特定的資訊。 使用者特定的資訊與工作站資訊分開，因為工作站上可以有多個使用者。

工作站使用者函式如下所示。



| 函式                                           | 描述                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | 列出所有目前登入工作站的使用者的相關資訊。           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | 傳回一個目前登入使用者的相關資訊。                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | 設定工作站設定元素的使用者特定資訊。 |



 

工作站使用者資訊可在下列層級取得：

-   [**WKSTA \_ 使用者 \_ 資訊 \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [**WKSTA \_ 使用者 \_ 資訊 \_ 1**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [**WKSTA \_ 使用者 \_ 資訊 \_ 1101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 