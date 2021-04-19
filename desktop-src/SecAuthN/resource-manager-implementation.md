---
description: 資源管理員會在單一進程中以受信任服務的形式執行。 所有智慧卡存取的要求都是對資源管理員進行，它會將這些要求路由傳送至包含目標卡片的讀取器。
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Resource Manager 的執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982403"
---
# <a name="resource-manager-implementation"></a>Resource Manager 的執行

[*資源管理員*](../secgloss/r-gly.md)會在單一進程中以受信任服務的形式執行。 所有 [*智慧卡*](../secgloss/s-gly.md) 存取的要求都是對資源管理員進行，它會將這些要求路由傳送至包含目標卡片的 [*讀取器*](../secgloss/r-gly.md) 。

智慧卡通常會與安全性和個人隱私一起使用。 在可能的情況下，資源管理員會在存取讀取器或智慧卡時，使用基礎作業系統內現有的安全性機制。

 

 
