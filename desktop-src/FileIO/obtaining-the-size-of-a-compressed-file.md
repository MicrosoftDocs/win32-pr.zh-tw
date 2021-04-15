---
description: 若要取得壓縮的檔案大小，請使用 GetCompressedFileSize 函數。
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: 取得壓縮檔案的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4954a53184e55341838fef7cd70f01639f13bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512025"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a><span data-ttu-id="ca99a-103">取得壓縮檔案的大小</span><span class="sxs-lookup"><span data-stu-id="ca99a-103">Obtaining the Size of a Compressed File</span></span>

<span data-ttu-id="ca99a-104">您可以使用 [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) 函式來取得檔案的壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="ca99a-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the compressed size of a file.</span></span> <span data-ttu-id="ca99a-105">如果檔案已壓縮，壓縮的大小將會小於其未壓縮的大小。</span><span class="sxs-lookup"><span data-stu-id="ca99a-105">If the file is compressed, its compressed size will be less than its uncompressed size.</span></span> <span data-ttu-id="ca99a-106">您可以使用 [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) 函數來判斷檔案的未壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="ca99a-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the uncompressed size of a file.</span></span>

 

 



