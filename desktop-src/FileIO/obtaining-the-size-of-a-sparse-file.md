---
description: 使用 GetCompressedFileSize 或 GetFileSize 函式，取得設定檔案大小或檔案的大小總計。
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: 取得稀疏檔案的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848259"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a><span data-ttu-id="cb173-103">取得稀疏檔案的大小</span><span class="sxs-lookup"><span data-stu-id="cb173-103">Obtaining the Size of a Sparse File</span></span>

<span data-ttu-id="cb173-104">您可以使用 [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) 函式來取得在磁片上配置給稀疏檔案的實際大小。</span><span class="sxs-lookup"><span data-stu-id="cb173-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the actual size allocated on disk for a sparse file.</span></span> <span data-ttu-id="cb173-105">此總計不包含已解除配置的區域大小，因為它們已填入零。</span><span class="sxs-lookup"><span data-stu-id="cb173-105">This total does not include the size of the regions which were deallocated because they were filled with zeros.</span></span> <span data-ttu-id="cb173-106">您可以使用 [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) 函式來判斷檔案的大小總計，包括已解除配置之稀疏區域的大小。</span><span class="sxs-lookup"><span data-stu-id="cb173-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the total size of a file, including the size of the sparse regions that were deallocated.</span></span>

 

 



