---
description: 限制模式設定檔和設定建立
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: 限制模式設定檔和設定建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bb4d4bea3f42eaf897e781ccf859d094a0d0321815e7457aa6c79f96cb5ded
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747048"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>限制模式設定檔和設定建立

由於 DirectX VA 可以解碼各種類型的資料，針對上述每一種類型的資料，在 DirectX VA 中支援的多個解碼設定 (例如，使用位流緩衝區與主機剩餘差異解碼的比較，或不加密每個相關類型的緩衝區，而不加密每個相關的緩衝區類型，因此在) 上，我們相信您只需要為每個唯一的資料類型和解碼設定指定唯一的 GUID。 這會建立大量的 Guid (例如，如果每個都有16個 DirectX VA 和16設定的設定檔，則需要有256個定義的 Guid，而只需要 4 kb 的記憶體就能容納全部。 此問題是決定如何將 DirectX VA 對應到 **IAMVideoAccelerator** 的最困難部分，而作業定義的其餘部分大多相當簡單。 因此，我們只會針對每個受限制模式配置) 檔的資料類型 (指定唯一的 GUID，並允許額外的 GUID 與每一種加密類型相關聯。 然後，會使用探查和鎖定作業來建立每個 DirectX VA 函式類型的設定，以使用探查和鎖定作業來建立解碼器與加速器之間的解碼設定。

 

 



