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
# <a name="aria-label-error"></a><span data-ttu-id="120cf-104">ARIA 標籤錯誤</span><span class="sxs-lookup"><span data-stu-id="120cf-104">ARIA Label Error</span></span>

## <a name="text"></a><span data-ttu-id="120cf-105">Text</span><span class="sxs-lookup"><span data-stu-id="120cf-105">Text</span></span>

<span data-ttu-id="120cf-106">元素的類型為 **輸入**、 **按鈕**、 **影像按鈕** 或 **地標** ，但沒有可存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="120cf-106">Element is of type **input**, **button**, **image-button** or **landmark** but doesn't have an accessible name.</span></span>

## <a name="type"></a><span data-ttu-id="120cf-107">類型</span><span class="sxs-lookup"><span data-stu-id="120cf-107">Type</span></span>

<span data-ttu-id="120cf-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="120cf-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="120cf-109">描述</span><span class="sxs-lookup"><span data-stu-id="120cf-109">Description</span></span>

<span data-ttu-id="120cf-110">此錯誤適用于：</span><span class="sxs-lookup"><span data-stu-id="120cf-110">This error applies to:</span></span>

-   <span data-ttu-id="120cf-111">表單輸入欄位：</span><span class="sxs-lookup"><span data-stu-id="120cf-111">Form input fields:</span></span>
    -   <span data-ttu-id="120cf-112">HTML 標籤-**輸入 \[ 類型 = "文字 \| 密碼 \| 核取方塊 \| 選項按鈕檔案 \| \| 電子郵件 \| 電話 \| 色彩 \| 日期日期時間日期 \| 時間 \| -本地 \| 時間周間 \| \| \| 數位 \| 範圍 \| 搜尋 \| url \] "**、 **select**、 **datalist** 和 **textarea**。</span><span class="sxs-lookup"><span data-stu-id="120cf-112">HTML tags—**input\[type= "text\|password\|checkbox\|radio\|file\|email\|tel\|color\|date\|datetime\|datetime-local\|time\|week\|month\|number\|range\|search\|url"\]**, **select**, **datalist**, and **textarea**.</span></span>
    -   <span data-ttu-id="120cf-113">WAI-ARIA 角色—**核取方塊**、 **combobox**、 **listbox**、 **radiogroup**、**選項按鈕**、 **textbox**、**樹狀結構**、**滑杆** 和圓 **軸。**</span><span class="sxs-lookup"><span data-stu-id="120cf-113">WAI-ARIA roles—**checkbox**, **combobox**, **listbox**, **radiogroup**, **radio**, **textbox**, **tree**, **slider**, and **spinbutton**.</span></span>
-   <span data-ttu-id="120cf-114">影像/影像按鈕/按鈕</span><span class="sxs-lookup"><span data-stu-id="120cf-114">Images/image buttons/ buttons</span></span>
    -   <span data-ttu-id="120cf-115">HTML 標籤—**img**、**輸入 \[ 類型 = "影像 \| 按鈕" \]** 和 **按鈕**。</span><span class="sxs-lookup"><span data-stu-id="120cf-115">HTML tags—**img**, **input\[type="image\|button"\]**, and **button**.</span></span>
    -   <span data-ttu-id="120cf-116">WAI-ARIA 角色—**img** 和 **button**。</span><span class="sxs-lookup"><span data-stu-id="120cf-116">WAI-ARIA roles—**img** and **button**.</span></span>
-   <span data-ttu-id="120cf-117">特徵點</span><span class="sxs-lookup"><span data-stu-id="120cf-117">Landmarks</span></span>
    -   <span data-ttu-id="120cf-118">WAI-ARIA 角色—**區域**、 **橫幅**、 **互補**、 **contentinfo**、 **表單**、 **主要**、 **導覽** 和 **搜尋**。</span><span class="sxs-lookup"><span data-stu-id="120cf-118">WAI-ARIA roles—**region**, **banner**, **complementary**, **contentinfo**, **form**, **main**, **navigation**, and **search**.</span></span>

> [!Note]  
> <span data-ttu-id="120cf-119">AccChecker 會顯示此錯誤，即使是根據內部 HTML 內容預設設定可存取名稱的專案 (請參閱上述範例中的 **橫幅** 元素) 。</span><span class="sxs-lookup"><span data-stu-id="120cf-119">AccChecker shows this error even for elements for which the accessible name is set by default based on inner HTML content (see the **banner** element in the above example).</span></span> <span data-ttu-id="120cf-120">在這些情況下，您可以隱藏此錯誤。</span><span class="sxs-lookup"><span data-stu-id="120cf-120">For these cases, you can suppress this errors.</span></span>

 

<span data-ttu-id="120cf-121">所有語義重要的 UI 專案（例如表單欄位） (例如， **輸入**、 **選取** **、文字** 區) 、影像、按鈕和地標 (標記（代表邏輯區域）) 都必須具有可存取的名稱，才能讓螢幕讀取器正確地將其宣告。</span><span class="sxs-lookup"><span data-stu-id="120cf-121">All semantically important UI elements such as form fields (for example, **input**, **select**, **textarea**), images, buttons and landmarks (tags representing logical regions) must have the accessible name to allow screen readers to correctly announce them.</span></span>

<span data-ttu-id="120cf-122">若要修正這個錯誤，請以下列其中一種方式來設定可存取的名稱 (以) 喜好設定順序列出。</span><span class="sxs-lookup"><span data-stu-id="120cf-122">To fix this error, set the accessible name in one of the following ways (listed in the order of preference).</span></span>

-   <span data-ttu-id="120cf-123">表單欄位：使用 **標籤** 標記，並將 **for** 屬性設為目標欄位的 **識別碼** 值。</span><span class="sxs-lookup"><span data-stu-id="120cf-123">Form fields: Use the **label** tag and set the **for** attribute to the **id** value of the target field.</span></span>
-   <span data-ttu-id="120cf-124">影像/影像按鈕：設定 **alt** 屬性。</span><span class="sxs-lookup"><span data-stu-id="120cf-124">Image/image button: Set the **alt** attribute.</span></span>
-   <span data-ttu-id="120cf-125">按鈕：設定按鈕標題文字。</span><span class="sxs-lookup"><span data-stu-id="120cf-125">Buttons: Set the button caption text.</span></span>
-   <span data-ttu-id="120cf-126">針對任何元素：</span><span class="sxs-lookup"><span data-stu-id="120cf-126">For any element:</span></span>
    -   <span data-ttu-id="120cf-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性：設定為包含可存取名稱字串之元素的 **識別碼** 值。</span><span class="sxs-lookup"><span data-stu-id="120cf-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the **id** value of the element containing the accessible name string.</span></span>
    -   <span data-ttu-id="120cf-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性：設定為可存取的名稱字串。</span><span class="sxs-lookup"><span data-stu-id="120cf-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the accessible name string.</span></span>
    -   <span data-ttu-id="120cf-129">[**標題**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) 屬性：設定為可存取的名稱字串 (也會建立 **工具提示**) 。</span><span class="sxs-lookup"><span data-stu-id="120cf-129">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attribute: Set to the accessible name string (also create a **tooltip**).</span></span>

## <a name="example"></a><span data-ttu-id="120cf-130">範例</span><span class="sxs-lookup"><span data-stu-id="120cf-130">Example</span></span>


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



 

 




