---
description: 當應用程式呼叫繪圖函式來繪製圖形時，系統會將筆刷放置於繪製作業的開頭，然後將筆刷點陣圖中的圖元對應至視窗原點的工作區，也就是視窗的左上角。
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: 筆刷來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ccdc1dfa370ceb84216c89d562ef56dd206ce744b3be4fd38deb87175c1cf73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400388"
---
# <a name="brush-origin"></a>筆刷來源

當應用程式呼叫繪圖函式來繪製圖形時，系統會將筆刷放置於繪製作業的開頭，然後將筆刷點陣圖中的圖元對應至 *視窗原點* 的工作區，也就是視窗的左上角。 系統對應的圖元座標稱為 *筆刷原點*。 預設筆刷原點位於筆刷點陣圖的左上角，位於座標 (0，0) 。 然後系統會將筆刷複製到工作區，形成與點陣圖高度一樣的模式。 複製作業會繼續（逐列），直到填滿整個工作區為止。 不過，筆刷模式只會顯示在指定圖形的界限內。

在某些情況下，不應使用預設筆刷來源。 例如，應用程式可能需要使用相同的筆刷來繪製其父視窗和子視窗的背景，並將子視窗的背景與父視窗的背景混合。 若要這樣做，應用程式應該呼叫 [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) 函式，並將原點移至所需的圖元數目，以重設筆刷原點。  (應用程式可以藉由呼叫 [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) 函式來取得目前的筆刷原點。 ) 

下圖顯示使用應用程式定義的筆刷填滿的五方星形。 下圖顯示筆刷的放大影像，以及繪製作業開始時所對應的位置。

![圖例顯示筆刷原點對應至視窗來源](images/csbru-01.png)

 

 



