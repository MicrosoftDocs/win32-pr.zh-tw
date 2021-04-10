---
title: 使用者驗證資訊
description: 用戶端電腦上的遠端存取連線管理員服務，會將使用者名稱和密碼傳送至遠端電腦上的 RAS 伺服器。
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842367"
---
# <a name="user-authentication-information"></a><span data-ttu-id="09652-103">使用者驗證資訊</span><span class="sxs-lookup"><span data-stu-id="09652-103">User Authentication Information</span></span>

<span data-ttu-id="09652-104">用戶端電腦上的遠端存取連線管理員服務，會將使用者名稱和密碼傳送至遠端電腦上的 RAS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="09652-104">The Remote Access Connection Manager service on the client computer sends a user name and password to the RAS server on the remote computer.</span></span> <span data-ttu-id="09652-105">在建立連接之前，遠端伺服器會使用此資訊來驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="09652-105">Before it establishes a connection, the remote server uses this information to authenticate the user.</span></span> <span data-ttu-id="09652-106">根據預設，遠端存取連線管理員傳送目前登入之使用者的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="09652-106">By default, the Remote Access Connection Manager sends the user name and password of the currently logged-on user.</span></span> <span data-ttu-id="09652-107">RAS 用戶端可以使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫中指定的 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構，來指定不同的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="09652-107">The RAS client can use the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure specified in the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call to specify a different user name and password.</span></span>

<span data-ttu-id="09652-108">如果遠端伺服器無法以指定的資訊驗證使用者，則可以允許線上作業進入 [暫停狀態](paused-states.md) ，讓 RAS 用戶端向使用者收集不同的驗證資料。</span><span class="sxs-lookup"><span data-stu-id="09652-108">If the remote server cannot authenticate the user with the specified information, it can allow the connection operation to enter a [paused state](paused-states.md) to enable the RAS client to collect different authentication data from the user.</span></span>

 

 