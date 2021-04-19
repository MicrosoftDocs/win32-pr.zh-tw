---
description: ICE65 會檢查環境資料表是否沒有不正確前置詞或附加值。
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987342"
---
# <a name="ice65"></a><span data-ttu-id="9fce9-103">ICE65</span><span class="sxs-lookup"><span data-stu-id="9fce9-103">ICE65</span></span>

<span data-ttu-id="9fce9-104">ICE65 會檢查 [環境資料表](environment-table.md) 是否沒有不正確前置詞或附加值。</span><span class="sxs-lookup"><span data-stu-id="9fce9-104">ICE65 checks that the [Environment table](environment-table.md) does not have invalid prefix or append values.</span></span>

<span data-ttu-id="9fce9-105">若無法修正 ICE65 回報的警告或錯誤，通常會導致安裝、卸載或修復環境變數時發生問題。</span><span class="sxs-lookup"><span data-stu-id="9fce9-105">Failure to fix a warning or error reported by ICE65 generally leads to problems in install, uninstall, or repair of the environment variable.</span></span> <span data-ttu-id="9fce9-106">例如，如果該變數的一或多個值具有尾端分隔符號，則只有某些特定變數的值可能會被移除。</span><span class="sxs-lookup"><span data-stu-id="9fce9-106">For example, only some values of a particular variable may be removed if one or more of the values for that variable have a trailing separator.</span></span>

## <a name="result"></a><span data-ttu-id="9fce9-107">結果</span><span class="sxs-lookup"><span data-stu-id="9fce9-107">Result</span></span>

<span data-ttu-id="9fce9-108">如果環境資料表有不正確前置詞或附加值，ICE65 就會張貼警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fce9-108">ICE65 posts a warning or an error if the environment table has invalid prefix or append values.</span></span>

## <a name="example"></a><span data-ttu-id="9fce9-109">範例</span><span class="sxs-lookup"><span data-stu-id="9fce9-109">Example</span></span>

<span data-ttu-id="9fce9-110">ICE65 會針對所顯示的範例報告下列錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="9fce9-110">ICE65 reports the following error and warning for the example shown.</span></span>

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

<span data-ttu-id="9fce9-111">值結尾的尾端 null (\[ ~ \]) 會將此值標示為任何現有值的前面。</span><span class="sxs-lookup"><span data-stu-id="9fce9-111">The trailing null at the end of the value (\[~\]) marks this value to be prepended to any existing value.</span></span> <span data-ttu-id="9fce9-112">緊接在 null (分號) 的字元會成為此值的分隔符號。</span><span class="sxs-lookup"><span data-stu-id="9fce9-112">The character immediately before the null (a semicolon) becomes the separator for this value.</span></span> <span data-ttu-id="9fce9-113">此值也是字串開頭的分號。</span><span class="sxs-lookup"><span data-stu-id="9fce9-113">This value has a semicolon at the beginning of the string as well.</span></span>

<span data-ttu-id="9fce9-114">若要修正此錯誤，只需刪除前置分號。</span><span class="sxs-lookup"><span data-stu-id="9fce9-114">To fix this error, simply delete the leading semicolon.</span></span>

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

<span data-ttu-id="9fce9-115">值中的前置 null (\[ ~ \]) 會將此值標示為附加至任何現有的值。</span><span class="sxs-lookup"><span data-stu-id="9fce9-115">The leading null in the value (\[~\]) marks this value to be appended to any existing value.</span></span> <span data-ttu-id="9fce9-116">緊接在 null 之後的字元會變成此值的分隔符號。</span><span class="sxs-lookup"><span data-stu-id="9fce9-116">The character immediately after the null becomes the separator for this value.</span></span> <span data-ttu-id="9fce9-117">在此情況下，該字元是字母 "e"，這也會出現在要附加的字串中間。</span><span class="sxs-lookup"><span data-stu-id="9fce9-117">In this case, that character is the letter "e", which also occurs in the middle of the string to be appended.</span></span> <span data-ttu-id="9fce9-118">此條件 (有一個分隔符號與要附加之字串內的字元相同，) 可能會導致無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="9fce9-118">This condition (having a separator that is the same as a character within the string to be appended) can cause unpredictable results.</span></span>

