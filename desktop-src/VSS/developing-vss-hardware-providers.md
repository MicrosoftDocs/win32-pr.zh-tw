---
description: 硬體提供者會執行 IVssProviderCreateSnapshotSet 和 IVssHardwareSnapshotProvider 介面。
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: 開發 VSS 硬體提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29533838b814a07f3da5310302a283f6cd60dc75779b4eb29dcdbf6b10816aa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032708"
---
# <a name="developing-vss-hardware-providers"></a>開發 VSS 硬體提供者

硬體提供者會執行 [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) 和 [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) 介面。 **IVssProviderCreateSnapshotSet** 會實行陰影複製狀態的排序。 **IVssHardwareSnapshotProvider** 會在 LUN 抽象上運作。 提供者必須實作為跨進程的 COM 伺服器。 提供者會使用提供者特定的機制 (通常私用 IOCTLs) 與具現化陰影複製 Lun 的儲存子系統進行通訊。

-   [陰影複製提供者註冊和載入](shadow-copy-provider-registration-and-loading.md)
-   [為提供者建立陰影複製](shadow-copy-creation-for-providers.md)
-   [硬體提供者互動和行為](hardware-provider-interactions-and-behaviors.md)

 

 



