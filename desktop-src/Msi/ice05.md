---
description: ICE05 會驗證某些資料表是否包含必要的專案。 這包括但不限於檢查必要屬性的屬性資料表： ProductName、ProductLanguage、ProductVersion、ProductCode 和製造商。
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994371"
---
# <a name="ice05"></a><span data-ttu-id="c9eaf-104">ICE05</span><span class="sxs-lookup"><span data-stu-id="c9eaf-104">ICE05</span></span>

<span data-ttu-id="c9eaf-105">ICE05 會驗證某些資料表是否包含必要的專案。</span><span class="sxs-lookup"><span data-stu-id="c9eaf-105">ICE05 validates that certain tables contain required entries.</span></span> <span data-ttu-id="c9eaf-106">這包括但不限於檢查必要屬性的 [屬性資料表](property-table.md) ： [**ProductName**](productname.md)、 [**ProductLanguage**](productlanguage.md)、 [**ProductVersion**](productversion.md)、 [**ProductCode**](productcode.md)和 [**製造商**](manufacturer.md)。</span><span class="sxs-lookup"><span data-stu-id="c9eaf-106">This includes, but is not restricted to, checking the [Property table](property-table.md) for the required properties: [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md), and [**Manufacturer**](manufacturer.md).</span></span>

## <a name="result"></a><span data-ttu-id="c9eaf-107">結果</span><span class="sxs-lookup"><span data-stu-id="c9eaf-107">Result</span></span>

<span data-ttu-id="c9eaf-108">如果遺漏必要的專案，ICE05 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9eaf-108">ICE05 posts an error if a required entry is missing.</span></span>

## <a name="example"></a><span data-ttu-id="c9eaf-109">範例</span><span class="sxs-lookup"><span data-stu-id="c9eaf-109">Example</span></span>

<span data-ttu-id="c9eaf-110">如範例所示，ICE05 會報告 ' Property ' 資料表中是否需要 ' ProductVersion ' 專案。</span><span class="sxs-lookup"><span data-stu-id="c9eaf-110">For the example shown, ICE05 would report that the entry: 'ProductVersion' is required in the 'Property' table.</span></span>

<span data-ttu-id="c9eaf-111">[屬性工作表](property-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="c9eaf-111">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="c9eaf-112">屬性</span><span class="sxs-lookup"><span data-stu-id="c9eaf-112">Property</span></span>                           | <span data-ttu-id="c9eaf-113">值</span><span class="sxs-lookup"><span data-stu-id="c9eaf-113">Value</span></span>     |
|------------------------------------|-----------|
| [<span data-ttu-id="c9eaf-114">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="c9eaf-114">**ProductName**</span></span>](productname.md) | <span data-ttu-id="c9eaf-115">MyProduct</span><span class="sxs-lookup"><span data-stu-id="c9eaf-115">MyProduct</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c9eaf-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9eaf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9eaf-117">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="c9eaf-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



