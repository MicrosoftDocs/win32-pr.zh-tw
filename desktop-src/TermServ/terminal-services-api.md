---
title: 遠端桌面服務 API
description: 遠端桌面服務 API 主要適用于遠端桌面服務管理的用戶端/伺服器應用程式和應用程式。
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839784"
---
# <a name="remote-desktop-services-api"></a>遠端桌面服務 API

大部分的應用程式都不需要修改就能在遠端桌面服務 (之前稱為終端機服務) 環境中執行，也不需要使用遠端桌面服務 API。 遠端桌面服務 API 主要適用于遠端桌面服務管理的用戶端/伺服器應用程式和應用程式。

遠端桌面服務 API 是一組 Wtsapi32.dll 的函式呼叫。 若要將您的應用程式設計成在遠端桌面服務和非遠端桌面服務環境中執行，請使用執行時間動態連結來檢查 Wtsapi32.dll 是否存在。 如需詳細資訊，請參閱 [執行時間連結至 Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)。

遠端桌面服務 API 可讓應用程式在遠端桌面服務環境中執行下列工作：

-   [遠端桌面服務系統管理](terminal-services-administration.md)，例如列舉和管理遠端桌面工作階段主機 (RD 工作階段主機) 伺服器 (先前稱為終端機伺服器) 網域中，或在 RD 工作階段主機伺服器上列舉和管理會話和進程。
-   強化遠端桌面服務環境中的用戶端/伺服器應用程式。
-   使用 [遠端桌面服務的虛擬通道](terminal-services-virtual-channels.md) 在應用程式的用戶端和伺服器模組之間進行通訊。
-   [設定和取出遠端桌面服務特定的使用者設定資訊](terminal-services-user-configuration.md)。

 

 




