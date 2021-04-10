---
description: ICE15 會驗證 MIME 和延伸模組資料表中的內容類型和延伸模組參考是否互相反向。 MIME 資料表必須參考延伸模組資料表參考相同內容類型之延伸模組的內容類型。
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027027"
---
# <a name="ice15"></a><span data-ttu-id="4b421-104">ICE15</span><span class="sxs-lookup"><span data-stu-id="4b421-104">ICE15</span></span>

<span data-ttu-id="4b421-105">ICE15 會驗證 [MIME](mime-table.md) 和 [延伸](extension-table.md) 模組資料表中的內容類型和延伸模組參考是否互相反向。</span><span class="sxs-lookup"><span data-stu-id="4b421-105">ICE15 validates that content type and extension references in the [MIME](mime-table.md) and [Extension](extension-table.md) tables are reciprocal.</span></span> <span data-ttu-id="4b421-106">MIME 資料表必須參考延伸模組資料表參考相同內容類型之延伸模組的內容類型。</span><span class="sxs-lookup"><span data-stu-id="4b421-106">The MIME table must reference a content type to an extension that the Extension table references back to the same content type.</span></span>

<span data-ttu-id="4b421-107">只要 MIME 型別參考回其中一個擴充功能，多個擴充功能就可以參考相同的 MIME 型別。</span><span class="sxs-lookup"><span data-stu-id="4b421-107">Multiple extensions can reference the same MIME type, as long as the MIME type references back to one of the extensions.</span></span> <span data-ttu-id="4b421-108">多個 MIME 類型可以參考相同的副檔名，只要副檔名參考回其中一個 MIME 類型即可。</span><span class="sxs-lookup"><span data-stu-id="4b421-108">Multiple MIME types can reference the same extension, as long as the extension references back to one of the MIME types.</span></span>

<span data-ttu-id="4b421-109">請注意，每當 MIME 參考副檔名時，延伸模組資料表中的 MIME 資料行都不能 \_ 設為 Null。</span><span class="sxs-lookup"><span data-stu-id="4b421-109">Note that whenever a MIME references an extension, that extension cannot have the MIME\_ column in the Extension table set to Null.</span></span>

## <a name="result"></a><span data-ttu-id="4b421-110">結果</span><span class="sxs-lookup"><span data-stu-id="4b421-110">Result</span></span>

<span data-ttu-id="4b421-111">如果內容類型和延伸模組參考不是交互，ICE15 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b421-111">ICE15 posts an error if the content type and extension references are not reciprocal.</span></span>

## <a name="example"></a><span data-ttu-id="4b421-112">範例</span><span class="sxs-lookup"><span data-stu-id="4b421-112">Example</span></span>

<span data-ttu-id="4b421-113">ICE15 會針對所顯示的範例張貼兩則錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="4b421-113">ICE15 posts two error messages for the example shown:</span></span>

-   <span data-ttu-id="4b421-114">MIME 資料表中的內容類型 test/x 翼參考了延伸模組 tst，但延伸模組表中的副檔名 tst 參考了翼翼/x 翼。</span><span class="sxs-lookup"><span data-stu-id="4b421-114">The content type test/x-flaps in the MIME table references the extension tst, but the extension tst in the Extension table references flaps/x-flaps.</span></span> <span data-ttu-id="4b421-115">這不是交互。</span><span class="sxs-lookup"><span data-stu-id="4b421-115">This is not reciprocal.</span></span>
-   <span data-ttu-id="4b421-116">內容類型的翼/x 翼參考延伸模組 flp，但延伸模組資料表的 MIME 資料行中有 Null 專案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4b421-116">The content type flaps/x-flaps references the extension flp, but that extension has a Null entry in the MIME\_ column of the Extension table.</span></span>

<span data-ttu-id="4b421-117">[MIME 表格](mime-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="4b421-117">[MIME Table](mime-table.md) (partial)</span></span>



| <span data-ttu-id="4b421-118">ContentType</span><span class="sxs-lookup"><span data-stu-id="4b421-118">ContentType</span></span>   | <span data-ttu-id="4b421-119">分機\_</span><span class="sxs-lookup"><span data-stu-id="4b421-119">Extension\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="4b421-120">測試/x 測試</span><span class="sxs-lookup"><span data-stu-id="4b421-120">test/x-test</span></span>   | <span data-ttu-id="4b421-121">Tst</span><span class="sxs-lookup"><span data-stu-id="4b421-121">tst</span></span>         |
| <span data-ttu-id="4b421-122">翼翼/x 翼</span><span class="sxs-lookup"><span data-stu-id="4b421-122">flaps/x-flaps</span></span> | <span data-ttu-id="4b421-123">flp</span><span class="sxs-lookup"><span data-stu-id="4b421-123">flp</span></span>         |



 

<span data-ttu-id="4b421-124">[延伸模組資料表](extension-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="4b421-124">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="4b421-125">分機</span><span class="sxs-lookup"><span data-stu-id="4b421-125">Extension</span></span> | <span data-ttu-id="4b421-126">MIME\_</span><span class="sxs-lookup"><span data-stu-id="4b421-126">MIME\_</span></span>        |
|-----------|---------------|
| <span data-ttu-id="4b421-127">Tst</span><span class="sxs-lookup"><span data-stu-id="4b421-127">tst</span></span>       | <span data-ttu-id="4b421-128">翼翼/x 翼</span><span class="sxs-lookup"><span data-stu-id="4b421-128">flaps/x-flaps</span></span> |
| <span data-ttu-id="4b421-129">flp</span><span class="sxs-lookup"><span data-stu-id="4b421-129">flp</span></span>       | <span data-ttu-id="4b421-130">Null</span><span class="sxs-lookup"><span data-stu-id="4b421-130">Null</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="4b421-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b421-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b421-132">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="4b421-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



