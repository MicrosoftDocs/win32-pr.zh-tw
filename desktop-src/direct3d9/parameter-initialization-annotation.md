---
description: 您可以使用此注釋，將外部檔案的內容定義為效果參數的初始化值。
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: 參數初始化注釋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187409"
---
# <a name="parameter-initialization-annotation"></a><span data-ttu-id="2bbcf-103">參數初始化注釋</span><span class="sxs-lookup"><span data-stu-id="2bbcf-103">Parameter Initialization Annotation</span></span>

<span data-ttu-id="2bbcf-104">您可以使用此注釋，將外部檔案的內容定義為效果參數的初始化值。</span><span class="sxs-lookup"><span data-stu-id="2bbcf-104">Use this annotation to define the contents of an external file as the initialization value for an effect parameter.</span></span> <span data-ttu-id="2bbcf-105">例如：</span><span class="sxs-lookup"><span data-stu-id="2bbcf-105">For example:</span></span>


```
string SasResourceAddress = "Value";
```



<span data-ttu-id="2bbcf-106">其中，值是可能包含絕對或相對路徑的 ASCII 文字字串。</span><span class="sxs-lookup"><span data-stu-id="2bbcf-106">where Value is an ASCII text string that may contain an absolute or relative path.</span></span> <span data-ttu-id="2bbcf-107">相對路徑是相對於包含效果檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="2bbcf-107">A relative path is relative to the directory that contains the effect file.</span></span>

<span data-ttu-id="2bbcf-108">請看以下範例：</span><span class="sxs-lookup"><span data-stu-id="2bbcf-108">Here is an example:</span></span>


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



<span data-ttu-id="2bbcf-109">預設值為空字串。</span><span class="sxs-lookup"><span data-stu-id="2bbcf-109">The default value is an empty string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bbcf-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="2bbcf-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bbcf-111">DirectX 標準注釋和語義參考</span><span class="sxs-lookup"><span data-stu-id="2bbcf-111">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



