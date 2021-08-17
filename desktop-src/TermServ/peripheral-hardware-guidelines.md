---
title: 週邊硬體指導方針
description: 如果其硬體裝置不是設計來透過遠端會話運作，廠商必須確保設備磁碟機軟體強制使用系統原則或群組原則來停用裝置的重新導向。
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0cbe39010eaa59d4207ad28722521793fe33a04f9d06591f21f8ac381940235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756267"
---
# <a name="peripheral-hardware-guidelines"></a>週邊硬體指導方針

在遠端桌面連線 (RDC) 用戶端上，遠端桌面工作階段主機 (RD 工作階段主機伺服器是本機電腦。 因此，連接到伺服器的裝置（如磁片磁碟機和印表機）會顯示為用戶端的本機裝置。 相反地，連接至用戶端終端機的磁片磁碟機和印表機可能會顯示為遠端裝置，視針對連線選取的選項、使用的伺服器和使用的用戶端軟體版本而定。

雖然初始版本的遠端桌面服務不支援將輸出直接傳送到連接至用戶端終端機的序列、平行和音效埠的應用程式，但目前的版本可讓這些裝置顯示為在遠端桌面服務會話中執行之應用程式的本機裝置。

如果其硬體裝置不是設計來透過遠端會話運作，廠商必須確保設備磁碟機軟體強制使用系統原則或群組原則來停用裝置的重新導向。

 

 




