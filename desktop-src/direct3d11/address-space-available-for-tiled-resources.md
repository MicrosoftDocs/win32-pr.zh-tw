---
title: 磚資源可用的位址空間
description: 此區段會指定可用於並排顯示資源的虛擬位址空間。
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5753fdb9d700689c6ebfffdae4368399c0e4bb36d328c9ff1a8cfc284005214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734280"
---
# <a name="address-space-available-for-tiled-resources"></a>磚資源可用的位址空間

此區段會指定可用於並排顯示資源的虛擬位址空間。

在 64 位元作業系統上，有至少 40 位元的虛擬位址空間 (1 Tb) 可用。

若為 32 位元的作業系統，位址空間為 32 位元 (4 GB)。 針對32位 ARM 系統，如果配置使用超過27位的位址空間 (128 MB) ，則建立個別的磚資源可能會失敗。 這包括位址中任何隱藏的邊框間距，硬體空間可能會將其用於 Mipmap、壓縮磚邊框間距，以及 2 之乘冪的邊框間距表面維度。

在使用不同分頁表的圖形處理器 (GPU) 圖形系統上，應用程式所做的 GPU 資源將可使用多數此種位址空間，即便顯示器驅動程式所做的 GPU 配置可納於相同的空間。

在 CPU 和 GPU 所共用之分頁表的未來系統上，處理程序的所有 CPU 和 GPU 配置會共用可用位址空間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源建立參數](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




