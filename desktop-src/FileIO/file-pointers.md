---
description: 檔案指標是64位的位移值，可指定要讀取的下一個位元組，或要接收下一個寫入位元組的位置。
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: 檔案指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192124"
---
# <a name="file-pointers"></a><span data-ttu-id="2fcf3-103">檔案指標</span><span class="sxs-lookup"><span data-stu-id="2fcf3-103">File Pointers</span></span>

<span data-ttu-id="2fcf3-104">開啟檔案時，Windows 會將檔案 *指標* 與預設資料流程產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-104">When a file is opened, Windows associates a *file pointer* with the default stream.</span></span> <span data-ttu-id="2fcf3-105">這個檔案指標是64位的位移值，可指定要讀取的下一個位元組，或要接收下一個寫入位元組的位置。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-105">This file pointer is a 64-bit offset value that specifies the next byte to be read or the location to receive the next byte written.</span></span> <span data-ttu-id="2fcf3-106">每次開啟檔案時，系統會將檔案指標放在檔案的開頭，也就是位移零。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-106">Each time a file is opened, the system places the file pointer at the beginning of the file, which is offset zero.</span></span> <span data-ttu-id="2fcf3-107">每個讀取和寫入作業都會依所讀取和寫入的位元組數目來推進檔案指標。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-107">Each read and write operation advances the file pointer by the number of bytes being read and written.</span></span> <span data-ttu-id="2fcf3-108">例如，如果檔案指標位於檔案的開頭，且要求了5個位元組的讀取作業，則檔案指標會緊接在讀取作業之後的位移5。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-108">For example, if the file pointer is at the beginning of the file and a read operation of 5 bytes is requested, the file pointer will be located at offset 5 immediately after the read operation.</span></span> <span data-ttu-id="2fcf3-109">當讀取或寫入每個位元組時，系統會將檔案指標前進。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-109">As each byte is read or written, the system advances the file pointer.</span></span> <span data-ttu-id="2fcf3-110">藉由呼叫 [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) 函式，也可以重新置放檔案指標。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-110">The file pointer can also be repositioned by calling the [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function.</span></span>

<span data-ttu-id="2fcf3-111">當檔案指標到達檔案結尾，而應用程式嘗試從檔案讀取時，不會發生任何錯誤，但不會讀取任何位元組。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-111">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="2fcf3-112">因此，讀取零位元組而不發生錯誤，表示應用程式已到達檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-112">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="2fcf3-113">寫入零位元組不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-113">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="2fcf3-114">應用程式可以使用 [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) 函數來截斷或擴充檔案。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-114">An application can truncate or extend a file by using the [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) function.</span></span> <span data-ttu-id="2fcf3-115">此函式會將檔案結尾設定為檔案指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="2fcf3-115">This function sets the end of file to the current position of the file pointer.</span></span>

 

 



