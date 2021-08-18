---
title: VML RadiusRange 屬性
description: VML RadiusRange 屬性
ms.assetid: bff2b185-7683-4994-9104-09a7579f963d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28e086ef45f60445f63d094934258832fa7e63b58f95f09b1391318d8283fea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007668"
---
# <a name="vml-radiusrange-attribute"></a>VML RadiusRange 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義極座標控點的範圍。 讀取/寫入 **VgVector2D**。

**適用於**

[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) 

**標記語法**

<v： *element* radiusrange = " *expression* " >

**備註**

定義星形控制碼的最小值和最大值。 每個值都可以是常數或公式。 如果未定義某個值，則可以在星形方向中移動控點，而不受限制。 這個屬性只適用于極座標控點。 預設值為 0,0。

*VML 標準屬性*

 

 