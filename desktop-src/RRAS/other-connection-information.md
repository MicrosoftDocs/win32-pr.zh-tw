---
title: 其他連接資訊
description: RASDIALPARAMS 結構的成員也可以指定下列連接資訊。
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933346"
---
# <a name="other-connection-information"></a><span data-ttu-id="ad62c-103">其他連接資訊</span><span class="sxs-lookup"><span data-stu-id="ad62c-103">Other Connection Information</span></span>

<span data-ttu-id="ad62c-104">[**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構的成員也可以指定下列連接資訊。</span><span class="sxs-lookup"><span data-stu-id="ad62c-104">The members of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure can also specify the following connection information.</span></span>

-   <span data-ttu-id="ad62c-105">用來覆寫電話簿輸入電話號碼的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="ad62c-105">A phone number to override the number in the phone-book entry.</span></span>
-   <span data-ttu-id="ad62c-106">遠端伺服器可回呼以建立連線的 [回呼](callback-connections.md) 電話號碼。</span><span class="sxs-lookup"><span data-stu-id="ad62c-106">A [callback](callback-connections.md) phone number that the remote server can call back to establish the connection.</span></span>
-   <span data-ttu-id="ad62c-107">要在其上進行驗證的遠端網路網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad62c-107">The name of the remote network domain on which the authentication is to occur.</span></span>

<span data-ttu-id="ad62c-108">針對回呼號碼和網域， [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) 成員可以指出 RAS 應使用電話簿專案中的資訊，或者可以提供覆寫電話簿資料的資訊。</span><span class="sxs-lookup"><span data-stu-id="ad62c-108">For the callback number and the domain, the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) members can either indicate that RAS should use the information in the phone-book entry, or it can provide information that overrides the phone-book data.</span></span>

<span data-ttu-id="ad62c-109">RAS 用戶端可以使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)函式的 *lpRasDialExtensions* 參數，來控制 RAS 是否使用電話簿輸入中指定的電話號碼首碼或尾碼。</span><span class="sxs-lookup"><span data-stu-id="ad62c-109">A RAS client can use the *lpRasDialExtensions* parameter of the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to control whether RAS uses a phone number prefix or suffix specified in a phone-book entry.</span></span>

 

 