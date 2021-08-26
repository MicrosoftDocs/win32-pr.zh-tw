---
title: 應用程式修復和重新開機函式
description: 應用程式復原和重新開機會定義下列功能
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df0a2139a24c3e69ae328533d6bf8b1baeee2043bc82b9f8d50f4272a16e2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024618"
---
# <a name="application-recovery-and-restart-functions"></a>應用程式修復和重新開機函式

應用程式復原和重新開機會定義下列功能：



| 函式                                                                               | 描述                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | 指出呼叫的應用程式已完成其資料復原。                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | 指出呼叫的應用程式繼續復原資料。                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | 抓取已針對指定進程註冊之復原回呼常式的指標。 |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | 抓取為指定進程註冊的重新開機資訊。                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | 註冊應用程式的使用中實例以進行復原。                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | 註冊應用程式的使用中實例以重新開機。                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | 從復原清單中移除應用程式的使用中實例。                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | 從重新開機清單中移除應用程式的使用中實例。                       |



 

 

 