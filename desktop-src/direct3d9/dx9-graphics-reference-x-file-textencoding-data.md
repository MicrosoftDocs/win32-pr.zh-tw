---
description: 資料物件包含實際資料或該資料的參考。 每個資料物件都有一個指定資料類型的對應範本。 下列各節將討論資料物件的表單和部分。
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: '資料 (X 檔案格式，文字編碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385744"
---
# <a name="data-x-file-format-text-encoding"></a><span data-ttu-id="63d9c-105">資料 (X 檔案格式，文字編碼) </span><span class="sxs-lookup"><span data-stu-id="63d9c-105">Data (X file format, text encoding)</span></span>

<span data-ttu-id="63d9c-106">資料物件包含實際資料或該資料的參考。</span><span class="sxs-lookup"><span data-stu-id="63d9c-106">Data objects contain the actual data or a reference to that data.</span></span> <span data-ttu-id="63d9c-107">每個資料物件都有一個指定資料類型的對應範本。</span><span class="sxs-lookup"><span data-stu-id="63d9c-107">Each data object has a corresponding template that specifies the data type.</span></span> <span data-ttu-id="63d9c-108">下列各節將討論資料物件的表單和部分。</span><span class="sxs-lookup"><span data-stu-id="63d9c-108">The following sections discuss the form and parts of data objects.</span></span>

## <a name="form-identifier-and-name"></a><span data-ttu-id="63d9c-109">表單、識別碼和名稱</span><span class="sxs-lookup"><span data-stu-id="63d9c-109">Form, Identifier, and Name</span></span>

<span data-ttu-id="63d9c-110">資料物件具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="63d9c-110">Data objects have the following form.</span></span>


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



<span data-ttu-id="63d9c-111">識別碼是強制性的，且必須符合先前定義的資料類型或基本類型。</span><span class="sxs-lookup"><span data-stu-id="63d9c-111">The identifier is compulsory and must match a previously defined data type or primitive.</span></span> <span data-ttu-id="63d9c-112">不過，名稱是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="63d9c-112">However, the name is optional.</span></span>

## <a name="data-members"></a><span data-ttu-id="63d9c-113">資料成員</span><span class="sxs-lookup"><span data-stu-id="63d9c-113">Data Members</span></span>

<span data-ttu-id="63d9c-114">資料成員可以是下列其中一項：資料物件、資料參考、整數清單、浮動清單或字串清單。</span><span class="sxs-lookup"><span data-stu-id="63d9c-114">Data members can be one of the following: data object, data reference, integer list, float list, or string list.</span></span>

<span data-ttu-id="63d9c-115">資料物件是嵌套的資料物件。</span><span class="sxs-lookup"><span data-stu-id="63d9c-115">A data object is a nested data object.</span></span> <span data-ttu-id="63d9c-116">這可表示檔案格式的階層式本質。</span><span class="sxs-lookup"><span data-stu-id="63d9c-116">This enables the hierarchical nature of the file format to be expressed.</span></span> <span data-ttu-id="63d9c-117">階層中允許的嵌套資料物件類型可能會受到限制。</span><span class="sxs-lookup"><span data-stu-id="63d9c-117">The types of nested data objects allowed in the hierarchy may be restricted.</span></span>

<span data-ttu-id="63d9c-118">資料參考是先前遇到之資料物件的參考，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="63d9c-118">A data reference is a reference to a previously encountered data object as shown in the following example.</span></span>


```
{
  name |
  UUID |
  name UUID
}
```



<span data-ttu-id="63d9c-119">整數清單是以分號分隔的整數清單，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="63d9c-119">An integer list is a semicolon-separated list of integers, as shown in the following example.</span></span>


```
1; 2; 3;
```



<span data-ttu-id="63d9c-120">Float 清單是以分號分隔的浮動清單，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="63d9c-120">A float list is a semicolon-separated list of floats, as shown in the following example.</span></span>


```
1.0; 2.0; 3.0;
```



<span data-ttu-id="63d9c-121">字串清單是以分號分隔的字串清單，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="63d9c-121">A string list is a semicolon-separated list of strings, as shown in the following example.</span></span>


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a><span data-ttu-id="63d9c-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="63d9c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63d9c-123">文字編碼方式</span><span class="sxs-lookup"><span data-stu-id="63d9c-123">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



