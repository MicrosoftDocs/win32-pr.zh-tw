---
title: 提供狀態更新
description: 提供狀態更新
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- MCIWndSetActiveTimer 宏
- MCIWndSetInactiveTimer 宏
- MCIWndGetActiveTimer 宏
- MCIWndGetInactiveTimer 宏
- MCIWndSetTimers 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372111"
---
# <a name="providing-status-updates"></a>提供狀態更新

MCIWnd 會使用計時器，定期更新視窗標題列和捲軸中的資訊，並將通知訊息傳送至父視窗。 其中一個計時器控制作用中 MCIWnd 視窗的更新期間，而第二個計時器則控制非使用中 MCIWnd 視窗的更新期間。 您的應用程式可以使用 MCIWnd 計時器宏來取出目前的計時器設定，並調整更新期間。

您可以使用 [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) 宏來設定使用中視窗計時器所使用的更新期間。 此宏會設定 MCIWnd 用來更新提要欄位的期間，以更新視窗標題列中所報告的播放位置，以及通知父視窗該媒體已變更。 您可以使用 [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) 宏來取得使用中視窗計時器目前使用的更新期間。 使用中視窗計時器的預設更新期間是500毫秒。

您可以使用 [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) 宏來設定非作用中視窗計時器所使用的更新期間。 此宏會設定 MCIWnd 用來更新標題的期間，以更新在視窗標題中報告的播放位置，以及通知父視窗該媒體已變更。 您可以使用 [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) 宏來取出非使用中視窗計時器目前使用的更新期間。 非作用中視窗計時器的預設更新期間是2000毫秒。

您的應用程式可以使用 [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) 宏同時設定這兩個計時器的更新期間。 更新週期值的儲存體限制為16位。 如果需要更新期間的較大數量，請個別設定計時器。

 

 




