---
description: ICE55 會驗證所有 LockPermission 物件都存在，而且具有有效的許可權值。
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194096"
---
# <a name="ice55"></a><span data-ttu-id="290c0-103">ICE55</span><span class="sxs-lookup"><span data-stu-id="290c0-103">ICE55</span></span>

<span data-ttu-id="290c0-104">ICE55 會驗證所有 LockPermission 物件都存在，而且具有有效的許可權值。</span><span class="sxs-lookup"><span data-stu-id="290c0-104">ICE55 validates that all LockPermission objects exist and have valid permission values.</span></span>

## <a name="result"></a><span data-ttu-id="290c0-105">結果</span><span class="sxs-lookup"><span data-stu-id="290c0-105">Result</span></span>

<span data-ttu-id="290c0-106">ICE55 會在 [LockPermissions 資料表](lockpermissions-table.md) 中所列的 LockObject 不存在或許可權資料行中未指定許可權層級時，張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="290c0-106">ICE55 post an error if a LockObject listed in the [LockPermissions table](lockpermissions-table.md) does not exist or if no privilege level is specified in the Permission column.</span></span>

## <a name="example"></a><span data-ttu-id="290c0-107">範例</span><span class="sxs-lookup"><span data-stu-id="290c0-107">Example</span></span>

<span data-ttu-id="290c0-108">ICE55 會報告範例的下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="290c0-108">ICE55 would report the following errors for the example.</span></span>

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

<span data-ttu-id="290c0-109">[LockPermissions 資料表](lockpermissions-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="290c0-109">[LockPermissions Table](lockpermissions-table.md) (partial)</span></span>



| <span data-ttu-id="290c0-110">LockObject</span><span class="sxs-lookup"><span data-stu-id="290c0-110">LockObject</span></span> | <span data-ttu-id="290c0-111">資料表</span><span class="sxs-lookup"><span data-stu-id="290c0-111">Table</span></span> | <span data-ttu-id="290c0-112">網域</span><span class="sxs-lookup"><span data-stu-id="290c0-112">Domain</span></span> | <span data-ttu-id="290c0-113">User</span><span class="sxs-lookup"><span data-stu-id="290c0-113">User</span></span>  | <span data-ttu-id="290c0-114">權限</span><span class="sxs-lookup"><span data-stu-id="290c0-114">Permission</span></span> |
|------------|-------|--------|-------|------------|
| <span data-ttu-id="290c0-115">File1</span><span class="sxs-lookup"><span data-stu-id="290c0-115">File1</span></span>      | <span data-ttu-id="290c0-116">檔案</span><span class="sxs-lookup"><span data-stu-id="290c0-116">File</span></span>  |        | <span data-ttu-id="290c0-117">guest</span><span class="sxs-lookup"><span data-stu-id="290c0-117">guest</span></span> |            |
| <span data-ttu-id="290c0-118">File3</span><span class="sxs-lookup"><span data-stu-id="290c0-118">File3</span></span>      | <span data-ttu-id="290c0-119">檔案</span><span class="sxs-lookup"><span data-stu-id="290c0-119">File</span></span>  |        | <span data-ttu-id="290c0-120">guest</span><span class="sxs-lookup"><span data-stu-id="290c0-120">guest</span></span> | <span data-ttu-id="290c0-121">1</span><span class="sxs-lookup"><span data-stu-id="290c0-121">1</span></span>          |



 

<span data-ttu-id="290c0-122">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="290c0-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="290c0-123">檔案</span><span class="sxs-lookup"><span data-stu-id="290c0-123">File</span></span>  | <span data-ttu-id="290c0-124">版本</span><span class="sxs-lookup"><span data-stu-id="290c0-124">Version</span></span> | <span data-ttu-id="290c0-125">語言</span><span class="sxs-lookup"><span data-stu-id="290c0-125">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="290c0-126">File1</span><span class="sxs-lookup"><span data-stu-id="290c0-126">File1</span></span> | <span data-ttu-id="290c0-127">File2</span><span class="sxs-lookup"><span data-stu-id="290c0-127">File2</span></span>   |          |
| <span data-ttu-id="290c0-128">File2</span><span class="sxs-lookup"><span data-stu-id="290c0-128">File2</span></span> | <span data-ttu-id="290c0-129">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="290c0-129">1.0.0.0</span></span> | <span data-ttu-id="290c0-130">1033</span><span class="sxs-lookup"><span data-stu-id="290c0-130">1033</span></span>     |



 

<span data-ttu-id="290c0-131">物件 File1 在許可權資料行中具有 null。</span><span class="sxs-lookup"><span data-stu-id="290c0-131">The object File1 has a null in the Permission column.</span></span> <span data-ttu-id="290c0-132">每個資料列都必須有 [許可權] 資料行中的值。</span><span class="sxs-lookup"><span data-stu-id="290c0-132">Each row must have a value in the Permissions column.</span></span> <span data-ttu-id="290c0-133">若要修正這個錯誤，請在此資料行中指定數值。</span><span class="sxs-lookup"><span data-stu-id="290c0-133">To fix this error specify a numeric value in this column.</span></span> <span data-ttu-id="290c0-134">如果這個物件不需要任何許可權，您應該移除該資料列。</span><span class="sxs-lookup"><span data-stu-id="290c0-134">If no privileges are needed for this object then you should remove the row.</span></span>

<span data-ttu-id="290c0-135">LockPermissions 資料表中所述的物件 File3 不會列在 File 資料表中。</span><span class="sxs-lookup"><span data-stu-id="290c0-135">The object File3 described in the LockPermissions table is not listed in the File table.</span></span> <span data-ttu-id="290c0-136">若要修正這個錯誤，請參考有效的物件。</span><span class="sxs-lookup"><span data-stu-id="290c0-136">To fix this error refer to a valid object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="290c0-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="290c0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="290c0-138">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="290c0-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



