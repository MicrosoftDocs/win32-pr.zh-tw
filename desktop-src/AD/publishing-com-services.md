---
title: 發行 COM + 服務
description: 以 COM 為基礎的服務會以 Windows installer (MSI) 封裝的形式提供應用程式 proxy。
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- 發行 COM + 服務
- Active Directory、使用、發行服務、COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020834"
---
# <a name="publishing-com-services"></a>發行 COM + 服務

以 COM 為基礎的服務會以 Windows installer (MSI) 封裝的形式提供應用程式 proxy。 這個 .msi 檔案包含要使用的伺服器名稱，以及其他必要的元素，例如封送處理所需的 proxy/stub 和類型程式庫。 [元件服務] 嵌入式管理單元會自動產生 COM + 伺服器應用程式的這些應用程式 proxy。

應用程式 proxy 會使用群組原則編輯器，發佈到 Active Directory 的原則物件中。 用戶端應用程式不需要任何特殊介入。 用戶端電腦上的電腦/使用者帳戶必須位於設定為使用發行應用程式 proxy 之原則物件的 OU 中。 當用戶端建立相關物件的實例時，COM 系結器會自動透過目錄來尋找伺服器。

 

 




