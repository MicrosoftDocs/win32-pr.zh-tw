---
title: 屬性識別碼/位移組
description: 在屬性（property）屬性集值的計數之後，是屬性（Property）識別碼/位移配對屬性（property）值的陣列。
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967854"
---
# <a name="property-identifiersoffset-pairs"></a><span data-ttu-id="58f64-103">屬性識別碼/位移組</span><span class="sxs-lookup"><span data-stu-id="58f64-103">Property Identifiers/Offset Pairs</span></span>

<span data-ttu-id="58f64-104">在屬性（property）屬性集值的計數之後，是屬性（Property）識別碼/位移配對屬性（property）值的陣列。</span><span class="sxs-lookup"><span data-stu-id="58f64-104">Following the Count of Properties property set value is an array of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="58f64-105">屬性識別碼是可唯一識別區段內屬性的32位值。</span><span class="sxs-lookup"><span data-stu-id="58f64-105">Property Identifiers are 32-bit values that uniquely identify a property within a section.</span></span> <span data-ttu-id="58f64-106">位移組表示從區段開始到屬性類型/值組開頭的距離。</span><span class="sxs-lookup"><span data-stu-id="58f64-106">The Offset Pairs indicate the distance from the start of the section to the start of the property Type/Value Pair.</span></span> <span data-ttu-id="58f64-107">因為位移會相對於區段，所以可以將區段複製為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="58f64-107">Because the offsets are relative to the section, sections can be copied as an array of bytes.</span></span>

<span data-ttu-id="58f64-108">屬性識別碼不會以任何特定順序排序。</span><span class="sxs-lookup"><span data-stu-id="58f64-108">Property identifiers are not sorted in any particular order.</span></span> <span data-ttu-id="58f64-109">您可以從預存屬性集省略屬性;讀取器不能依賴特定順序或屬性識別碼的範圍。</span><span class="sxs-lookup"><span data-stu-id="58f64-109">Properties can be omitted from the stored property set; readers must not rely on a specific order or range of property identifiers.</span></span>

 

 




