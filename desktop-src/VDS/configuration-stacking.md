---
description: 設定堆疊
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: 設定堆疊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567838"
---
# <a name="configuration-stacking"></a>設定堆疊

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

堆疊牽涉到一組邏輯區塊對應的串連。 您可以從一個 LUN 下的相同子系統堆疊多個 Lun。 您可以將 LUN 與同一個磁片區中相同套件的磁片區堆疊在一起。 此外，您可以堆疊一個磁片區下的異類子系統所呈現的多個 Lun。

如下圖所示，建立磁片區並不會變更參與 LUN 的現有系結。 同樣地，解除系結也不會解除系結參與的 LUN。 下圖描述 RAID 0 1 (0 + 1) 設定。 這項知名設定結合了分割 (RAID 0) 和鏡像 (RAID 1) ，可將 RAID 0 的快速資料存取與 RAID 1 的可靠性配對在一起。

![顯示 RAID 0 1 (0 + 1) 設定的圖表。](images/vdsstacklunvolzeroplusone.png)

參與 Lun 的系結類型可能不同。 有許多設定都可以使用 VDS，但很不可能發生，例如下圖。 在此範例中，一個磁片區 plex 是等量 LUN，另一個則是三向鏡像 LUN。

![顯示 VDS 設定的圖表，其中一個磁片區 plex 是等量 LUN，另一個則是三向鏡像 LUN。](images/vdsstacklunvol.png)

雖然不實用，但此範例說明堆疊的重要層面。 由於堆疊串連了 plex，因此 VDS 會將三個 LUN 的 plex 新增至兩個磁片區的 plex，總共有五個 plex。

 

 
