---
description: 應用程式可以藉由呼叫 PathToRegion 函數，將路徑轉換成區域。
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: 將路徑轉換成區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d404aa50669fe2349b3e39f172dd652ef765c9de8c615cde446e8540e6051bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062458"
---
# <a name="conversion-of-paths-to-regions"></a>將路徑轉換成區域

應用程式可以藉由呼叫 [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) 函數，將路徑轉換成區域。 如同 [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)， **PathToRegion** 在建立特殊圖形效果方面很有用。 例如，沒有可允許應用程式位移路徑的函式;不過，有一個函式可讓應用程式 ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)) 來位移區域。 使用 **PathToRegion** ，應用程式可以藉由建立定義圖形的路徑、將路徑轉換成區域 (藉由呼叫 **PathToRegion**) ，然後重複繪製、移動和清除區域 (（例如 [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn)、 **OffsetRgn** 和 **FillRgn**) ），來建立複雜圖形的動畫效果。

 

 



