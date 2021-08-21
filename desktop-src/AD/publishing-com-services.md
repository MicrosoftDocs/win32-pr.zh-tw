---
title: 發行 COM + 服務
description: 以 COM 為基礎的服務會以 Windows 安裝程式 (MSI) 套件的形式提供應用程式 proxy。
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- 發行 COM + 服務
- Active Directory、使用、發行服務、COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91801bbfcbf8efa34ac0b79477dd9d859fc2ed34a8d40bcf0bd829f82cfd571a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025426"
---
# <a name="publishing-com-services"></a>發行 COM + 服務

以 COM 為基礎的服務會以 Windows 安裝程式 (MSI) 套件的形式提供應用程式 proxy。 此 .msi 檔案包含要使用的伺服器名稱，以及其他必要的元素，例如封送處理所需的 proxy/stub 和類型程式庫。 [元件服務] 嵌入式管理單元會自動產生 COM + 伺服器應用程式的這些應用程式 proxy。

應用程式 proxy 會使用群組原則編輯器，發佈到 Active Directory 的原則物件中。 用戶端應用程式不需要任何特殊介入。 用戶端電腦上的電腦/使用者帳戶必須位於設定為使用發行應用程式 proxy 之原則物件的 OU 中。 當用戶端建立相關物件的實例時，COM 系結器會自動透過目錄來尋找伺服器。

 

 




