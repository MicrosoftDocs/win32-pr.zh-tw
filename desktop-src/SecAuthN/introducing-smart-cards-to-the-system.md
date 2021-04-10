---
description: 在智慧卡子系統可以找到智慧卡之前，必須先將智慧卡引入系統。
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: 將智慧卡引入系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194510"
---
# <a name="introducing-smart-cards-to-the-system"></a>將智慧卡引入系統

在 [*智慧卡子系統*](../secgloss/s-gly.md) 可以找到 [*智慧卡*](../secgloss/s-gly.md)之前，必須先將智慧卡引入系統。 這通常是透過卡片製造商提供的智慧卡設定工具來完成。 此工具可能是磁片磁碟機上的一種程式， (與智慧卡) 、網站上可用的 ActiveX 控制項等等。

安裝工具必須提供下列有關卡片的資訊：

-   它的 [*ATR 字串*](../secgloss/a-gly.md)，以及選用的遮罩，用來做為識別卡片的輔助工具。
-   卡片所支援的智慧卡介面清單。
-   卡片的顯示名稱，用來識別使用者的卡片。 在大部分的情況下，使用者會將它提供給安裝工具。
-   與卡片相關聯的 [*主要服務提供者*](../secgloss/p-gly.md) (選擇性) ，可在透過 COM 介面存取卡片時使用。

為了簡化安裝工具，以及確保 [*智慧卡資料庫*](../secgloss/s-gly.md)的完整性，智慧卡子系統提供下列兩個功能。 [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) 會在資料庫中引進智慧卡，而 [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) 則會將它從資料庫中移除。

 

 
