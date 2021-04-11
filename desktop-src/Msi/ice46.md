---
description: ICE46 只會在一或多個字元的情況下，檢查條件中的自訂屬性、格式化的文字，以及與系統定義的屬性不同的其他位置。
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692791"
---
# <a name="ice46"></a><span data-ttu-id="9c0b1-103">ICE46</span><span class="sxs-lookup"><span data-stu-id="9c0b1-103">ICE46</span></span>

<span data-ttu-id="9c0b1-104">ICE46 只會在一或多個字元的情況下，檢查條件中的自訂屬性、格式化的文字，以及與系統定義的屬性不同的其他位置。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-104">ICE46 checks for custom properties in conditions, formatted text, and other locations that differ from a system defined property only by the case of one or more characters.</span></span>

## <a name="result"></a><span data-ttu-id="9c0b1-105">結果</span><span class="sxs-lookup"><span data-stu-id="9c0b1-105">Result</span></span>

<span data-ttu-id="9c0b1-106">如果條件中有自訂屬性、格式化的文字，以及在一或多個字元的情況下與系統定義的屬性不同的其他位置，ICE46 會張貼參考用訊息。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-106">ICE46 posts an informational message if there is a custom property in a condition, formatted text, and other location that differs from a system defined properties only in the case of one or more characters.</span></span>

## <a name="example"></a><span data-ttu-id="9c0b1-107">範例</span><span class="sxs-lookup"><span data-stu-id="9c0b1-107">Example</span></span>

<span data-ttu-id="9c0b1-108">ICE46 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-108">ICE46 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="9c0b1-109">ICE46 錯誤</span><span class="sxs-lookup"><span data-stu-id="9c0b1-109">ICE46 error</span></span>                                                                                                                                            | <span data-ttu-id="9c0b1-110">Description</span><span class="sxs-lookup"><span data-stu-id="9c0b1-110">Description</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0b1-111">在屬性資料表中定義的屬性 ReinstallMode，與另一個已定義的屬性不同，只有大小寫。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-111">Property ReinstallMode defined in property table differs from another defined property only by case.</span></span>                                                   | <span data-ttu-id="9c0b1-112">系統定義的屬性名稱 **REINSTALLMODE** 與自訂屬性的大小寫不同。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-112">The system defined property name **REINSTALLMODE** differs from the custom property by case only.</span></span> <span data-ttu-id="9c0b1-113">屬性會區分大小寫，因此自訂屬性與系統屬性不同。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-113">Properties are case sensitive, so custom property is not the same as the system property.</span></span> <span data-ttu-id="9c0b1-114">這是錯誤的常見原因。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-114">This is a common cause of errors.</span></span> |
| <span data-ttu-id="9c0b1-115">在資料行 ' InstallExecuteSequence ' 中參考的屬性 ' Myproperty '。資料列 ' InstallFinalize ' 的條件 ' 與已定義的屬性（僅限大小寫）不同。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-115">Property 'Myproperty' referenced in column 'InstallExecuteSequence'.'Condition' of row 'InstallFinalize' differs from a defined property by case only.</span></span> | <span data-ttu-id="9c0b1-116">屬性工作表定義了資料表 MyProperty，但是參考的屬性是 Myproperty。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-116">The property table defines the table MyProperty, but the referenced property is Myproperty.</span></span> <span data-ttu-id="9c0b1-117">屬性會區分大小寫，因此這兩個屬性不相同。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-117">Properties are case sensitive, so the two properties are NOT the same.</span></span> <span data-ttu-id="9c0b1-118">這是錯誤的常見原因。</span><span class="sxs-lookup"><span data-stu-id="9c0b1-118">This is a common cause of errors.</span></span>                          |



 

[<span data-ttu-id="9c0b1-119">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="9c0b1-119">Property Table</span></span>](property-table.md)



| <span data-ttu-id="9c0b1-120">屬性</span><span class="sxs-lookup"><span data-stu-id="9c0b1-120">Property</span></span>      | <span data-ttu-id="9c0b1-121">值</span><span class="sxs-lookup"><span data-stu-id="9c0b1-121">Value</span></span>   |
|---------------|---------|
| <span data-ttu-id="9c0b1-122">ReinstallMode</span><span class="sxs-lookup"><span data-stu-id="9c0b1-122">ReinstallMode</span></span> | <span data-ttu-id="9c0b1-123">omus reinstall</span><span class="sxs-lookup"><span data-stu-id="9c0b1-123">omus</span></span>    |
| <span data-ttu-id="9c0b1-124">MyProperty</span><span class="sxs-lookup"><span data-stu-id="9c0b1-124">MyProperty</span></span>    | <span data-ttu-id="9c0b1-125">值</span><span class="sxs-lookup"><span data-stu-id="9c0b1-125">a value</span></span> |



 

<span data-ttu-id="9c0b1-126">[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="9c0b1-126">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="9c0b1-127">動作</span><span class="sxs-lookup"><span data-stu-id="9c0b1-127">Action</span></span>          | <span data-ttu-id="9c0b1-128">條件</span><span class="sxs-lookup"><span data-stu-id="9c0b1-128">Condition</span></span>  |
|-----------------|------------|
| <span data-ttu-id="9c0b1-129">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="9c0b1-129">InstallFinalize</span></span> | <span data-ttu-id="9c0b1-130">Myproperty</span><span class="sxs-lookup"><span data-stu-id="9c0b1-130">Myproperty</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9c0b1-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c0b1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c0b1-132">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="9c0b1-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



