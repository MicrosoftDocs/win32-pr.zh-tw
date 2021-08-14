---
title: ARIA Tabindex 錯誤
description: ARIA Tabindex 錯誤
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1637008b6679f196f7bba0701606e0514abe44410032e1a5ffc063977ddf10e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326742"
---
# <a name="aria-tabindex-error"></a>ARIA Tabindex 錯誤

## <a name="text"></a>Text

元素不是停用的，而且具有 **click** 事件處理常式，但它的 **tabIndex** < 為0，預設不在定位順序中。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于具有 click 事件處理常式且未停用的元素。 這些元素必須在定位順序中。 這可確保可以使用 Tab 鍵來觸達元素，這就是螢幕瀏覽器使用者通常流覽 UI 的方式。

若要修正這個錯誤，請將 [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) 屬性設定為等於或大於0的值。 根據預設，您不需要針對位於定位順序中的標記明確地設定 **tabindex** 屬性，例如具有 href 屬性 [**的 (（**](https://developer.mozilla.org/docs/Web/HTML/Element/a)例如具有 [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes)屬性的）) 、[**按鈕**](https://developer.mozilla.org/docs/Web/HTML/Element/button)、[**輸入**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (不包括「隱藏」 ) 、[**選取**](https://developer.mozilla.org/docs/Web/HTML/Element/select)、文字區 [**和**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)[**區域**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (作為影像地圖) 的一部分。

## <a name="example"></a>範例


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




