---
description: 硬體提供者互動和行為
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: 硬體提供者互動和行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192291"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>硬體提供者互動和行為

硬體提供者可能會支援寫入時複製和/或完整複製鏡像 (差異和/或 plex) 陰影複製。 陰影複製的資源配置應遵循 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)中要求者所指定的內容，並以 [**\_ VSS \_ 快照集 \_ 內容**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)為陰影複製集進行列舉。

-   如果要求者指定提供者所支援的陰影複製內容，則提供者應該使用該方法建立陰影複製。
-   如果要求者指定提供者不支援的陰影複製內容，則提供者不應嘗試建立陰影複製，並透過 [**IVssHardwareSnapshotProvider：： AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported)中的 *PbIsSupported* 參數傳回 **FALSE** 。
-   如果要求者未明確指定陰影複製內容，則提供者應該使用合理的預設行為來建立陰影複製。

與 SAN RAID 子系統相關聯的硬體提供者應該支援可轉移的陰影複製，以允許在 SAN 上的主機之間進行移動。

在 SAN 上的多部機器上執行的硬體提供者，但管理相同的 RAID 子系統並不需要在 SAN 上的提供者之間協調。 協調器會維持任何必要的狀態。 可辨識的狀態有兩種：

-   支援資料存取硬體陰影複製上所含磁片區所需的狀態。 這包括將磁片區標記為唯讀或隱藏。 此狀態必須位於硬體 LUN 上，並與 LUN 一起移動。 此狀態會在開機 epoch 和/或裝置探索之間保留。 VSS 會在陰影複製的存留期內管理此狀態。
-   將特定磁片區辨識為陰影複製集一部分所需的狀態。 此狀態是由 VSS 與最初建立陰影複製集的要求者一起保存。

如需詳細資訊，請參閱下列主題：

-   [陰影複製建立程式](the-shadow-copy-creation-process.md)
-   [陰影複製提供者的必要行為](required-behaviors-for-shadow-copy-providers.md)
-   [陰影複製提供者中的狀態轉換](state-transitions-in-shadow-copy-providers.md)
-   [陰影複製提供者中的錯誤處理](error-handling-in-shadow-copy-providers.md)

 

 



