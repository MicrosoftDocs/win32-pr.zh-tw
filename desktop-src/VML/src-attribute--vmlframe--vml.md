---
title: 'Src 屬性 (VMLFrame)  (VML) '
description: 'Src 屬性 (VMLFrame)  (VML) '
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315493"
---
# <a name="src-attribute-vmlframevml"></a><span data-ttu-id="6cd48-103">Src 屬性 (VMLFrame)  (VML) </span><span class="sxs-lookup"><span data-stu-id="6cd48-103">Src Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="6cd48-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="6cd48-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6cd48-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="6cd48-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6cd48-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="6cd48-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6cd48-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="6cd48-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6cd48-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="6cd48-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6cd48-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="6cd48-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6cd48-110">定義框架的資料來源。</span><span class="sxs-lookup"><span data-stu-id="6cd48-110">Defines the source of data for the frame.</span></span> <span data-ttu-id="6cd48-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6cd48-111">Read/write.</span></span> <span data-ttu-id="6cd48-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="6cd48-112">**String**.</span></span>

<span data-ttu-id="6cd48-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="6cd48-113">**Applies To**</span></span>

[<span data-ttu-id="6cd48-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="6cd48-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="6cd48-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="6cd48-115">**Tag Syntax**</span></span>

<span data-ttu-id="6cd48-116"><v： *element* src = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="6cd48-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="6cd48-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="6cd48-117">**Script Syntax**</span></span>

<span data-ttu-id="6cd48-118"> src = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="6cd48-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="6cd48-119">*運算式* =*元素* src</span><span class="sxs-lookup"><span data-stu-id="6cd48-119">*expression*=*element*.src</span></span>

<span data-ttu-id="6cd48-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="6cd48-120">**Remarks**</span></span>

<span data-ttu-id="6cd48-121">**Src** 屬性可能包含下列語法：</span><span class="sxs-lookup"><span data-stu-id="6cd48-121">The **Src** attribute can involve the following syntaxes:</span></span>

-   <span data-ttu-id="6cd48-122">外部檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="6cd48-122">URL to external file.</span></span> <span data-ttu-id="6cd48-123">檔案必須是具有下列格式的 XML 檔案：</span><span class="sxs-lookup"><span data-stu-id="6cd48-123">The file must be an XML file with the following format:</span></span>
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   <span data-ttu-id="6cd48-124">在檔案中，您必須有一個或多個具有有效識別碼的 VML 圖形，而且可以使用此語法來參考：</span><span class="sxs-lookup"><span data-stu-id="6cd48-124">Inside the file you must have one or more VML shapes with valid IDs that can be referenced by using this syntax:</span></span>
    ```HTML
       filename#shapename
    ```

    

-   <span data-ttu-id="6cd48-125">在下列參考中，外部檔案的副檔名為 vml，但可以使用任何擴充功能：</span><span class="sxs-lookup"><span data-stu-id="6cd48-125">In the following reference, external files have the .vml extension, but any extension can be used:</span></span>
    ```HTML
       external.vml#image01
    ```

    

-   <span data-ttu-id="6cd48-126">您可以使用下列語法，在相同檔案中參考圖形：</span><span class="sxs-lookup"><span data-stu-id="6cd48-126">You can reference a shape within the same file by using the following syntax:</span></span>
    ```HTML
       #shapename
    ```

    

<span data-ttu-id="6cd48-127">如果 **剪輯** 為 **False**，圖形將會縮放以符合框架。</span><span class="sxs-lookup"><span data-stu-id="6cd48-127">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="6cd48-128">若 **為 True**，將不會顯示框架外之圖形的任何部分。</span><span class="sxs-lookup"><span data-stu-id="6cd48-128">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="6cd48-129">請注意，除非 **剪輯** 為 **True**，否則不會使用 [原始](origin-attribute--vmlframe--vml.md)和 [大小](size-attribute--vmlframe.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd48-129">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="6cd48-130">**VML 標準屬性**</span><span class="sxs-lookup"><span data-stu-id="6cd48-130">**VML Standard Attribute**</span></span>

<span data-ttu-id="6cd48-131">**範例**</span><span class="sxs-lookup"><span data-stu-id="6cd48-131">**Example**</span></span>

<span data-ttu-id="6cd48-132">外部檔案中定義的映射將會被裁剪。</span><span class="sxs-lookup"><span data-stu-id="6cd48-132">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 