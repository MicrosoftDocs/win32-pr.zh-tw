---
title: 使用 Windows 通訊端註冊發佈 & 解析
description: Windows 通訊端服務可以使用註冊和解析 (RnR) Api 來發佈服務，以及查閱以 RnR 發佈的服務。
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows 通訊端註冊和解析 AD，發行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/04/2019
ms.locfileid: "104462632"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>使用 Windows 通訊端註冊發佈 & 解析

Windows 通訊端服務可以使用註冊和解析 (RnR) Api 來發佈服務，以及查閱以 RnR 發佈的服務。 RnR 發行會以兩個步驟進行。 第一個步驟會安裝服務類別，以將 GUID 與服務的名稱產生關聯。 服務類別可保存服務特定的設定資料。 接著，服務會將自己發佈為服務類別的實例。 發佈時，用戶端可以使用 RnR Api 來查詢指定類別之實例的目錄服務，並選取要系結的實例。 當不再需要類別時，就可以將它移除。

 

 




