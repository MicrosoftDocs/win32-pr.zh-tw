---
title: 應用程式修復和重新開機函式
description: 應用程式復原和重新開機會定義下列功能
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092995"
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



 

 

 