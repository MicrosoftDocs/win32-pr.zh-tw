---
title: RAS 使用者管理功能
description: 使用下列功能來管理撥號使用者
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf8c1e7df962eff2064dac06da256f3a78e8ed17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463585"
---
# <a name="ras-user-administration-functions"></a>RAS 使用者管理功能

使用下列功能來管理撥號使用者：

-   [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

若要取得特定網域上的目前使用者清單，請使用 [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) 函數。 這個函式的原型位於 lmaccess .h 標頭檔中。

 

 