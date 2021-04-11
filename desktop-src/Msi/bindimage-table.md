---
description: BindImage 資料表包含每個可執行檔或 DLL 的相關資訊，這些可執行檔或 DLL 必須系結至它所匯入的 Dll。
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: BindImage 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943998"
---
# <a name="bindimage-table"></a><span data-ttu-id="6bbb7-103">BindImage 資料表</span><span class="sxs-lookup"><span data-stu-id="6bbb7-103">BindImage Table</span></span>

<span data-ttu-id="6bbb7-104">BindImage 資料表包含每個可執行檔或 DLL 的相關資訊，這些可執行檔或 DLL 必須系結至它所匯入的 Dll。</span><span class="sxs-lookup"><span data-stu-id="6bbb7-104">The BindImage table contains information about each executable or DLL that needs to be bound to the DLLs imported by it.</span></span>

<span data-ttu-id="6bbb7-105">BindImage 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="6bbb7-105">The BindImage table has the following columns.</span></span>



| <span data-ttu-id="6bbb7-106">Column</span><span class="sxs-lookup"><span data-stu-id="6bbb7-106">Column</span></span> | <span data-ttu-id="6bbb7-107">類型</span><span class="sxs-lookup"><span data-stu-id="6bbb7-107">Type</span></span>                         | <span data-ttu-id="6bbb7-108">答案</span><span class="sxs-lookup"><span data-stu-id="6bbb7-108">Key</span></span> | <span data-ttu-id="6bbb7-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="6bbb7-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="6bbb7-110">檔案\_</span><span class="sxs-lookup"><span data-stu-id="6bbb7-110">File\_</span></span> | [<span data-ttu-id="6bbb7-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="6bbb7-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="6bbb7-112">Y</span><span class="sxs-lookup"><span data-stu-id="6bbb7-112">Y</span></span>   | <span data-ttu-id="6bbb7-113">N</span><span class="sxs-lookup"><span data-stu-id="6bbb7-113">N</span></span>        |
| <span data-ttu-id="6bbb7-114">路徑</span><span class="sxs-lookup"><span data-stu-id="6bbb7-114">Path</span></span>   | [<span data-ttu-id="6bbb7-115">路徑</span><span class="sxs-lookup"><span data-stu-id="6bbb7-115">Paths</span></span>](paths.md)           | <span data-ttu-id="6bbb7-116">N</span><span class="sxs-lookup"><span data-stu-id="6bbb7-116">N</span></span>   | <span data-ttu-id="6bbb7-117">Y</span><span class="sxs-lookup"><span data-stu-id="6bbb7-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6bbb7-118">資料行</span><span class="sxs-lookup"><span data-stu-id="6bbb7-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6bbb7-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="6bbb7-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="6bbb7-120">檔案 [資料表](file-table.md)中第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6bbb7-120">An external key to column one of the [File table](file-table.md).</span></span> <span data-ttu-id="6bbb7-121">這必須是可執行檔或 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="6bbb7-121">This must be an executable file or a DLL file.</span></span>

</dd> <dt>

<span data-ttu-id="6bbb7-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>路徑</span><span class="sxs-lookup"><span data-stu-id="6bbb7-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="6bbb7-123">以分號分隔的路徑清單，表示要搜尋以尋找匯入之 Dll 的路徑。</span><span class="sxs-lookup"><span data-stu-id="6bbb7-123">A list of paths, separated by semicolons, that represent the paths to be searched to find the imported DLLs.</span></span> <span data-ttu-id="6bbb7-124">清單通常是屬性清單，其中每個屬性都以方括弧括住 (\[ \]) 中。</span><span class="sxs-lookup"><span data-stu-id="6bbb7-124">The list is usually a list of properties, with each property enclosed inside square brackets (\[ \]) .</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bbb7-125">備註</span><span class="sxs-lookup"><span data-stu-id="6bbb7-125">Remarks</span></span>

<span data-ttu-id="6bbb7-126">安裝程式會計算從所有 Dll 匯入之每個函式的虛擬位址，然後計算的虛擬位址會儲存在匯入映射的匯入位址表中 (IAT) 。</span><span class="sxs-lookup"><span data-stu-id="6bbb7-126">The installer computes the virtual address of each function that is imported from all DLLs, and the computed virtual address is then saved in the importing image's Import Address Table (IAT).</span></span>

<span data-ttu-id="6bbb7-127">當 [BindImage 動作](bindimage-action.md) 執行時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="6bbb7-127">This table is referred to when the [BindImage action](bindimage-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="6bbb7-128">驗證</span><span class="sxs-lookup"><span data-stu-id="6bbb7-128">Validation</span></span>

<dl>

[<span data-ttu-id="6bbb7-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="6bbb7-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6bbb7-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="6bbb7-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6bbb7-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="6bbb7-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="6bbb7-132">ICE46</span><span class="sxs-lookup"><span data-stu-id="6bbb7-132">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="6bbb7-133">ICE76</span><span class="sxs-lookup"><span data-stu-id="6bbb7-133">ICE76</span></span>](ice76.md)  
</dl>

 

 



