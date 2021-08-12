---
title: VML InvX 屬性
description: VML InvX 屬性
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e040c4ff013ec9c2a606e1034458f9149d666813dd42341d9ec68a39901094b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600124"
---
# <a name="vml-invx-attribute"></a>VML InvX 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷控制碼的 x 位置是否反轉。 讀取/寫入 **VgTriState**。

**適用於**

[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) 

**標記語法**

<v： *element* invx = " *expression* " >

**備註**

若 **為 True**，則會將 **CoordOrigin** x 值的 x 值減去 **CoordSize** 的 x 值，以反轉控制碼的 x 位置。 預設值為 **[False]** 。

這個屬性等同于

coordorigin. x + coordsize. x-h. x

*VML 標準屬性*

 

 