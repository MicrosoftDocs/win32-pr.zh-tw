---
description: 關於當的架構
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: 關於當的架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194943"
---
# <a name="about-the-acm-architecture"></a>關於當的架構

自動設定模組 (的配置) 是適用于 Windows Vista 的新無線設置元件。 Windows XP Service Pack 3 (SP3) 和適用于 Windows XP Service Pack 2 (SP2 的無線區域網路 API) 改為使用無線零設定 (WZC) 服務。

當該網路有啟用自動連線的介面時，會定期掃描網路，並使用反復的程式來選取並聯機到範圍內最慣用的網路。 此設定檔也會儲存並取出網路設定檔，其中包含配置配置、媒體特定模組 (MSM) 、安全性和獨立硬體廠商 (IHV) 設定。 這些網路設定檔適用于自動設定。

自動設定同時支援全域和個別介面設定和網路設定檔。 如果電腦已加入具有群組原則物件的網域 (GPO) 在網域層級或組織單位 (OU) 層級的 Active Directory (AD) 階層中，就會設定全域設定和網路設定檔。 這些群組原則設定和設定檔是唯讀的，會套用至系統中的每個802.11 介面，且一律優先于每個介面和個別使用者的設定和網路設定檔。 群組原則設定檔會放在每個802.11 網路介面上慣用網路設定檔案清單的頂端。

可延伸的架構是可延伸的。 Ihv 可以實行專屬的無線功能，而不需要改變所提供的原生802.11 架構。 公開的 IHV 控制函式和結構可啟用此擴充性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於原生 Wifi](about-native-wifi.md)
</dt> </dl>

 

 



