---
description: 應用程式可以使用 FindFirstFile、FindFirstFileEx、FindNextFile 和 FindClose 函數，在目前的目錄中搜尋符合指定模式的所有檔案名。
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: 搜尋一個或多個檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972266"
---
# <a name="searching-for-one-or-more-files"></a><span data-ttu-id="0f7bb-103">搜尋一個或多個檔案</span><span class="sxs-lookup"><span data-stu-id="0f7bb-103">Searching for One or More Files</span></span>

<span data-ttu-id="0f7bb-104">應用程式可以使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)、 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)和 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數，在目前的目錄中搜尋符合指定模式的所有檔案名。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-104">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span> <span data-ttu-id="0f7bb-105">模式必須是有效的檔案名，而且可以包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-105">The pattern must be a valid file name and can include wildcard characters.</span></span>

<span data-ttu-id="0f7bb-106">[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)和 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)函式會建立 **FindFirstFileEx** 用來搜尋具有相同模式之其他檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-106">The [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) functions create handles that **FindFirstFileEx** uses to search for other files with the same pattern.</span></span> <span data-ttu-id="0f7bb-107">所有函式都會傳回所找到檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-107">All functions return information about the file that was found.</span></span> <span data-ttu-id="0f7bb-108">此資訊包含檔案名、大小、屬性和時間。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-108">This information includes the file name, size, attributes, and time.</span></span>

<span data-ttu-id="0f7bb-109">[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)函式也可讓應用程式根據其他搜尋準則來搜尋檔案。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-109">The [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) function also allows an application to search for files based on additional search criteria.</span></span> <span data-ttu-id="0f7bb-110">此函式可以限制搜尋裝置名稱或目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-110">The function can limit searches to device names or directory names.</span></span>

<span data-ttu-id="0f7bb-111">[**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose)函式會終結 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)和 [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-111">The [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function destroys handles created by [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span></span>

<span data-ttu-id="0f7bb-112">應用程式可以使用 [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) 函數，在特定路徑上搜尋單一檔案。</span><span class="sxs-lookup"><span data-stu-id="0f7bb-112">An application can search for a single file on a specific path by using the [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) function.</span></span>

 

 
