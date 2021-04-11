---
description: GetFileSize 函式會捕獲檔案的大小。
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: 判斷檔案的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944375"
---
# <a name="determining-the-size-of-a-file"></a><span data-ttu-id="70553-103">判斷檔案的大小</span><span class="sxs-lookup"><span data-stu-id="70553-103">Determining the Size of a File</span></span>

<span data-ttu-id="70553-104">[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)函式會捕獲檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="70553-104">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span>

<span data-ttu-id="70553-105">因為 NTFS 檔案系統的檔案允許在檔案內進行多個資料流程，所以您撰寫來存取檔案的任何應用程式，都必須考慮檔案建立者可以在檔案中包含多個資料流程的可能性。</span><span class="sxs-lookup"><span data-stu-id="70553-105">Because the NTFS file system implementation of files allows for multiple streams within a file, any application you write that accesses files must account for the possibility that the creator of the file can include multiple streams in the file.</span></span> <span data-ttu-id="70553-106">如果檔案中沒有檢查多個資料流程，應用程式可能會低估檔案的總大小，還有其他錯誤。</span><span class="sxs-lookup"><span data-stu-id="70553-106">If multiple streams are not checked for in a file, the application can underestimate the total size of the file, among other errors.</span></span>

 

 



