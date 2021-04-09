---
description: ICE66 會使用資料庫中的資料表，來判斷您的資料庫應該使用哪一個架構。
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691184"
---
# <a name="ice66"></a><span data-ttu-id="e8b10-103">ICE66</span><span class="sxs-lookup"><span data-stu-id="e8b10-103">ICE66</span></span>

<span data-ttu-id="e8b10-104">ICE66 會使用資料庫中的資料表，來判斷您的資料庫應該使用哪一個架構。</span><span class="sxs-lookup"><span data-stu-id="e8b10-104">ICE66 uses the tables in the database to determine which schema your database should use.</span></span>

<span data-ttu-id="e8b10-105">只有當封裝安裝在具有目前 Windows Installer 版本的系統上時，才能使用某些功能。</span><span class="sxs-lookup"><span data-stu-id="e8b10-105">Some functionality may only be available if the package is installed on a system with a current Windows Installer version.</span></span>

## <a name="result"></a><span data-ttu-id="e8b10-106">結果</span><span class="sxs-lookup"><span data-stu-id="e8b10-106">Result</span></span>

<span data-ttu-id="e8b10-107">如果您的資料庫使用錯誤的架構，ICE66 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="e8b10-107">ICE66 posts a warning if your database is using the wrong schema.</span></span>

## <a name="example"></a><span data-ttu-id="e8b10-108">範例</span><span class="sxs-lookup"><span data-stu-id="e8b10-108">Example</span></span>

<span data-ttu-id="e8b10-109">ICE66 會針對所顯示的範例報告下列警告。</span><span class="sxs-lookup"><span data-stu-id="e8b10-109">ICE66 reports the following warning for the example shown.</span></span>

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

<span data-ttu-id="e8b10-110">如果您想要使用目前的 Windows Installer 版本安裝封裝，可以忽略這個警告。</span><span class="sxs-lookup"><span data-stu-id="e8b10-110">This warning can be ignored if you want your package to be installed using a current Windows Installer version.</span></span> <span data-ttu-id="e8b10-111">例如，如果您只想要在2.0 版或更新版本上安裝套件，請將您的封裝架構 (PID \_ PAGECOUNT) 變更為200。</span><span class="sxs-lookup"><span data-stu-id="e8b10-111">For example, if you want your package to be installable only on version 2.0 or later, change your package schema (PID\_PAGECOUNT) to 200.</span></span>

[<span data-ttu-id="e8b10-112">IsolatedComponent 資料表</span><span class="sxs-lookup"><span data-stu-id="e8b10-112">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="e8b10-113">元件 \_ 共用</span><span class="sxs-lookup"><span data-stu-id="e8b10-113">Component\_Shared</span></span> | <span data-ttu-id="e8b10-114">元件 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="e8b10-114">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="e8b10-115">Component1</span><span class="sxs-lookup"><span data-stu-id="e8b10-115">Component1</span></span>        | <span data-ttu-id="e8b10-116">Component2</span><span class="sxs-lookup"><span data-stu-id="e8b10-116">Component2</span></span>             |



 

[<span data-ttu-id="e8b10-117">摘要資訊串流</span><span class="sxs-lookup"><span data-stu-id="e8b10-117">Summary Information Stream</span></span>](summary-information-stream.md)



| <span data-ttu-id="e8b10-118">PIDt</span><span class="sxs-lookup"><span data-stu-id="e8b10-118">PIDt</span></span>           | <span data-ttu-id="e8b10-119">值</span><span class="sxs-lookup"><span data-stu-id="e8b10-119">Value</span></span> |
|----------------|-------|
| <span data-ttu-id="e8b10-120">PID \_ PAGECOUNT</span><span class="sxs-lookup"><span data-stu-id="e8b10-120">PID\_PAGECOUNT</span></span> | <span data-ttu-id="e8b10-121">100</span><span class="sxs-lookup"><span data-stu-id="e8b10-121">100</span></span>   |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="e8b10-122">執行期間所使用的資料表：</span><span class="sxs-lookup"><span data-stu-id="e8b10-122">Table used during execution:</span></span>

[<span data-ttu-id="e8b10-123">\_Columns 資料表</span><span class="sxs-lookup"><span data-stu-id="e8b10-123">\_Columns table</span></span>](-columns-table.md)

## <a name="related-topics"></a><span data-ttu-id="e8b10-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8b10-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8b10-125">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="e8b10-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



