---
title: ARIA 方格結構錯誤
description: ARIA 方格結構錯誤
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684181"
---
# <a name="aria-grid-structure-error"></a>ARIA 方格結構錯誤

## <a name="text"></a>Text

具有 **方格** 角色的元素沒有對應的方格結構或可存取的標記。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于 **role** 屬性設為 "grid" 的自訂元素。 它並不適用于具有「方格」隱含 **角色** 的 HTML 資料表標記。

將其 **role** 屬性設定為 "grid" 的元素，必須具有由 Web 協助工具輔助的豐富網際網路應用程式所定義的結構 (WAI-ARIA) 方格角色，包括方格的可存取名稱和其標頭子項目。

若要修正這個錯誤，請檢查您的執行方式，以確定它符合 WAI-ARIA 規格。 具體而言，請確定結構符合下列規則。

-   **方格** 包含資料列 **或資料****列** 群組元素。
-   資料列 **群組包含資料****列** 元素。
-   **row** 元素包含 **columnheader** 或 **gridcell** 或 **rowheader** 元素。

您應使用下列其中一個屬性，為 **grid**、 **columnheader**、 **gridcell** 和 **rowheader** 元素定義可存取的名稱。

-   [**labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，用於參考包含文字的元素。
-   [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，可直接設定可存取的名稱。
-   用來建立工具提示的 [**標題**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title)，該工具提示同時作為名稱使用。

 

 




