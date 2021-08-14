---
description: 有些應用程式需要在事件發生之前，或在事件發生時，或兩者都收到連接事件的通知。 您可以建立 DLL，以接收連接事件的前進和事後通知。
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: 接收連接通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a581855ef134536df8c4c728521e796e541c963a780e2f572ad88dc704c677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919687"
---
# <a name="receiving-connection-notifications"></a>接收連接通知

有些應用程式需要在事件發生之前，或在事件發生時，或兩者都收到連接事件的通知。 您可以建立 DLL，以接收連接事件的前進和事後通知。

遠端存取服務 (RAS) ，是需要接收連接事件之提前通知的應用程式範例。 必須先通知 RAS，才能進行連線，因為可能需要先建立數據機連線，才能進行網路連線。

同樣地，在建立連線之後，應用程式可能需要清除資源，因此需要連接後通知。

有興趣接收「前進」和「事後」連接事件通知的應用程式，必須提供可匯出兩個函式（ [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) 和 [**CANCELCONNECTNOTIFY**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify)）的 DLL。

在您執行這些函式之後，您必須依照 [註冊接收連接通知](registering-to-receive-connection-notifications.md)中所述的方式註冊 DLL。

 

 