<span data-ttu-id="9fce9-119">字母 "e" 是通用字母，可能在值中找到。</span><span class="sxs-lookup"><span data-stu-id="9fce9-119">The letter "e", being a common letter, is likely to be found in the value.</span></span> <span data-ttu-id="9fce9-120">更好的選擇是 ";" 或一些其他非英數位元。</span><span class="sxs-lookup"><span data-stu-id="9fce9-120">A better choice would be ";" or some other non-alphanumeric character.</span></span> <span data-ttu-id="9fce9-121">不過 (不過，如果值是路徑，則 "：" 和 " \\ " 和 "." 是有風險的選擇。 ) </span><span class="sxs-lookup"><span data-stu-id="9fce9-121">(However, if the value is a path, then ":" and "\\" and "." are risky choices.)</span></span>

<span data-ttu-id="9fce9-122">若要修正此警告，請使用不同的分隔字元。</span><span class="sxs-lookup"><span data-stu-id="9fce9-122">To fix this warning, use a different separator character.</span></span>

[<span data-ttu-id="9fce9-123">環境資料表</span><span class="sxs-lookup"><span data-stu-id="9fce9-123">Environment Table</span></span>](environment-table.md)



| <span data-ttu-id="9fce9-124">元件</span><span class="sxs-lookup"><span data-stu-id="9fce9-124">Component</span></span> | <span data-ttu-id="9fce9-125">目錄</span><span class="sxs-lookup"><span data-stu-id="9fce9-125">Directory</span></span> | <span data-ttu-id="9fce9-126">屬性</span><span class="sxs-lookup"><span data-stu-id="9fce9-126">Attributes</span></span>         | <span data-ttu-id="9fce9-127">KeyPath</span><span class="sxs-lookup"><span data-stu-id="9fce9-127">KeyPath</span></span>       |
|-----------|-----------|--------------------|---------------|
| <span data-ttu-id="9fce9-128">Var1</span><span class="sxs-lookup"><span data-stu-id="9fce9-128">Var1</span></span>      | <span data-ttu-id="9fce9-129">TestVar</span><span class="sxs-lookup"><span data-stu-id="9fce9-129">TestVar</span></span>   | <span data-ttu-id="9fce9-130">\[~\];AppendThis</span><span class="sxs-lookup"><span data-stu-id="9fce9-130">\[~\];AppendThis</span></span>   | <span data-ttu-id="9fce9-131">TestComponent</span><span class="sxs-lookup"><span data-stu-id="9fce9-131">TestComponent</span></span> |
| <span data-ttu-id="9fce9-132">Var2</span><span class="sxs-lookup"><span data-stu-id="9fce9-132">Var2</span></span>      | <span data-ttu-id="9fce9-133">TestVar</span><span class="sxs-lookup"><span data-stu-id="9fce9-133">TestVar</span></span>   | <span data-ttu-id="9fce9-134">\[~\]eAppendThis</span><span class="sxs-lookup"><span data-stu-id="9fce9-134">\[~\]eAppendThis</span></span>   | <span data-ttu-id="9fce9-135">TestComponent</span><span class="sxs-lookup"><span data-stu-id="9fce9-135">TestComponent</span></span> |
| <span data-ttu-id="9fce9-136">Var3</span><span class="sxs-lookup"><span data-stu-id="9fce9-136">Var3</span></span>      | <span data-ttu-id="9fce9-137">TestVar</span><span class="sxs-lookup"><span data-stu-id="9fce9-137">TestVar</span></span>   | <span data-ttu-id="9fce9-138">;PrependThis;\[~\]</span><span class="sxs-lookup"><span data-stu-id="9fce9-138">;PrependThis;\[~\]</span></span> | <span data-ttu-id="9fce9-139">TestComponent</span><span class="sxs-lookup"><span data-stu-id="9fce9-139">TestComponent</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9fce9-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fce9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fce9-141">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="9fce9-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



