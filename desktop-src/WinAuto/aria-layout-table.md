---
title: ARIA 展示表錯誤
description: ARIA 展示表錯誤
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896c7ec4061119535ed544cfc41598c1387d98011eb275f6a0345d9334a7dc9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122280"
---
# <a name="aria-presentation-table-error"></a>ARIA 展示表錯誤

## <a name="text"></a>Text

用於配置的資料表不能有標頭、可存取的名稱或摘要資訊 (**第** 一個、 **摘要**、 **aria-describedby**、 **aria labelledby**、 **aria 標籤**、 **標題**、 **標題** 屬性) 定義。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于將 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性設為 "presentation" 的 HTML 資料表標記，或是具有單一資料格 (1 ×1資料表) 的資料表。

此錯誤表示資料表標示為僅限配置 (有 `role="presentation"`) ，但它也包含協助工具資訊，就像是資料表一樣，這可能會對螢幕閱讀程式使用者造成混淆。

若要解決此錯誤，請判斷資料表是否真的只是版面配置表，如果是的話，請移除可存取的標記：

-   [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) 元素、 [**aria labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)、 [**aria 標籤**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)或 [**標題**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) 屬性。
-   [**摘要**](https://www.bing.com/search?q=**summary**) 或 [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性。
-   [**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) 標記。

## <a name="example"></a>範例

![資料表元素的 html，其屬性（例如摘要）會觸發 aria 展示表錯誤，並顯示為使用超時 html 標記 ](images/aria-layout-table.png)

## <a name="remarks"></a>備註

如果您判斷資料表確實需要協助工具資訊，請移除 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性，或將它設定為 [presentation] 以外的值。

 

 




