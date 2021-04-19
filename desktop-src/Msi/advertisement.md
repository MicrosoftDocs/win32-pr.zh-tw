---
description: Windows Installer 可以將應用程式的可用性通告給使用者或其他應用程式，而無須實際安裝應用程式。
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: 廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999882"
---
# <a name="advertisement"></a>廣告

Windows Installer 可以將應用程式的可用性通告給使用者或其他應用程式，而無須實際安裝應用程式。 如果已公告應用程式，則只會對使用者或其他應用程式顯示載入和啟動應用程式所需的介面。 如果使用者或應用程式啟動已公告的介面，安裝程式就會繼續安裝所需的元件，如 [隨選安裝](installation-on-demand.md)所述。

這兩種類型的廣告是指派和發佈的。 當應用程式指派給使用者時，應用程式就會顯示安裝給使用者。 [ **開始** ] 功能表包含適當的快捷方式、顯示圖示、檔案與應用程式相關聯，以及登錄專案會反映應用程式的安裝。 當使用者嘗試開啟指派的應用程式時，它會隨選安裝。

安裝程式會根據作業系統支援應用程式和功能的公告。 安裝程式會從 Windows XP 開始，為指派的應用程式註冊 COM 類別資訊。 這可讓安裝程式在建立已公告類別的實例時，安裝應用程式。 如需詳細資訊，請參閱 [廣告的平臺支援](platform-support-of-advertisement.md)。

您可以從 Windows Server 2003 開始的伺服器發行應用程式。 然後，已發佈的應用程式會透過其檔案關聯或多用途網際網路郵件延伸模組 (MIME) 類型進行安裝。 發佈時，不會在使用者介面中填入任何應用程式的圖示。 用戶端作業系統可以從 Windows XP 開始安裝已發佈的應用程式。

 

 



