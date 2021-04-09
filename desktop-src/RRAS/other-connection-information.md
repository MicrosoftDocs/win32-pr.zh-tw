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
# <a name="other-connection-information"></a>其他連接資訊

[**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構的成員也可以指定下列連接資訊。

-   用來覆寫電話簿輸入電話號碼的電話號碼。
-   遠端伺服器可回呼以建立連線的 [回呼](callback-connections.md) 電話號碼。
-   要在其上進行驗證的遠端網路網域的名稱。

針對回呼號碼和網域， [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) 成員可以指出 RAS 應使用電話簿專案中的資訊，或者可以提供覆寫電話簿資料的資訊。

RAS 用戶端可以使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)函式的 *lpRasDialExtensions* 參數，來控制 RAS 是否使用電話簿輸入中指定的電話號碼首碼或尾碼。

 

 