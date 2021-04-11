---
description: ICEM06 會檢查模組對功能的直接參考是否無效。
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849647"
---
# <a name="icem06"></a><span data-ttu-id="9cd62-103">ICEM06</span><span class="sxs-lookup"><span data-stu-id="9cd62-103">ICEM06</span></span>

<span data-ttu-id="9cd62-104">ICEM06 會檢查模組對功能的直接參考是否無效。</span><span class="sxs-lookup"><span data-stu-id="9cd62-104">ICEM06 checks for invalid direct references to features by the module.</span></span>

<span data-ttu-id="9cd62-105">Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。</span><span class="sxs-lookup"><span data-stu-id="9cd62-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="9cd62-106">結果</span><span class="sxs-lookup"><span data-stu-id="9cd62-106">Result</span></span>

<span data-ttu-id="9cd62-107">當模組資料庫包含功能的直接參考時，ICEM06 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="9cd62-107">ICEM06 posts an error when the module database contains direct references to a feature.</span></span> <span data-ttu-id="9cd62-108">功能資訊必須由模組的使用者提供。</span><span class="sxs-lookup"><span data-stu-id="9cd62-108">Feature information must be provided by the user of the module.</span></span>

## <a name="example"></a><span data-ttu-id="9cd62-109">範例</span><span class="sxs-lookup"><span data-stu-id="9cd62-109">Example</span></span>

<span data-ttu-id="9cd62-110">ICEM06 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="9cd62-110">ICEM06 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

<span data-ttu-id="9cd62-111"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="9cd62-111">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="9cd62-112">快速鍵</span><span class="sxs-lookup"><span data-stu-id="9cd62-112">Shortcut</span></span>          | <span data-ttu-id="9cd62-113">目標</span><span class="sxs-lookup"><span data-stu-id="9cd62-113">Target</span></span>                                 |
|-------------------|----------------------------------------|
| <span data-ttu-id="9cd62-114">Shortcut1.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="9cd62-114">Shortcut1.*GUID1*</span></span> | <span data-ttu-id="9cd62-115">cmd.exe</span><span class="sxs-lookup"><span data-stu-id="9cd62-115">cmd.exe</span></span>                                |
| <span data-ttu-id="9cd62-116">Shortcut2.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="9cd62-116">Shortcut2.*GUID1*</span></span> | <span data-ttu-id="9cd62-117">\[MyProp\]</span><span class="sxs-lookup"><span data-stu-id="9cd62-117">\[MyProp\]</span></span>                             |
| <span data-ttu-id="9cd62-118">Shortcut3.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="9cd62-118">Shortcut3.*GUID1*</span></span> | {00000000-0000-0000-0000-000000000000} |



 

<span data-ttu-id="9cd62-119">[類別表](class-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="9cd62-119">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="9cd62-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="9cd62-120">CLSID</span></span>   | <span data-ttu-id="9cd62-121">Context</span><span class="sxs-lookup"><span data-stu-id="9cd62-121">Context</span></span>       | <span data-ttu-id="9cd62-122">元件\_</span><span class="sxs-lookup"><span data-stu-id="9cd62-122">Component\_</span></span> | <span data-ttu-id="9cd62-123">功能\_</span><span class="sxs-lookup"><span data-stu-id="9cd62-123">Feature\_</span></span>                              |
|---------|---------------|-------------|----------------------------------------|
| <span data-ttu-id="9cd62-124">*GUID1*</span><span class="sxs-lookup"><span data-stu-id="9cd62-124">*GUID1*</span></span> | <span data-ttu-id="9cd62-125">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="9cd62-125">LocalServer32</span></span> | <span data-ttu-id="9cd62-126">Component1</span><span class="sxs-lookup"><span data-stu-id="9cd62-126">Component1</span></span>  | {00000000-0000-0000-0000-000000000000} |
| <span data-ttu-id="9cd62-127">*GUID2*</span><span class="sxs-lookup"><span data-stu-id="9cd62-127">*GUID2*</span></span> | <span data-ttu-id="9cd62-128">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="9cd62-128">LocalServer32</span></span> | <span data-ttu-id="9cd62-129">Component2</span><span class="sxs-lookup"><span data-stu-id="9cd62-129">Component2</span></span>  | <span data-ttu-id="9cd62-130">MyFeature</span><span class="sxs-lookup"><span data-stu-id="9cd62-130">MyFeature</span></span>                              |



 

<span data-ttu-id="9cd62-131">ICEM06 會報告第一個錯誤，因為快捷方式資料表中的第一筆記錄在目標欄位中有一個專案，而該專案不是屬性或 null GUID。</span><span class="sxs-lookup"><span data-stu-id="9cd62-131">ICEM06 reports the first error because the first record in the Shortcut table has an entry in the Target field that is not a property or a null GUID.</span></span> <span data-ttu-id="9cd62-132">模組無法直接參考功能。</span><span class="sxs-lookup"><span data-stu-id="9cd62-132">A module cannot reference a feature directly.</span></span> <span data-ttu-id="9cd62-133">功能資訊必須由模組的使用者提供。</span><span class="sxs-lookup"><span data-stu-id="9cd62-133">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="9cd62-134">若要修正這個錯誤，應該以 null GUID 取代功能的參考。</span><span class="sxs-lookup"><span data-stu-id="9cd62-134">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

<span data-ttu-id="9cd62-135">ICEM06 會報告第二個錯誤，因為類別資料表中的第二筆記錄在功能欄位中有一個不是 null GUID 的專案。</span><span class="sxs-lookup"><span data-stu-id="9cd62-135">ICEM06 reports the second error because the second record in the Class table has an entry in the Feature field that is not a null GUID.</span></span> <span data-ttu-id="9cd62-136">模組無法直接參考功能。</span><span class="sxs-lookup"><span data-stu-id="9cd62-136">A module cannot reference a feature directly.</span></span> <span data-ttu-id="9cd62-137">功能資訊必須由模組的使用者提供。</span><span class="sxs-lookup"><span data-stu-id="9cd62-137">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="9cd62-138">若要修正這個錯誤，應該以 null GUID 取代功能的參考。</span><span class="sxs-lookup"><span data-stu-id="9cd62-138">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cd62-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cd62-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cd62-140">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="9cd62-140">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



