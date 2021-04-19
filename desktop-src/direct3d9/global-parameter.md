---
description: 每個符合 DXSAS 的效果都必須定義一個具有全域語義的單一全域效果參數（最小值）。
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: 全域參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971936"
---
# <a name="global-parameter"></a><span data-ttu-id="37ca1-103">全域參數</span><span class="sxs-lookup"><span data-stu-id="37ca1-103">Global Parameter</span></span>

<span data-ttu-id="37ca1-104">每個符合 DXSAS 的效果都必須定義一個具有全域語義的單一全域效果參數（最小值）。</span><span class="sxs-lookup"><span data-stu-id="37ca1-104">Each DXSAS compliant effect must define, as a minimum, a single global effect parameter with the global semantic.</span></span> <span data-ttu-id="37ca1-105">全域參數也可以使用一或多個選擇性批註。</span><span class="sxs-lookup"><span data-stu-id="37ca1-105">The global parameter can also use one or more optional annotations.</span></span> <span data-ttu-id="37ca1-106">語法如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-106">The syntax is as follows:</span></span>


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



<span data-ttu-id="37ca1-107">其中：</span><span class="sxs-lookup"><span data-stu-id="37ca1-107">where:</span></span>

-   <span data-ttu-id="37ca1-108">VariableName 是使用者指定的 ASCII 文字字串變數名稱。</span><span class="sxs-lookup"><span data-stu-id="37ca1-108">VariableName is a user-specified, ASCII text string variable name.</span></span>
-   <span data-ttu-id="37ca1-109">SasGlobal 是將此參數識別為 global DXSAS 參數的語義關鍵字。</span><span class="sxs-lookup"><span data-stu-id="37ca1-109">SasGlobal is the semantic keyword that identifies this parameter as the global DXSAS parameter.</span></span>
-   <span data-ttu-id="37ca1-110">SasVersion 是唯一需要的批註。</span><span class="sxs-lookup"><span data-stu-id="37ca1-110">SasVersion is the only required annotation.</span></span>
-   <span data-ttu-id="37ca1-111">OptionalAnnotations 可包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="37ca1-111">OptionalAnnotations can include the following:</span></span>
    -   [<span data-ttu-id="37ca1-112">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="37ca1-112">SasEffectAuthor</span></span>](#saseffectauthor)
    -   [<span data-ttu-id="37ca1-113">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="37ca1-113">SasEffectAuthoringSoftware</span></span>](#saseffectauthoringsoftware)
    -   [<span data-ttu-id="37ca1-114">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="37ca1-114">SasEffectCategory</span></span>](#saseffectcategory)
    -   [<span data-ttu-id="37ca1-115">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="37ca1-115">SasEffectCompany</span></span>](#saseffectcompany)
    -   [<span data-ttu-id="37ca1-116">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="37ca1-116">SasEffectDescription</span></span>](#saseffectdescription)
    -   [<span data-ttu-id="37ca1-117">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="37ca1-117">SasEffectHelp</span></span>](#saseffecthelp)
    -   [<span data-ttu-id="37ca1-118">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="37ca1-118">SasEffectRevision</span></span>](#saseffectrevision)

## <a name="sasversion"></a><span data-ttu-id="37ca1-119">SasVersion</span><span class="sxs-lookup"><span data-stu-id="37ca1-119">SasVersion</span></span>

<span data-ttu-id="37ca1-120">唯一必要的注釋是 SasVersion。</span><span class="sxs-lookup"><span data-stu-id="37ca1-120">The only required annotation is SasVersion.</span></span> <span data-ttu-id="37ca1-121">其宣告如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-121">It is declared like this:</span></span>


```
int3 SasVersion = { major, minor, revision };
```



<span data-ttu-id="37ca1-122">其中：</span><span class="sxs-lookup"><span data-stu-id="37ca1-122">where:</span></span>

-   <span data-ttu-id="37ca1-123">「主要」表示 DXSAS 的主要版本。</span><span class="sxs-lookup"><span data-stu-id="37ca1-123">major indicates the DXSAS major release.</span></span> <span data-ttu-id="37ca1-124">DXSAS 的主要版本可以包含所定義的一組語義和注釋的變更。</span><span class="sxs-lookup"><span data-stu-id="37ca1-124">Major releases of DXSAS can contain sweeping changes to the set of semantics and annotations defined.</span></span> <span data-ttu-id="37ca1-125">您可以新增和移除語義和注釋，而且通常不保證與先前版本的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="37ca1-125">Semantics and annotations can be added and removed and, in general, backward compatibility with previous releases is not guaranteed.</span></span>
-   <span data-ttu-id="37ca1-126">[次要] 表示 SAS 次要版本。</span><span class="sxs-lookup"><span data-stu-id="37ca1-126">minor indicates the SAS minor release.</span></span> <span data-ttu-id="37ca1-127">DXSAS 的次要版本可以包含新的語義或批註的加入。</span><span class="sxs-lookup"><span data-stu-id="37ca1-127">Minor releases of DXSAS can include the addition of new semantics or annotations.</span></span> <span data-ttu-id="37ca1-128">此外，在 DXSAS 標準中，可以將語義和注釋標示為已淘汰。</span><span class="sxs-lookup"><span data-stu-id="37ca1-128">Additionally, semantics and annotations may be marked as deprecated in the DXSAS standard.</span></span> <span data-ttu-id="37ca1-129">主機應用程式仍然必須支援已被取代的語法和注釋，但是使用這類語義或批註時，可能會發出警告診斷。</span><span class="sxs-lookup"><span data-stu-id="37ca1-129">Deprecated semantics and annotations must still be supported by host applications but can emit a warning diagnostic when such a semantic or annotation is used.</span></span> <span data-ttu-id="37ca1-130">次要版本可回溯相容于先前的版本。</span><span class="sxs-lookup"><span data-stu-id="37ca1-130">Minor releases are backward compatible with previous releases.</span></span>
-   <span data-ttu-id="37ca1-131">修訂表示 DXSAS 修訂。</span><span class="sxs-lookup"><span data-stu-id="37ca1-131">revision indicates the DXSAS revision.</span></span> <span data-ttu-id="37ca1-132">DXSAS 的修訂僅作為修正 bug、移除不明確和精簡標準的方法。</span><span class="sxs-lookup"><span data-stu-id="37ca1-132">Revisions of DXSAS exist only as a means to fix bugs, remove ambiguity, and refine the standard.</span></span> <span data-ttu-id="37ca1-133">標準版的修訂與舊版的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="37ca1-133">Revisions to the standard are backward compatible with previous releases.</span></span>

<span data-ttu-id="37ca1-134">目前的版本為1.0.0。</span><span class="sxs-lookup"><span data-stu-id="37ca1-134">The current version is 1.0.0.</span></span> <span data-ttu-id="37ca1-135">此批註沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="37ca1-135">There is no default value for this annotation.</span></span>

## <a name="saseffectauthor"></a><span data-ttu-id="37ca1-136">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="37ca1-136">SasEffectAuthor</span></span>

<span data-ttu-id="37ca1-137">這會宣告建立效果的人員。</span><span class="sxs-lookup"><span data-stu-id="37ca1-137">This declares the person who created the effect.</span></span> <span data-ttu-id="37ca1-138">其宣告如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-138">It is declared like this:</span></span>


```
string SasEffectAuthor = "value";
```



<span data-ttu-id="37ca1-139">其中 value 是識別效果作者的字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-139">where value is a string that identifies the effect author.</span></span> <span data-ttu-id="37ca1-140">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-140">The default is an empty string.</span></span>

## <a name="saseffectauthoringsoftware"></a><span data-ttu-id="37ca1-141">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="37ca1-141">SasEffectAuthoringSoftware</span></span>

<span data-ttu-id="37ca1-142">這會宣告此效果所撰寫的軟體。</span><span class="sxs-lookup"><span data-stu-id="37ca1-142">This declares the software that the effect was authored on.</span></span> <span data-ttu-id="37ca1-143">其宣告如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-143">It is declared like this:</span></span>


```
string SasEffectAuthoringSoftware = "value";
```



<span data-ttu-id="37ca1-144">其中 value 是識別效果撰寫軟體的字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-144">where value is a string that identifies the effect authoring software.</span></span> <span data-ttu-id="37ca1-145">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-145">The default is an empty string.</span></span>

## <a name="saseffectcategory"></a><span data-ttu-id="37ca1-146">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="37ca1-146">SasEffectCategory</span></span>

<span data-ttu-id="37ca1-147">這會宣告效果類別目錄。</span><span class="sxs-lookup"><span data-stu-id="37ca1-147">This declares the effect category.</span></span> <span data-ttu-id="37ca1-148">其宣告如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-148">It is declared like this:</span></span>


```
string SasEffectCategory = "value";
```



<span data-ttu-id="37ca1-149">其中 value 是識別效果類別目錄的字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-149">where value is a string that identifies the effect category.</span></span> <span data-ttu-id="37ca1-150">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-150">The default is an empty string.</span></span> <span data-ttu-id="37ca1-151">類別是透過類似路徑的值來表示，使用正斜線作為分隔符號。</span><span class="sxs-lookup"><span data-stu-id="37ca1-151">The category is expressed via a path-like value using the forward slash as a delimiter.</span></span> <span data-ttu-id="37ca1-152">效果只能屬於一個類別，因為沒有任何語法可在單一 SasEffectCategory 值內的多個路徑中表示包含。</span><span class="sxs-lookup"><span data-stu-id="37ca1-152">Effects can only belong to one category as there is no syntax for expressing inclusion in multiple paths within a single SasEffectCategory value.</span></span> <span data-ttu-id="37ca1-153">主應用程式不會將這個批註的值視為區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="37ca1-153">The value of this annotation is not treated as case-sensitive by the host application.</span></span>

## <a name="saseffectcompany"></a><span data-ttu-id="37ca1-154">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="37ca1-154">SasEffectCompany</span></span>

<span data-ttu-id="37ca1-155">這會宣告建立效果的公司。</span><span class="sxs-lookup"><span data-stu-id="37ca1-155">This declares the company that created the effect.</span></span> <span data-ttu-id="37ca1-156">其宣告如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-156">It is declared like this:</span></span>


```
string SasEffectCompany = "value";
```



<span data-ttu-id="37ca1-157">其中的值是可識別擁有效果之公司名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-157">where value is a string that identifies the name of the company that owns the effect.</span></span> <span data-ttu-id="37ca1-158">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-158">The default is an empty string.</span></span>

## <a name="saseffectdescription"></a><span data-ttu-id="37ca1-159">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="37ca1-159">SasEffectDescription</span></span>

<span data-ttu-id="37ca1-160">這會描述效果。</span><span class="sxs-lookup"><span data-stu-id="37ca1-160">This describes the effect.</span></span> <span data-ttu-id="37ca1-161">其宣告如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-161">It is declared like this:</span></span>


```
string SasEffectDescription = "value";
```



<span data-ttu-id="37ca1-162">其中的值是描述效果的字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-162">where value is a string that describes the effect.</span></span> <span data-ttu-id="37ca1-163">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-163">The default is an empty string.</span></span>

## <a name="saseffecthelp"></a><span data-ttu-id="37ca1-164">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="37ca1-164">SasEffectHelp</span></span>

<span data-ttu-id="37ca1-165">這是一個說明字串，可在每次要求相關效果的說明時向使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="37ca1-165">This is a help string that can be displayed to the user whenever help on the associated effect is requested.</span></span> <span data-ttu-id="37ca1-166">其宣告如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-166">It is declared like this:</span></span>


```
string SasEffectHelp = "value";
```



<span data-ttu-id="37ca1-167">其中的值是當使用者要求協助時，可以顯示的字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-167">where value is a string that can be displayed if the user requests help.</span></span> <span data-ttu-id="37ca1-168">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-168">The default is an empty string.</span></span>

## <a name="saseffectrevision"></a><span data-ttu-id="37ca1-169">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="37ca1-169">SasEffectRevision</span></span>

<span data-ttu-id="37ca1-170">此批註可讓工具和使用者記錄相關效果檔案的修訂編號。</span><span class="sxs-lookup"><span data-stu-id="37ca1-170">This annotation allows tools and users to record the revision number of the associated effect file.</span></span> <span data-ttu-id="37ca1-171">例如，使用者可以在此注釋的值中插入適當的關鍵字，以在其最愛的修訂控制軟體中叫用關鍵字替代。</span><span class="sxs-lookup"><span data-stu-id="37ca1-171">For example, users could insert appropriate keywords in the value of this annotation to invoke keyword substitution in their favorite revision control software.</span></span> <span data-ttu-id="37ca1-172">其宣告如下：</span><span class="sxs-lookup"><span data-stu-id="37ca1-172">It is declared like this:</span></span>


```
string SasEffectRevision = "value";
```



<span data-ttu-id="37ca1-173">其中值是可識別效果修訂的字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-173">where value is a string that identifies the effect revision.</span></span> <span data-ttu-id="37ca1-174">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="37ca1-174">The default is an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="37ca1-175">範例</span><span class="sxs-lookup"><span data-stu-id="37ca1-175">Examples</span></span>

<span data-ttu-id="37ca1-176">以下是只使用單一必要注釋的範例：</span><span class="sxs-lookup"><span data-stu-id="37ca1-176">Here is an example that uses only the single, required annotation:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



<span data-ttu-id="37ca1-177">以下是使用必要注釋和數個選用注釋的範例：</span><span class="sxs-lookup"><span data-stu-id="37ca1-177">Here is an example that uses the required annotation and several optional annotations:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a><span data-ttu-id="37ca1-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="37ca1-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37ca1-179">DirectX 標準注釋和語義參考</span><span class="sxs-lookup"><span data-stu-id="37ca1-179">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



