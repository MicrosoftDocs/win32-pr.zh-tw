---
title: VML 參數屬性
description: VML 參數屬性
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d102d6af20e698d8ec281cb1be6fae9690de4e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967262"
---
# <a name="vml-switch-attribute"></a>VML 參數屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否要交換控制碼方向。 讀取/寫入 **VgTriState**。

**適用於**

[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) 

**標記語法**

<v： *element* switch = " *expression* " >

**備註**

若 **為 True**，則當圖形高度高於寬度時，會在 x 和 y 方向之間切換控制碼。 預設值為 **[False]** 。

這個屬性會用於具有 limo 延展行為的圖形。

*VML 標準屬性*

 

 