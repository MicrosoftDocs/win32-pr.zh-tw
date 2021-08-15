---
title: Web 應用程式 Proxy
description: Web 應用程式 Proxy
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a346297dca0a81d8c2269b61e8a5d581f03f95fab56e044bedce7513882535f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211323"
---
# <a name="web-application-proxy"></a>Web 應用程式 Proxy

## <a name="platform"></a>平台

**伺服器-** Windows Server 2012 R2  






## <a name="description"></a>Description

在 Windows Server 2012 R2 中，我們已在遠端存取角色下新增名為 Web 應用程式 Proxy 的服務，讓系統管理員可以發佈應用程式以進行外部存取。 這種服務會作為反向 proxy，並做為 Active Directory 同盟服務 (AD FS) proxy。 事實上，這項服務會取代 Windows Server 2012 中已知的 AD FS proxy 服務。

使用 Web 應用程式 Proxy 時，組織可以讓內部部署 Web 資源可供外部存取，同時也能控制 AD FS 上的驗證和授權原則，藉此管理此存取的風險。

## <a name="manifestation"></a>表現

AD FS proxy 服務已不再位於 Active Directory 同盟服務角色 (AD FS) ，但已由遠端存取角色下的 Web 應用程式 Proxy 取代。 這代表 AD FS proxy 服務的擴充，包括應用程式發行的反向 proxy 功能。

## <a name="solution"></a>解決方案

若要存取 Web 應用程式 Proxy，系統管理員可以移至伺服器管理員並新增角色/角色服務。 系統管理員會在遠端存取角色下找到 Web 應用程式 Proxy。

## <a name="resources"></a>資源

-   [解決方案指南](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 