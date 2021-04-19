---
description: 描述在一項作業中用來讀取或寫入非連續資料區塊的散佈集合配置。
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: 使用 Scatter-Gather 配置讀取或寫入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981019"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a><span data-ttu-id="1ac71-103">使用 Scatter-Gather 配置讀取或寫入檔案</span><span class="sxs-lookup"><span data-stu-id="1ac71-103">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>

<span data-ttu-id="1ac71-104">散佈收集配置會使用作業系統，在一個作業中傳遞多個離散的資料區塊 (例如，從檔案) 的資料庫記錄，到記憶體中的非連續緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1ac71-104">A scatter-gather scheme uses the operating system to deliver in one operation multiple discrete chunks of data (such as database records) from a file to separate, noncontiguous buffers in memory.</span></span> <span data-ttu-id="1ac71-105">散佈式收集配置也會在一項作業中從非連續的緩衝區寫入資料。</span><span class="sxs-lookup"><span data-stu-id="1ac71-105">A scatter-gather scheme also writes the data from noncontiguous buffers in one operation.</span></span>

<span data-ttu-id="1ac71-106">應用程式可以使用 [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) 和 [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) 函式來執行散佈集合配置。</span><span class="sxs-lookup"><span data-stu-id="1ac71-106">An application can implement a scatter-gather scheme by using the [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) functions.</span></span>

 

 



