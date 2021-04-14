---
description: 這些元素組成 Web 發行和線上列印訂購嚮導的傳送資訊清單中所使用的 XML 架構。
title: 傳送資訊清單架構
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991694"
---
# <a name="transfer-manifest-schema"></a><span data-ttu-id="c97d3-103">傳送資訊清單架構</span><span class="sxs-lookup"><span data-stu-id="c97d3-103">Transfer Manifest Schema</span></span>

<span data-ttu-id="c97d3-104">這些元素組成 Web 發行和線上列印訂購嚮導的傳送資訊清單中所使用的 XML 架構。</span><span class="sxs-lookup"><span data-stu-id="c97d3-104">These elements make up the XML schema used in the Web Publishing and Online Print Ordering wizards' transfer manifest.</span></span>

<span data-ttu-id="c97d3-105">下列是針對傳送資訊清單所定義的元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-105">The following elements are defined for the transfer manifest.</span></span>

-   [<span data-ttu-id="c97d3-106">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="c97d3-106">cancelledpage</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-107">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-107">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-108">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-110">failurepage</span><span class="sxs-lookup"><span data-stu-id="c97d3-110">failurepage</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-111">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-111">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-112">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-114">喜歡</span><span class="sxs-lookup"><span data-stu-id="c97d3-114">favorite</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-115">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-115">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-116">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-116">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-117">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-118">file</span><span class="sxs-lookup"><span data-stu-id="c97d3-118">file</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-119">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-119">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-120">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-120">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-121">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-121">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-122">filelist</span><span class="sxs-lookup"><span data-stu-id="c97d3-122">filelist</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-123">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-123">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-124">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-124">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-125">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-125">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-126">資料夾</span><span class="sxs-lookup"><span data-stu-id="c97d3-126">folder</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-127">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-127">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-128">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-128">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-129">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-129">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-130">folderlist</span><span class="sxs-lookup"><span data-stu-id="c97d3-130">folderlist</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-131">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-131">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-132">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-132">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-133">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-133">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-134">formdata</span><span class="sxs-lookup"><span data-stu-id="c97d3-134">formdata</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-135">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-135">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-136">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-136">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-137">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-137">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-138">htmlui</span><span class="sxs-lookup"><span data-stu-id="c97d3-138">htmlui</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-139">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-139">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-140">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-140">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-141">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-141">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-142">imageproperty</span><span class="sxs-lookup"><span data-stu-id="c97d3-142">imageproperty</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-143">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-143">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-144">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-144">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-145">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-145">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-146">元</span><span class="sxs-lookup"><span data-stu-id="c97d3-146">metadata</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-147">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-147">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-148">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-148">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-149">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-149">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-150">netplace</span><span class="sxs-lookup"><span data-stu-id="c97d3-150">netplace</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-151">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-151">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-152">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-152">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-153">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-153">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-154">發佈</span><span class="sxs-lookup"><span data-stu-id="c97d3-154">post</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-155">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-155">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-156">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-156">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-157">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-157">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-158">調整</span><span class="sxs-lookup"><span data-stu-id="c97d3-158">resize</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-159">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-159">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-160">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-160">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-161">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-161">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-162">successpage</span><span class="sxs-lookup"><span data-stu-id="c97d3-162">successpage</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-163">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-163">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-164">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-164">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-165">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-165">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-166">目標</span><span class="sxs-lookup"><span data-stu-id="c97d3-166">target</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-167">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-167">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-168">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-168">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-169">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-169">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-170">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="c97d3-170">transfermanifest</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-171">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-171">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-172">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-172">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-173">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-173">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c97d3-174">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-174">uploadinfo</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-175">語法</span><span class="sxs-lookup"><span data-stu-id="c97d3-175">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="c97d3-176">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-176">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="c97d3-177">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-177">Element Information</span></span>](#element-information)

## <a name="cancelledpage"></a><span data-ttu-id="c97d3-178">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="c97d3-178">cancelledpage</span></span>

<span data-ttu-id="c97d3-179">指定當使用者按一下 [ **取消** ] 按鈕時，在關閉嚮導之前顯示的伺服器端 HTML 網頁。</span><span class="sxs-lookup"><span data-stu-id="c97d3-179">Specifies the server-side HTML page to display before the wizard is closed when the user clicks the **Cancel** button.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-180">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-180">Syntax</span></span>


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-181">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-181">Attributes</span></span>



| <span data-ttu-id="c97d3-182">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-182">Attribute</span></span> | <span data-ttu-id="c97d3-183">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-183">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-184">href</span><span class="sxs-lookup"><span data-stu-id="c97d3-184">href</span></span>      | <span data-ttu-id="c97d3-185">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-185">Required.</span></span> <span data-ttu-id="c97d3-186">當使用者按一下 [ **取消** ] 按鈕時要顯示之伺服器端 HTML 頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-186">The URL of the server-side HTML page to display when the user clicks the **Cancel** button.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-187">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-187">Element Information</span></span>



| <span data-ttu-id="c97d3-188">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-188">Parent Element</span></span>        | <span data-ttu-id="c97d3-189">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-189">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="c97d3-190">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-190">uploadinfo</span></span>](#syntax) | <span data-ttu-id="c97d3-191">無</span><span class="sxs-lookup"><span data-stu-id="c97d3-191">None</span></span>           |



 

## <a name="failurepage"></a><span data-ttu-id="c97d3-192">failurepage</span><span class="sxs-lookup"><span data-stu-id="c97d3-192">failurepage</span></span>

<span data-ttu-id="c97d3-193">指定當上傳不成功時，要顯示的伺服器端 HTML 網頁。</span><span class="sxs-lookup"><span data-stu-id="c97d3-193">Specifies the server-side HTML page to display if the upload is not successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-194">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-194">Syntax</span></span>


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-195">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-195">Attributes</span></span>



| <span data-ttu-id="c97d3-196">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-196">Attribute</span></span> | <span data-ttu-id="c97d3-197">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-197">Description</span></span>                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-198">href</span><span class="sxs-lookup"><span data-stu-id="c97d3-198">href</span></span>      | <span data-ttu-id="c97d3-199">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-199">Required.</span></span> <span data-ttu-id="c97d3-200">當上傳不成功時，要顯示之伺服器端 HTML 頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-200">The URL of the server-side HTML page to display if the upload is not successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-201">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-201">Element Information</span></span>



| <span data-ttu-id="c97d3-202">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-202">Parent Element</span></span>        | <span data-ttu-id="c97d3-203">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-203">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="c97d3-204">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-204">uploadinfo</span></span>](#syntax) | <span data-ttu-id="c97d3-205">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-205">None.</span></span> <span data-ttu-id="c97d3-206">允許文字。</span><span class="sxs-lookup"><span data-stu-id="c97d3-206">Text is allowed.</span></span> |



 

## <a name="favorite"></a><span data-ttu-id="c97d3-207">我的最愛</span><span class="sxs-lookup"><span data-stu-id="c97d3-207">favorite</span></span>

<span data-ttu-id="c97d3-208">指示嚮導在指定 URL 的 [我的最愛 **] 功能表中** 建立最愛的網站專案。</span><span class="sxs-lookup"><span data-stu-id="c97d3-208">Instructs the wizard to create a favorite website entry in the **Favorites** menu for the given URL.</span></span> <span data-ttu-id="c97d3-209">如果未指定這個元素，則會在其位置使用 [htmlui](#syntax) 元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-209">If this element is not specified, then the [htmlui](#syntax) element is used in its place.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-210">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-210">Syntax</span></span>


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-211">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-211">Attributes</span></span>



| <span data-ttu-id="c97d3-212">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-212">Attribute</span></span> | <span data-ttu-id="c97d3-213">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-213">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-214">comment</span><span class="sxs-lookup"><span data-stu-id="c97d3-214">comment</span></span>   | <span data-ttu-id="c97d3-215">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-215">Required.</span></span> <span data-ttu-id="c97d3-216">與 [我的最愛 **]** 專案相關聯的批註。</span><span class="sxs-lookup"><span data-stu-id="c97d3-216">The comment associated with the **Favorites** entry.</span></span>         |
| <span data-ttu-id="c97d3-217">href</span><span class="sxs-lookup"><span data-stu-id="c97d3-217">href</span></span>      | <span data-ttu-id="c97d3-218">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-218">Required.</span></span> <span data-ttu-id="c97d3-219">[我的最愛 **]** 專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-219">The URL of the **Favorites** entry.</span></span>                          |
| <span data-ttu-id="c97d3-220">NAME</span><span class="sxs-lookup"><span data-stu-id="c97d3-220">name</span></span>      | <span data-ttu-id="c97d3-221">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-221">Required.</span></span> <span data-ttu-id="c97d3-222">出現在 [我的最愛 **]** 功能表中的 URL 名稱。</span><span class="sxs-lookup"><span data-stu-id="c97d3-222">The name for the URL that appears in the **Favorites** menu.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-223">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-223">Element Information</span></span>



| <span data-ttu-id="c97d3-224">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-224">Parent Element</span></span>        | <span data-ttu-id="c97d3-225">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-225">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="c97d3-226">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-226">uploadinfo</span></span>](#syntax) | <span data-ttu-id="c97d3-227">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-227">None.</span></span> <span data-ttu-id="c97d3-228">允許文字。</span><span class="sxs-lookup"><span data-stu-id="c97d3-228">Text is allowed.</span></span> |



 

## <a name="file"></a><span data-ttu-id="c97d3-229">file</span><span class="sxs-lookup"><span data-stu-id="c97d3-229">file</span></span>

<span data-ttu-id="c97d3-230">描述要複製的單一檔案。</span><span class="sxs-lookup"><span data-stu-id="c97d3-230">Describes a single file to be copied.</span></span> <span data-ttu-id="c97d3-231">單一[filelist](#syntax)節點底下可能[包含多個](#syntax)檔案元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-231">Multiple [file](#syntax) elements may be contained under a single [filelist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-232">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-232">Syntax</span></span>


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-233">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-233">Attributes</span></span>



| <span data-ttu-id="c97d3-234">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-234">Attribute</span></span>   | <span data-ttu-id="c97d3-235">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-235">Description</span></span>                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-236">contenttype</span><span class="sxs-lookup"><span data-stu-id="c97d3-236">contenttype</span></span> | <span data-ttu-id="c97d3-237">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c97d3-237">Optional.</span></span> <span data-ttu-id="c97d3-238">檔案的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="c97d3-238">The MIME type of the file.</span></span>                                                                                                                                         |
| <span data-ttu-id="c97d3-239">目的地</span><span class="sxs-lookup"><span data-stu-id="c97d3-239">destination</span></span> | <span data-ttu-id="c97d3-240">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-240">Required.</span></span> <span data-ttu-id="c97d3-241">檔案上傳之後的建議路徑。</span><span class="sxs-lookup"><span data-stu-id="c97d3-241">A suggested path for the file once it is uploaded.</span></span> <span data-ttu-id="c97d3-242">此路徑相對於上傳網站的目的地 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-242">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="c97d3-243">上傳網站可以視需要修改此值。</span><span class="sxs-lookup"><span data-stu-id="c97d3-243">The upload site can modify this value as necessary.</span></span> |
| <span data-ttu-id="c97d3-244">擴充功能</span><span class="sxs-lookup"><span data-stu-id="c97d3-244">extension</span></span>   | <span data-ttu-id="c97d3-245">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c97d3-245">Optional.</span></span> <span data-ttu-id="c97d3-246">檔案名的副檔名。</span><span class="sxs-lookup"><span data-stu-id="c97d3-246">The file name extension of the file.</span></span>                                                                                                                               |
| <span data-ttu-id="c97d3-247">id</span><span class="sxs-lookup"><span data-stu-id="c97d3-247">id</span></span>          | <span data-ttu-id="c97d3-248">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-248">Required.</span></span> <span data-ttu-id="c97d3-249">檔案的數值索引。</span><span class="sxs-lookup"><span data-stu-id="c97d3-249">The numerical index of the file.</span></span>                                                                                                                                   |
| <span data-ttu-id="c97d3-250">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="c97d3-250">size</span></span>        | <span data-ttu-id="c97d3-251">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c97d3-251">Optional.</span></span> <span data-ttu-id="c97d3-252">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c97d3-252">The size of the file, in bytes.</span></span>                                                                                                                                    |
| <span data-ttu-id="c97d3-253">source</span><span class="sxs-lookup"><span data-stu-id="c97d3-253">source</span></span>      | <span data-ttu-id="c97d3-254">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-254">Required.</span></span> <span data-ttu-id="c97d3-255">檔案的完整檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="c97d3-255">The full file system path for the file.</span></span>                                                                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-256">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-256">Element Information</span></span>



| <span data-ttu-id="c97d3-257">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-257">Parent Element</span></span>      | <span data-ttu-id="c97d3-258">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-258">Child Elements</span></span>                                          |
|---------------------|---------------------------------------------------------|
| [<span data-ttu-id="c97d3-259">filelist</span><span class="sxs-lookup"><span data-stu-id="c97d3-259">filelist</span></span>](#syntax) | <span data-ttu-id="c97d3-260">[中繼資料](#syntax)、 [貼](#syntax)文、重 [設大小](#syntax)</span><span class="sxs-lookup"><span data-stu-id="c97d3-260">[metadata](#syntax), [post](#syntax), [resize](#syntax)</span></span> |



 

## <a name="filelist"></a><span data-ttu-id="c97d3-261">filelist</span><span class="sxs-lookup"><span data-stu-id="c97d3-261">filelist</span></span>

<span data-ttu-id="c97d3-262">描述要複製之檔案的元素容器。</span><span class="sxs-lookup"><span data-stu-id="c97d3-262">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="c97d3-263">單一[transfermanifest](#syntax)節點底下可能包含多個[filelist](#syntax)元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-263">Multiple [filelist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-264">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-264">Syntax</span></span>


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-265">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-265">Attributes</span></span>



| <span data-ttu-id="c97d3-266">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-266">Attribute</span></span>   | <span data-ttu-id="c97d3-267">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-267">Description</span></span>      |
|-------------|------------------|
| <span data-ttu-id="c97d3-268">usesfolders</span><span class="sxs-lookup"><span data-stu-id="c97d3-268">usesfolders</span></span> | <span data-ttu-id="c97d3-269">未實作。</span><span class="sxs-lookup"><span data-stu-id="c97d3-269">Not implemented.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-270">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-270">Element Information</span></span>



| <span data-ttu-id="c97d3-271">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-271">Parent Element</span></span>              | <span data-ttu-id="c97d3-272">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-272">Child Elements</span></span>  |
|-----------------------------|-----------------|
| [<span data-ttu-id="c97d3-273">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="c97d3-273">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="c97d3-274">file</span><span class="sxs-lookup"><span data-stu-id="c97d3-274">file</span></span>](#syntax) |



 

## <a name="folder"></a><span data-ttu-id="c97d3-275">folder</span><span class="sxs-lookup"><span data-stu-id="c97d3-275">folder</span></span>

<span data-ttu-id="c97d3-276">描述儲存檔案的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c97d3-276">Describes a folder in which files are stored.</span></span> <span data-ttu-id="c97d3-277">單一[folderlist](#syntax)節點底下可能包含多個[資料夾](#syntax)元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-277">Multiple [folder](#syntax) elements may be contained under a single [folderlist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-278">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-278">Syntax</span></span>


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-279">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-279">Attributes</span></span>



| <span data-ttu-id="c97d3-280">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-280">Attribute</span></span>   | <span data-ttu-id="c97d3-281">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-281">Description</span></span>                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-282">目的地</span><span class="sxs-lookup"><span data-stu-id="c97d3-282">destination</span></span> | <span data-ttu-id="c97d3-283">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-283">Required.</span></span> <span data-ttu-id="c97d3-284">資料夾上傳之後的建議路徑。</span><span class="sxs-lookup"><span data-stu-id="c97d3-284">A suggested path for the folder once it is uploaded.</span></span> <span data-ttu-id="c97d3-285">此路徑相對於上傳網站的目的地 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-285">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="c97d3-286">上傳網站可以視需要修改此值。</span><span class="sxs-lookup"><span data-stu-id="c97d3-286">The upload site can modify this value as necessary.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-287">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-287">Element Information</span></span>



| <span data-ttu-id="c97d3-288">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-288">Parent Element</span></span>        | <span data-ttu-id="c97d3-289">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-289">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="c97d3-290">folderlist</span><span class="sxs-lookup"><span data-stu-id="c97d3-290">folderlist</span></span>](#syntax) | <span data-ttu-id="c97d3-291">無</span><span class="sxs-lookup"><span data-stu-id="c97d3-291">None</span></span>           |



 

## <a name="folderlist"></a><span data-ttu-id="c97d3-292">folderlist</span><span class="sxs-lookup"><span data-stu-id="c97d3-292">folderlist</span></span>

<span data-ttu-id="c97d3-293">描述要複製之檔案的元素容器。</span><span class="sxs-lookup"><span data-stu-id="c97d3-293">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="c97d3-294">單一[transfermanifest](#syntax)節點底下可能包含多個[folderlist](#syntax)元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-294">Multiple [folderlist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-295">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-295">Syntax</span></span>


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-296">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-296">Attributes</span></span>

<span data-ttu-id="c97d3-297">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-297">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="c97d3-298">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-298">Element Information</span></span>



| <span data-ttu-id="c97d3-299">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-299">Parent Element</span></span>              | <span data-ttu-id="c97d3-300">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-300">Child Elements</span></span>    |
|-----------------------------|-------------------|
| [<span data-ttu-id="c97d3-301">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="c97d3-301">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="c97d3-302">資料夾</span><span class="sxs-lookup"><span data-stu-id="c97d3-302">folder</span></span>](#syntax) |



 

## <a name="formdata"></a><span data-ttu-id="c97d3-303">formdata</span><span class="sxs-lookup"><span data-stu-id="c97d3-303">formdata</span></span>

<span data-ttu-id="c97d3-304">描述可隨檔案傳送的選擇性 HTML 編碼表單資料。</span><span class="sxs-lookup"><span data-stu-id="c97d3-304">Describes optional HTML encoded form data that may be transferred with the files.</span></span> <span data-ttu-id="c97d3-305">如果它想要將檔案上傳為多部分的貼文，則服務會新增這個元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-305">This element is added by the service if it elects to upload the files as a multi-part post.</span></span> <span data-ttu-id="c97d3-306">表單資料會連同 [post](#syntax) 元素中的資訊，用來建立貼文標頭。</span><span class="sxs-lookup"><span data-stu-id="c97d3-306">The form data, together with information from the [post](#syntax) element, is used to create the post header.</span></span>

<span data-ttu-id="c97d3-307">單一[uploadinfo](#syntax)節點底下可能包含多個[formdata](#syntax)元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-307">Multiple [formdata](#syntax) elements may be contained under a single [uploadinfo](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-308">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-308">Syntax</span></span>


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-309">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-309">Attributes</span></span>



| <span data-ttu-id="c97d3-310">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-310">Attribute</span></span> | <span data-ttu-id="c97d3-311">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-311">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-312">NAME</span><span class="sxs-lookup"><span data-stu-id="c97d3-312">name</span></span>      | <span data-ttu-id="c97d3-313">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-313">Required.</span></span> <span data-ttu-id="c97d3-314">定義與上傳區段相關聯的表單資料名稱。</span><span class="sxs-lookup"><span data-stu-id="c97d3-314">Defines the form data name associated with this section of the upload.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-315">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-315">Element Information</span></span>



| <span data-ttu-id="c97d3-316">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-316">Parent Element</span></span>        | <span data-ttu-id="c97d3-317">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-317">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="c97d3-318">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-318">uploadinfo</span></span>](#syntax) | <span data-ttu-id="c97d3-319">無</span><span class="sxs-lookup"><span data-stu-id="c97d3-319">None</span></span>           |



 

## <a name="htmlui"></a><span data-ttu-id="c97d3-320">htmlui</span><span class="sxs-lookup"><span data-stu-id="c97d3-320">htmlui</span></span>

<span data-ttu-id="c97d3-321">當嚮導關閉時要顯示之伺服器端 HTML 頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-321">The URL of the server-side HTML page to display when the wizard is closed.</span></span> <span data-ttu-id="c97d3-322">如果 [我的 [最愛](#syntax)] 專案不存在，且已指定上傳網站的易記名稱，此專案會在 [我的最愛 **]** 功能表中建立最愛的網頁</span><span class="sxs-lookup"><span data-stu-id="c97d3-322">This element creates a favorite webpage entry in the **Favorites** menu if the [favorite](#syntax) element is absent and the upload site's friendly name is specified.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-323">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-323">Syntax</span></span>


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-324">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-324">Attributes</span></span>



| <span data-ttu-id="c97d3-325">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-325">Attribute</span></span> | <span data-ttu-id="c97d3-326">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-326">Description</span></span>                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-327">href</span><span class="sxs-lookup"><span data-stu-id="c97d3-327">href</span></span>      | <span data-ttu-id="c97d3-328">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-328">Required.</span></span> <span data-ttu-id="c97d3-329">當嚮導關閉時要顯示之伺服器端 HTML 頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-329">The URL of the server-side HTML page to display when the wizard is closed.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-330">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-330">Element Information</span></span>



| <span data-ttu-id="c97d3-331">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-331">Parent Element</span></span>        | <span data-ttu-id="c97d3-332">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-332">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="c97d3-333">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-333">uploadinfo</span></span>](#syntax) | <span data-ttu-id="c97d3-334">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-334">None.</span></span> <span data-ttu-id="c97d3-335">允許文字。</span><span class="sxs-lookup"><span data-stu-id="c97d3-335">Text is allowed.</span></span> |



 

## <a name="imageproperty"></a><span data-ttu-id="c97d3-336">imageproperty</span><span class="sxs-lookup"><span data-stu-id="c97d3-336">imageproperty</span></span>

<span data-ttu-id="c97d3-337">指定與檔案相關的影像屬性。</span><span class="sxs-lookup"><span data-stu-id="c97d3-337">Specifies an image property relating to the file.</span></span> <span data-ttu-id="c97d3-338">單一[中繼資料](#syntax)節點下可包含多個[imageproperty](#syntax)元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-338">Multiple [imageproperty](#syntax) elements may be contained under a single [metadata](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-339">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-339">Syntax</span></span>


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-340">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-340">Attributes</span></span>



| <span data-ttu-id="c97d3-341">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-341">Attribute</span></span> | <span data-ttu-id="c97d3-342">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-342">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="c97d3-343">id</span><span class="sxs-lookup"><span data-stu-id="c97d3-343">id</span></span>        | <span data-ttu-id="c97d3-344">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-344">Required.</span></span> <span data-ttu-id="c97d3-345">特定屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c97d3-345">The ID of the particular property.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-346">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-346">Element Information</span></span>



| <span data-ttu-id="c97d3-347">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-347">Parent Element</span></span>      | <span data-ttu-id="c97d3-348">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-348">Child Elements</span></span>         |
|---------------------|------------------------|
| [<span data-ttu-id="c97d3-349">元</span><span class="sxs-lookup"><span data-stu-id="c97d3-349">metadata</span></span>](#syntax) | <span data-ttu-id="c97d3-350">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-350">None.</span></span> <span data-ttu-id="c97d3-351">允許文字。</span><span class="sxs-lookup"><span data-stu-id="c97d3-351">Text is allowed.</span></span> |



 

## <a name="metadata"></a><span data-ttu-id="c97d3-352">中繼資料</span><span class="sxs-lookup"><span data-stu-id="c97d3-352">metadata</span></span>

<span data-ttu-id="c97d3-353">元素和文字的容器，用於定義特定檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c97d3-353">A container for elements and text defining metadata for the particular file.</span></span> <span data-ttu-id="c97d3-354">[單一檔案](#syntax)節點底下可能包含多個[中繼資料](#syntax)元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-354">Multiple [metadata](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-355">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-355">Syntax</span></span>


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-356">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-356">Attributes</span></span>

<span data-ttu-id="c97d3-357">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-357">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="c97d3-358">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-358">Element Information</span></span>



| <span data-ttu-id="c97d3-359">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-359">Parent Element</span></span>  | <span data-ttu-id="c97d3-360">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-360">Child Elements</span></span>           |
|-----------------|--------------------------|
| [<span data-ttu-id="c97d3-361">file</span><span class="sxs-lookup"><span data-stu-id="c97d3-361">file</span></span>](#syntax) | [<span data-ttu-id="c97d3-362">imageproperty</span><span class="sxs-lookup"><span data-stu-id="c97d3-362">imageproperty</span></span>](#syntax) |



 

## <a name="netplace"></a><span data-ttu-id="c97d3-363">netplace</span><span class="sxs-lookup"><span data-stu-id="c97d3-363">netplace</span></span>

<span data-ttu-id="c97d3-364">定義當上傳完成時，在 **我的網路位置** 中建立之網路位置的目標。</span><span class="sxs-lookup"><span data-stu-id="c97d3-364">Defines the target for a network place that is created in **My Network Places** when the upload is complete.</span></span> <span data-ttu-id="c97d3-365">您可以透過 [**IPublishingWizard：： Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) 方法來防止建立網路位置。</span><span class="sxs-lookup"><span data-stu-id="c97d3-365">Creation of a network place can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-366">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-366">Syntax</span></span>


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-367">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-367">Attributes</span></span>



| <span data-ttu-id="c97d3-368">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-368">Attribute</span></span> | <span data-ttu-id="c97d3-369">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-369">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-370">comment</span><span class="sxs-lookup"><span data-stu-id="c97d3-370">comment</span></span>   | <span data-ttu-id="c97d3-371">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-371">Required.</span></span> <span data-ttu-id="c97d3-372">當游標停留在網路位置圖示上時，所顯示的批註。</span><span class="sxs-lookup"><span data-stu-id="c97d3-372">The comment displayed for the network place icon when the cursor rests on it.</span></span>         |
| <span data-ttu-id="c97d3-373">href</span><span class="sxs-lookup"><span data-stu-id="c97d3-373">href</span></span>      | <span data-ttu-id="c97d3-374">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-374">Required.</span></span> <span data-ttu-id="c97d3-375">網路位置專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-375">The URL of the network place entry.</span></span>                                                   |
| <span data-ttu-id="c97d3-376">NAME</span><span class="sxs-lookup"><span data-stu-id="c97d3-376">name</span></span>      | <span data-ttu-id="c97d3-377">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-377">Required.</span></span> <span data-ttu-id="c97d3-378">出現在 [ **我的網路位置** ] 資料夾中的網路位置圖示名稱。</span><span class="sxs-lookup"><span data-stu-id="c97d3-378">The name for the network place icon that appears in the **My Network Places** folder.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-379">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-379">Element Information</span></span>



| <span data-ttu-id="c97d3-380">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-380">Parent Element</span></span>        | <span data-ttu-id="c97d3-381">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-381">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="c97d3-382">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-382">uploadinfo</span></span>](#syntax) | <span data-ttu-id="c97d3-383">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-383">None.</span></span> <span data-ttu-id="c97d3-384">允許文字。</span><span class="sxs-lookup"><span data-stu-id="c97d3-384">Text is allowed.</span></span> |



 

## <a name="post"></a><span data-ttu-id="c97d3-385">post</span><span class="sxs-lookup"><span data-stu-id="c97d3-385">post</span></span>

<span data-ttu-id="c97d3-386">應張貼檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-386">URL to which the file should be posted.</span></span> <span data-ttu-id="c97d3-387">此專案是由服務在以多部分的 post 完成傳送時加入，且使用 [formdata](#syntax)來建立貼文標頭。</span><span class="sxs-lookup"><span data-stu-id="c97d3-387">This element is added by the service when the transfer is done as a multi-part post and, with [formdata](#syntax), is used to build the post header.</span></span> <span data-ttu-id="c97d3-388">如果服務選擇使用 World Wide Web 分散式撰寫和版本設定來執行檔案傳輸 (WebDAV) ，它就不應該加入這個元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-388">If the service chooses to perform the file transfer using World Wide Web Distributed Authoring and Versioning (WebDAV), it should not add this element.</span></span> <span data-ttu-id="c97d3-389">[單一檔案](#syntax)節點底下可能包含多個[post](#syntax)元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-389">Multiple [post](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-390">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-390">Syntax</span></span>


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-391">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-391">Attributes</span></span>



| <span data-ttu-id="c97d3-392">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-392">Attribute</span></span> | <span data-ttu-id="c97d3-393">說明</span><span class="sxs-lookup"><span data-stu-id="c97d3-393">Description</span></span>                                                                    |
|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-394">filename</span><span class="sxs-lookup"><span data-stu-id="c97d3-394">filename</span></span>  | <span data-ttu-id="c97d3-395">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c97d3-395">Optional.</span></span> <span data-ttu-id="c97d3-396">張貼之檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c97d3-396">The file name for the posted file.</span></span>                                   |
| <span data-ttu-id="c97d3-397">href</span><span class="sxs-lookup"><span data-stu-id="c97d3-397">href</span></span>      | <span data-ttu-id="c97d3-398">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-398">Required.</span></span> <span data-ttu-id="c97d3-399">目的資料夾的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-399">The URL of the destination folder.</span></span>                                   |
| <span data-ttu-id="c97d3-400">NAME</span><span class="sxs-lookup"><span data-stu-id="c97d3-400">name</span></span>      | <span data-ttu-id="c97d3-401">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-401">Required.</span></span> <span data-ttu-id="c97d3-402">定義與此貼文的這個區段相關聯的表單資料名稱。</span><span class="sxs-lookup"><span data-stu-id="c97d3-402">Defines the form data name associated with this section of the post.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-403">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-403">Element Information</span></span>



| <span data-ttu-id="c97d3-404">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-404">Parent Element</span></span>  | <span data-ttu-id="c97d3-405">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-405">Child Elements</span></span>      |
|-----------------|---------------------|
| [<span data-ttu-id="c97d3-406">file</span><span class="sxs-lookup"><span data-stu-id="c97d3-406">file</span></span>](#syntax) | [<span data-ttu-id="c97d3-407">formdata</span><span class="sxs-lookup"><span data-stu-id="c97d3-407">formdata</span></span>](#syntax) |



 

## <a name="resize"></a><span data-ttu-id="c97d3-408">調整大小</span><span class="sxs-lookup"><span data-stu-id="c97d3-408">resize</span></span>

<span data-ttu-id="c97d3-409">以 JPEG 格式定義影像檔的縮放和 recompression。</span><span class="sxs-lookup"><span data-stu-id="c97d3-409">Defines the scaling and recompression of an image file into JPEG format.</span></span> <span data-ttu-id="c97d3-410">如果來源檔案已為 JPEG 格式，且小於或等於指定的寬度和高度，則不會調整大小。</span><span class="sxs-lookup"><span data-stu-id="c97d3-410">If the source file is already in JPEG format and is less than or equal to the specified width and height, it is not sized.</span></span> <span data-ttu-id="c97d3-411">如果來源檔案不是 JPEG 檔案，則會進行轉換。</span><span class="sxs-lookup"><span data-stu-id="c97d3-411">If the source file is not a JPEG file, it is converted.</span></span> <span data-ttu-id="c97d3-412">您可以透過 [**IPublishingWizard：： Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) 方法防止調整、recompression 和轉換檔案。</span><span class="sxs-lookup"><span data-stu-id="c97d3-412">Scaling, recompression, and conversion of the file can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span> <span data-ttu-id="c97d3-413">[單一檔案](#syntax)節點底下可能包含多個重[設大小](#syntax)的元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-413">Multiple [resize](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-414">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-414">Syntax</span></span>


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-415">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-415">Attributes</span></span>



| <span data-ttu-id="c97d3-416">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-416">Attribute</span></span> | <span data-ttu-id="c97d3-417">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-417">Description</span></span>                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-418">殘雪</span><span class="sxs-lookup"><span data-stu-id="c97d3-418">cx</span></span>        | <span data-ttu-id="c97d3-419">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-419">Required.</span></span> <span data-ttu-id="c97d3-420">上傳之後影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c97d3-420">The width of the image, in pixels, after uploading.</span></span> <span data-ttu-id="c97d3-421">如果這個值為0，則會從 **cy** 值計算 **cx** 以保留相對維度。</span><span class="sxs-lookup"><span data-stu-id="c97d3-421">If this value is 0, then **cx** is calculated from the **cy** value to preserve relative dimensions.</span></span>  |
| <span data-ttu-id="c97d3-422">cy</span><span class="sxs-lookup"><span data-stu-id="c97d3-422">cy</span></span>        | <span data-ttu-id="c97d3-423">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-423">Required.</span></span> <span data-ttu-id="c97d3-424">上傳之後影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c97d3-424">The height of the image, in pixels, after uploading.</span></span> <span data-ttu-id="c97d3-425">如果這個值為0，則會從 **cx** 值計算 **cy** 以保留相對維度。</span><span class="sxs-lookup"><span data-stu-id="c97d3-425">If this value is 0, then **cy** is calculated from the **cx** value to preserve relative dimensions.</span></span> |
| <span data-ttu-id="c97d3-426">品質</span><span class="sxs-lookup"><span data-stu-id="c97d3-426">quality</span></span>   | <span data-ttu-id="c97d3-427">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-427">Required.</span></span> <span data-ttu-id="c97d3-428">JPEG 品質值（介於0和100之間），100為最高品質。</span><span class="sxs-lookup"><span data-stu-id="c97d3-428">The JPEG quality value, between 0 and 100, with 100 being the highest quality.</span></span>                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-429">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-429">Element Information</span></span>



| <span data-ttu-id="c97d3-430">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-430">Parent Element</span></span>  | <span data-ttu-id="c97d3-431">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-431">Child Elements</span></span> |
|-----------------|----------------|
| [<span data-ttu-id="c97d3-432">file</span><span class="sxs-lookup"><span data-stu-id="c97d3-432">file</span></span>](#syntax) | <span data-ttu-id="c97d3-433">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-433">None.</span></span>          |



 

## <a name="successpage"></a><span data-ttu-id="c97d3-434">successpage</span><span class="sxs-lookup"><span data-stu-id="c97d3-434">successpage</span></span>

<span data-ttu-id="c97d3-435">指定當上傳成功時，要顯示的伺服器端 HTML 頁面。</span><span class="sxs-lookup"><span data-stu-id="c97d3-435">Specifies the server-side HTML page to display if the upload is successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-436">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-436">Syntax</span></span>


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-437">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-437">Attributes</span></span>



| <span data-ttu-id="c97d3-438">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-438">Attribute</span></span> | <span data-ttu-id="c97d3-439">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-439">Description</span></span>                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-440">href</span><span class="sxs-lookup"><span data-stu-id="c97d3-440">href</span></span>      | <span data-ttu-id="c97d3-441">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-441">Required.</span></span> <span data-ttu-id="c97d3-442">當上傳成功時，要顯示之伺服器端 HTML 頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-442">The URL of the server-side HTML page to display if the upload is successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-443">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-443">Element Information</span></span>



| <span data-ttu-id="c97d3-444">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-444">Parent Element</span></span>        | <span data-ttu-id="c97d3-445">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-445">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="c97d3-446">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-446">uploadinfo</span></span>](#syntax) | <span data-ttu-id="c97d3-447">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-447">None.</span></span> <span data-ttu-id="c97d3-448">允許文字。</span><span class="sxs-lookup"><span data-stu-id="c97d3-448">Text is allowed.</span></span> |



 

## <a name="target"></a><span data-ttu-id="c97d3-449">目標</span><span class="sxs-lookup"><span data-stu-id="c97d3-449">target</span></span>

<span data-ttu-id="c97d3-450">以通用命名慣例指定的目的資料夾 (UNC) 格式或 WebDAV 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c97d3-450">A destination folder specified in Universal Naming Convention (UNC) format or as a WebDAV server.</span></span> <span data-ttu-id="c97d3-451">如果傳送使用 WebDAV 或檔案系統通訊協定，則服務會新增這個目標來指定目的地資料夾。</span><span class="sxs-lookup"><span data-stu-id="c97d3-451">The service adds this target to specify a destination folder if the transfer uses a WebDAV or file system protocol.</span></span> <span data-ttu-id="c97d3-452">如果服務選擇以多部分 post 的方式執行檔案傳輸，則不應新增此元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-452">If the service chooses to perform the file transfer as a multi-part post, it should not add this element.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-453">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-453">Syntax</span></span>


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-454">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-454">Attributes</span></span>



| <span data-ttu-id="c97d3-455">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-455">Attribute</span></span> | <span data-ttu-id="c97d3-456">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-456">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-457">href</span><span class="sxs-lookup"><span data-stu-id="c97d3-457">href</span></span>      | <span data-ttu-id="c97d3-458">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-458">Required.</span></span> <span data-ttu-id="c97d3-459">目的資料夾的 URL。</span><span class="sxs-lookup"><span data-stu-id="c97d3-459">The URL of the destination folder.</span></span> <span data-ttu-id="c97d3-460">針對 WebDAV 使用 **HTTPs://** 格式，或針對 UNC 使用 **\\ \\ 伺服器 \\ 共用** 表單。</span><span class="sxs-lookup"><span data-stu-id="c97d3-460">Use the **https://** form for WebDAV or the **\\\\server\\share** form for UNC.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-461">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-461">Element Information</span></span>



| <span data-ttu-id="c97d3-462">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-462">Parent Element</span></span>        | <span data-ttu-id="c97d3-463">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-463">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="c97d3-464">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-464">uploadinfo</span></span>](#syntax) | <span data-ttu-id="c97d3-465">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-465">None.</span></span> <span data-ttu-id="c97d3-466">允許文字。</span><span class="sxs-lookup"><span data-stu-id="c97d3-466">Text is allowed.</span></span> |



 

## <a name="transfermanifest"></a><span data-ttu-id="c97d3-467">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="c97d3-467">transfermanifest</span></span>

<span data-ttu-id="c97d3-468">傳送資訊清單檔案的父節點。</span><span class="sxs-lookup"><span data-stu-id="c97d3-468">The parent node of the transfer manifest file.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-469">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-469">Syntax</span></span>


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-470">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-470">Attributes</span></span>

<span data-ttu-id="c97d3-471">無。</span><span class="sxs-lookup"><span data-stu-id="c97d3-471">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="c97d3-472">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-472">Element Information</span></span>



| <span data-ttu-id="c97d3-473">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-473">Parent Element</span></span> | <span data-ttu-id="c97d3-474">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-474">Child Elements</span></span>                                                    |
|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="c97d3-475">無</span><span class="sxs-lookup"><span data-stu-id="c97d3-475">None</span></span>           | <span data-ttu-id="c97d3-476">[filelist](#syntax)、 [folderlist](#syntax)、 [uploadinfo](#syntax)</span><span class="sxs-lookup"><span data-stu-id="c97d3-476">[filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax)</span></span> |



 

## <a name="uploadinfo"></a><span data-ttu-id="c97d3-477">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="c97d3-477">uploadinfo</span></span>

<span data-ttu-id="c97d3-478">專案的容器，可從交易中使用的上傳網站提供資訊。</span><span class="sxs-lookup"><span data-stu-id="c97d3-478">A container for elements providing information from the upload site used in the transaction.</span></span> <span data-ttu-id="c97d3-479">單一[transfermanifest](#syntax)節點底下可能包含多個[uploadinfo](#syntax)元素。</span><span class="sxs-lookup"><span data-stu-id="c97d3-479">Multiple [uploadinfo](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="c97d3-480">Syntax</span><span class="sxs-lookup"><span data-stu-id="c97d3-480">Syntax</span></span>


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="c97d3-481">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-481">Attributes</span></span>



| <span data-ttu-id="c97d3-482">屬性</span><span class="sxs-lookup"><span data-stu-id="c97d3-482">Attribute</span></span>    | <span data-ttu-id="c97d3-483">描述</span><span class="sxs-lookup"><span data-stu-id="c97d3-483">Description</span></span>                                                                 |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="c97d3-484">友好</span><span class="sxs-lookup"><span data-stu-id="c97d3-484">friendlyname</span></span> | <span data-ttu-id="c97d3-485">必要。</span><span class="sxs-lookup"><span data-stu-id="c97d3-485">Required.</span></span> <span data-ttu-id="c97d3-486">網站的易記名稱，此名稱會顯示在嚮導中。</span><span class="sxs-lookup"><span data-stu-id="c97d3-486">A friendly name for the website which is displayed in the wizard.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="c97d3-487">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c97d3-487">Element Information</span></span>



| <span data-ttu-id="c97d3-488">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="c97d3-488">Parent Element</span></span>              | <span data-ttu-id="c97d3-489">子元素</span><span class="sxs-lookup"><span data-stu-id="c97d3-489">Child Elements</span></span>                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c97d3-490">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="c97d3-490">transfermanifest</span></span>](#syntax) | <span data-ttu-id="c97d3-491">[cancelledpage](#syntax)、 [failurepage](#syntax)、我的 [最愛](#syntax)、 [htmlui](#syntax)、 [netplace](#syntax)、 [successpage](#syntax)、 [target](#syntax)</span><span class="sxs-lookup"><span data-stu-id="c97d3-491">[cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span></span> |



 

 

 



