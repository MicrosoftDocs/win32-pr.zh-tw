---
description: 應用程式可以使用 LZOpenFile、LZCopy 和 LZClose 函式，將多個檔案解壓縮。
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: 解壓縮多個檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992018"
---
# <a name="decompressing-multiple-files"></a><span data-ttu-id="3b0b8-103">解壓縮多個檔案</span><span class="sxs-lookup"><span data-stu-id="3b0b8-103">Decompressing Multiple Files</span></span>

<span data-ttu-id="3b0b8-104">應用程式可以藉由執行下列工作來解壓縮多個檔案：</span><span class="sxs-lookup"><span data-stu-id="3b0b8-104">An application can decompress multiple files by performing the following tasks:</span></span>

1.  <span data-ttu-id="3b0b8-105">藉由呼叫 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) 函數來開啟原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="3b0b8-105">Open the source files by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="3b0b8-106">藉由呼叫 [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)來開啟目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="3b0b8-106">Open the destination files by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="3b0b8-107">藉由呼叫 [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) 函式，將原始程式檔複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="3b0b8-107">Copy the source files to the destination files by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function.</span></span>
4.  <span data-ttu-id="3b0b8-108">藉由呼叫 [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) 函數來關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="3b0b8-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



