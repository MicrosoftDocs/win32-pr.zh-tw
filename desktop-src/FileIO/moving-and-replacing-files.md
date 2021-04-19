---
description: 使用 CopyFileEx、CreateFile、Replacefile 和 MoveFileEx 函數移動和取代檔案的考慮。
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: 移動和取代檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7f08d2bd8d07645076620e839d7d12f5969502
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "106988531"
---
# <a name="moving-and-replacing-files"></a><span data-ttu-id="f562a-103">移動和取代檔案</span><span class="sxs-lookup"><span data-stu-id="f562a-103">Moving and Replacing Files</span></span>

<span data-ttu-id="f562a-104">在可以執行複製作業之前，必須先關閉或開啟來源檔案以進行讀取。</span><span class="sxs-lookup"><span data-stu-id="f562a-104">Before a copy operation can be performed, the source file must be closed or opened only for reading.</span></span> <span data-ttu-id="f562a-105">沒有任何執行緒可以開啟來源檔案進行寫入。</span><span class="sxs-lookup"><span data-stu-id="f562a-105">No thread can have the the source file opened for writing.</span></span> <span data-ttu-id="f562a-106">若要將現有的檔案複製到新的檔案，請使用 [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) 或 [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="f562a-106">To copy an existing file to a new one, use the [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) or [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function.</span></span> <span data-ttu-id="f562a-107">如果目的地檔案已經存在，應用程式可以指定 **CopyFile** 和 **CopyFileEx** 是否失敗。</span><span class="sxs-lookup"><span data-stu-id="f562a-107">Applications can specify whether **CopyFile** and **CopyFileEx** fail if the destination file already exists.</span></span> <span data-ttu-id="f562a-108">如果目的地檔案存在且為開啟狀態，則必須已使用適用的共用許可權開啟該檔案。</span><span class="sxs-lookup"><span data-stu-id="f562a-108">If the destination file does exist and is open, it must have been opened with applicable sharing permissions.</span></span> <span data-ttu-id="f562a-109">如需詳細資訊，請參閱 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)。</span><span class="sxs-lookup"><span data-stu-id="f562a-109">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span>

<span data-ttu-id="f562a-110">[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)函式也可讓應用程式指定回呼函式的位址 (請參閱 [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)) ，每次複製檔案的另一個部分時，就會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="f562a-110">The [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function also allows an application to specify the address of a callback function (see [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)) that is called each time another portion of the file has been copied.</span></span> <span data-ttu-id="f562a-111">應用程式可以使用這項資訊來顯示指標，顯示覆制的總位元組數（以總檔案大小的百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="f562a-111">The application can use this information to display an indicator that shows the total number of bytes copied as a percent of the total file size.</span></span>

<span data-ttu-id="f562a-112">[**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)函式會以另一個檔案取代一個檔案，選項是建立原始檔案的備份副本。</span><span class="sxs-lookup"><span data-stu-id="f562a-112">The [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) function replaces one file with another file, with the option of creating a backup copy of the original file.</span></span> <span data-ttu-id="f562a-113">函式會保留原始檔案的屬性，例如其建立時間、Acl 和加密屬性。</span><span class="sxs-lookup"><span data-stu-id="f562a-113">The function preserves attributes of the original file, such as its creation time, ACLs, and encryption attribute.</span></span>

<span data-ttu-id="f562a-114">您也必須先關閉檔案，應用程式才能將它移動。</span><span class="sxs-lookup"><span data-stu-id="f562a-114">A file must also be closed before an application can move it.</span></span> <span data-ttu-id="f562a-115">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)和 [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)函式會將現有的檔案複製到新位置，並刪除原始的檔案。</span><span class="sxs-lookup"><span data-stu-id="f562a-115">The [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) and [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) functions copy an existing file to a new location and deletes the original.</span></span>

<span data-ttu-id="f562a-116">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)函式也允許應用程式指定移動檔案的方式。</span><span class="sxs-lookup"><span data-stu-id="f562a-116">The [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) function also allows an application to specify how to move the file.</span></span> <span data-ttu-id="f562a-117">此函數可以取代現有的檔案、跨磁片區移動檔案，以及延遲移動檔案，直到作業系統重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="f562a-117">The function can replace an existing file, move a file across volumes, and delay moving the file until the operating system is restarted.</span></span>

 

 



