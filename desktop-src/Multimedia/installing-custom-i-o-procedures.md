---
title: 安裝自訂 i/o 程式
description: 安裝自訂 i/o 程式
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- 多媒體檔案 i/o，自訂程式
- 檔案 i/o，自訂程式
- 輸入和輸出 (i/o) ，自訂程式
- I/o (輸入和輸出) ，自訂程式
- 安裝自訂 i/o 程式
- 自訂 i/o
- mmioInstallIOProc 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375296"
---
# <a name="installing-custom-io-procedures"></a><span data-ttu-id="60e35-110">安裝自訂 i/o 程式</span><span class="sxs-lookup"><span data-stu-id="60e35-110">Installing Custom I/O Procedures</span></span>

<span data-ttu-id="60e35-111">若要安裝與相關聯的 i/o 程式。ARC 副檔名，請使用 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) 函數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="60e35-111">To install an I/O procedure associated with the .ARC filename extension, use the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function as follows:</span></span>


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



<span data-ttu-id="60e35-112">當您使用 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)安裝 i/o 程式時，程式會保持安裝，直到您將它移除為止。</span><span class="sxs-lookup"><span data-stu-id="60e35-112">When you install an I/O procedure using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), the procedure remains installed until you remove it.</span></span> <span data-ttu-id="60e35-113">只要檔案具有適當的副檔名，i/o 程式就會用於您開啟的任何檔案。</span><span class="sxs-lookup"><span data-stu-id="60e35-113">The I/O procedure is used for any file you open as long as the file has the appropriate filename extension.</span></span>

<span data-ttu-id="60e35-114">您也可以使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函數，暫時安裝 i/o 程式。</span><span class="sxs-lookup"><span data-stu-id="60e35-114">You can also temporarily install an I/O procedure by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="60e35-115">在此情況下，i/o 程式只適用于使用 **mmioOpen** 開啟的檔案，而且會在使用 [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) 函數關閉檔案時移除。</span><span class="sxs-lookup"><span data-stu-id="60e35-115">In this case, the I/O procedure is used only with a file opened by using **mmioOpen** and is removed when the file is closed by using the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function.</span></span> <span data-ttu-id="60e35-116">當您使用 **mmioOpen** 開啟檔案時，若要指定 i/o 程式，請使用 *Lpmmioinfo* 參數參考 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="60e35-116">To specify an I/O procedure when you open a file by using **mmioOpen**, use the *lpmmioinfo* parameter to reference an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure as follows:</span></span>

1.  <span data-ttu-id="60e35-117">將 **fccIOProc** 成員設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="60e35-117">Set the **fccIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="60e35-118">將 **pIOProc** 成員設定為 i/o 程式的程式實例位址。</span><span class="sxs-lookup"><span data-stu-id="60e35-118">Set the **pIOProc** member to the procedure-instance address of the I/O procedure.</span></span>
3.  <span data-ttu-id="60e35-119">除非您要開啟記憶體檔案，或直接讀取或寫入檔案 i/o 緩衝區) ，否則請將所有其他成員設定為零 (。</span><span class="sxs-lookup"><span data-stu-id="60e35-119">Set all other members to zero (unless you are opening a memory file, or directly reading or writing to the file I/O buffer).</span></span>

<span data-ttu-id="60e35-120">在結束您的應用程式之前，請務必移除您已安裝的所有 i/o 程式。</span><span class="sxs-lookup"><span data-stu-id="60e35-120">Be sure to remove any I/O procedures you have installed before you exit your application.</span></span>

 

 