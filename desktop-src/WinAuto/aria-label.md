---
title: ARIA 標籤錯誤
description: ARIA 標籤錯誤
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1091c46dbb660c4c3568d24bfca34d94ef869f1e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104024262"
---
# <a name="aria-label-error"></a>ARIA 標籤錯誤

## <a name="text"></a>Text

元素的類型為 **輸入**、 **按鈕**、 **影像按鈕** 或 **地標** ，但沒有可存取的名稱。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于：

-   表單輸入欄位：
    -   HTML 標籤-**輸入 \[ 類型 = "文字 \| 密碼 \| 核取方塊 \| 選項按鈕檔案 \| \| 電子郵件 \| 電話 \| 色彩 \| 日期日期時間日期 \| 時間 \| -本地 \| 時間周間 \| \| \| 數位 \| 範圍 \| 搜尋 \| url \] "**、 **select**、 **datalist** 和 **textarea**。
    -   WAI-ARIA 角色—**核取方塊**、 **combobox**、 **listbox**、 **radiogroup**、**選項按鈕**、 **textbox**、**樹狀結構**、**滑杆** 和圓 **軸。**
-   影像/影像按鈕/按鈕
    -   HTML 標籤—**img**、**輸入 \[ 類型 = "影像 \| 按鈕" \]** 和 **按鈕**。
    -   WAI-ARIA 角色—**img** 和 **button**。
-   特徵點
    -   WAI-ARIA 角色—**區域**、 **橫幅**、 **互補**、 **contentinfo**、 **表單**、 **主要**、 **導覽** 和 **搜尋**。

> [!Note]  
> AccChecker 會顯示此錯誤，即使是根據內部 HTML 內容預設設定可存取名稱的專案 (請參閱上述範例中的 **橫幅** 元素) 。 在這些情況下，您可以隱藏此錯誤。

 

所有語義重要的 UI 專案（例如表單欄位） (例如， **輸入**、 **選取** **、文字** 區) 、影像、按鈕和地標 (標記（代表邏輯區域）) 都必須具有可存取的名稱，才能讓螢幕讀取器正確地將其宣告。

若要修正這個錯誤，請以下列其中一種方式來設定可存取的名稱 (以) 喜好設定順序列出。

-   表單欄位：使用 **標籤** 標記，並將 **for** 屬性設為目標欄位的 **識別碼** 值。
-   影像/影像按鈕：設定 **alt** 屬性。
-   按鈕：設定按鈕標題文字。
-   針對任何元素：
    -   [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性：設定為包含可存取名稱字串之元素的 **識別碼** 值。
    -   [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性：設定為可存取的名稱字串。
    -   [**標題**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) 屬性：設定為可存取的名稱字串 (也會建立 **工具提示**) 。

## <a name="example"></a>範例


```HTML
<!-- For landmark tags, set the accessible name by using the aria-labelledby 
attribute to reference the visible headers. -->
<h1 id="formHeader">Application Form</h1>
<form aria-labelledby="formHeader">

  <!-- For input fields, use the LABEL tag with the for attribute. -->
  <label for="fullName">Full Name</label>
  <input id="fullName" type="text" />

  <!-- If there is no visible text that can be referenced, set the accessible 
  name by using aria-label or title attributes. -->
  <input type="file" aria-label="Your photo"/>

  <!-- For images, use the alt attribute. -->
  <img src="…" alt="Uploaded photo" />

  <!-- For buttons, caption text is also used as the accessible name. -->
  <button onclick="processForm()">Send</button>

  <!-- For image buttons, use the alt attribute to define the accessible name. -->
  <input type="image" src="images/moreinfo.png" alt="Show more info"/>

  <!-- For elements with inner text this error can be suppressed because the 
  accessible name is set by default. -->
  <div role="banner">Accessible name set by default</div>
</form >
```



 

 




