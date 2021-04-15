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
# <a name="ras-user-administration-functions"></a><span data-ttu-id="6e0a3-103">RAS 使用者管理功能</span><span class="sxs-lookup"><span data-stu-id="6e0a3-103">RAS User Administration Functions</span></span>

<span data-ttu-id="6e0a3-104">使用下列功能來管理撥號使用者：</span><span class="sxs-lookup"><span data-stu-id="6e0a3-104">Use the following functions to manage dial-up users:</span></span>

-   [<span data-ttu-id="6e0a3-105">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="6e0a3-105">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [<span data-ttu-id="6e0a3-106">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="6e0a3-106">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [<span data-ttu-id="6e0a3-107">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="6e0a3-107">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [<span data-ttu-id="6e0a3-108">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="6e0a3-108">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

<span data-ttu-id="6e0a3-109">若要取得特定網域上的目前使用者清單，請使用 [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) 函數。</span><span class="sxs-lookup"><span data-stu-id="6e0a3-109">To obtain a list of current users on a particular domain, use the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function.</span></span> <span data-ttu-id="6e0a3-110">這個函式的原型位於 lmaccess .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="6e0a3-110">The prototype for this function is in the lmaccess.h header file.</span></span>

 

 