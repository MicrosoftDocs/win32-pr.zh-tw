---
description: Windows 使用檔案指標來追蹤讀取或寫入的位元組。
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: 放置檔案指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985656"
---
# <a name="positioning-a-file-pointer"></a><span data-ttu-id="79d93-103">放置檔案指標</span><span class="sxs-lookup"><span data-stu-id="79d93-103">Positioning a File Pointer</span></span>

<span data-ttu-id="79d93-104">當應用程式第一次呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 開啟檔案時，Windows 會將檔案 [指標](file-pointers.md) 放在檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="79d93-104">When an application calls [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open a file for the first time, Windows places the [file pointer](file-pointers.md) at the beginning of the file.</span></span> <span data-ttu-id="79d93-105">當位元組讀取或寫入至檔案時，Windows 會將檔案指標往上讀取或寫入的位元組數目前移。</span><span class="sxs-lookup"><span data-stu-id="79d93-105">As bytes are read from or written to the file, Windows advances the file pointer the number of bytes read or written.</span></span>

<span data-ttu-id="79d93-106">應用程式可以藉由呼叫 [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)，將檔案指標定位至指定的位移。</span><span class="sxs-lookup"><span data-stu-id="79d93-106">An application can position the file pointer to a specified offset by calling [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span></span>

<span data-ttu-id="79d93-107">[**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)函式也可以用來查詢目前的檔案指標位置，方法是指定檔案 **\_ 目前** 的移動方法和距離零的距離。</span><span class="sxs-lookup"><span data-stu-id="79d93-107">The [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function can also be used to query the current file pointer position by specifying a move method of **FILE\_CURRENT** and a distance of zero.</span></span>

 

 



