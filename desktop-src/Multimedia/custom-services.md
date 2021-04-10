---
title: 自訂服務
description: 自訂服務
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- 多媒體檔案 i/o，自訂服務
- 檔案 i/o，自訂服務
- 輸入和輸出 (i/o) ，自訂服務
- I/o (輸入和輸出) ，自訂服務
- 自訂 i/o
- mmioInstallIOProc 函式
- mmioOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023429"
---
# <a name="custom-services"></a><span data-ttu-id="152ac-110">自訂服務</span><span class="sxs-lookup"><span data-stu-id="152ac-110">Custom Services</span></span>

<span data-ttu-id="152ac-111">多媒體檔案 i/o 服務使用 i/o 程式來處理與讀取和寫入不同類型的儲存系統（例如檔案保存系統和資料庫儲存系統）相關聯的實體輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="152ac-111">Multimedia file I/O services use I/O procedures to handle the physical input and output associated with reading and writing to different types of storage systems, such as file-archival systems and database-storage systems.</span></span> <span data-ttu-id="152ac-112">預先定義的 i/o 程式存在於標準檔案系統和記憶體檔案中，但是您可以使用 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) 函式提供自訂的 i/o 程式來存取唯一的儲存系統。</span><span class="sxs-lookup"><span data-stu-id="152ac-112">Predefined I/O procedures exist for the standard file systems and for memory files, but you can supply a custom I/O procedure for accessing a unique storage system by using the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function.</span></span>

<span data-ttu-id="152ac-113">若要使用自訂的 i/o 程式來開啟檔案，請使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函數。</span><span class="sxs-lookup"><span data-stu-id="152ac-113">To open a file by using a custom I/O procedure, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="152ac-114">在檔案名中包含加號 (+) 或 CFSEPCHAR 常數，以將實體檔案名與您想要開啟之檔案的專案名稱分開。</span><span class="sxs-lookup"><span data-stu-id="152ac-114">Include a plus sign (+) or the CFSEPCHAR constant in the filename to separate the name of the physical file from the name of the element of the file you want to open.</span></span> <span data-ttu-id="152ac-115">下列範例會從名為 FILENAME 的檔案開啟名為 "element" 的檔案元素。弧：</span><span class="sxs-lookup"><span data-stu-id="152ac-115">The following example opens a file element named "element" from a file named FILENAME.ARC:</span></span>


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



<span data-ttu-id="152ac-116">當檔案 i/o 管理員遇到檔案名的加號時，它會檢查副檔名，以決定要與檔案相關聯的 i/o 程式。</span><span class="sxs-lookup"><span data-stu-id="152ac-116">When the file I/O manager encounters a plus sign in a filename, it examines the filename extension to determine which I/O procedure to associate with the file.</span></span> <span data-ttu-id="152ac-117">在上述範例中，file i/o 管理員會嘗試使用與相關聯的 i/o 程式。ARC 副檔名;這個 i/o 程式會使用 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)進行安裝。</span><span class="sxs-lookup"><span data-stu-id="152ac-117">In the previous example, the file I/O manager would attempt to use the I/O procedure associated with the .ARC filename extension; this I/O procedure would have been installed by using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span></span> <span data-ttu-id="152ac-118">如果未安裝任何 i/o 程式， [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="152ac-118">If no I/O procedure is installed, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) returns an error.</span></span>

<span data-ttu-id="152ac-119">I/o 程式必須回應下列訊息：</span><span class="sxs-lookup"><span data-stu-id="152ac-119">I/O procedures must respond to the following messages:</span></span>

-   [<span data-ttu-id="152ac-120">**MMIOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="152ac-120">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="152ac-121">**MMIOM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="152ac-121">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="152ac-122">**MMIOM \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="152ac-122">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="152ac-123">**MMIOM \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="152ac-123">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="152ac-124">**MMIOM \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="152ac-124">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="152ac-125">**MMIOM \_ 重新命名**</span><span class="sxs-lookup"><span data-stu-id="152ac-125">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="152ac-126">**MMIOM \_ WRITEFLUSH**</span><span class="sxs-lookup"><span data-stu-id="152ac-126">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)

<span data-ttu-id="152ac-127">您也可以使用 [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) 函式來建立自訂訊息，並將其傳送至您的 i/o 程式。</span><span class="sxs-lookup"><span data-stu-id="152ac-127">You can also create custom messages and send them to your I/O procedure by using the [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) function.</span></span> <span data-ttu-id="152ac-128">如果您定義自己的訊息，請確定其定義于或高於 MMIOM 使用者常數所定義的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="152ac-128">If you define your own messages, make sure they are defined at or above the value defined by the MMIOM\_USER constant.</span></span>

<span data-ttu-id="152ac-129">除了處理訊息之外，i/o 程式還必須維護 **mmioOpen** 函式的 *lpmmioinfo* 參數所指向之 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構 (的 **lDiskOffset** 成員) 。</span><span class="sxs-lookup"><span data-stu-id="152ac-129">In addition to processing messages, an I/O procedure must maintain the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure (pointed to by the *lpmmioinfo* parameter of the **mmioOpen** function).</span></span> <span data-ttu-id="152ac-130">**LDiskOffset** 成員一律必須包含下一個 MMIOM \_ READ 或 MMIOM \_ 寫入訊息將存取之位置的檔案位移。</span><span class="sxs-lookup"><span data-stu-id="152ac-130">The **lDiskOffset** member must always contain the file offset to the location that the next MMIOM\_READ or MMIOM\_WRITE message will access.</span></span> <span data-ttu-id="152ac-131">位移是以位元組為單位來指定，且相對於檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="152ac-131">The offset is specified in bytes and is relative to the beginning of the file.</span></span> <span data-ttu-id="152ac-132">I/o 程式可以使用 **adwInfo** 成員來維護任何必要的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="152ac-132">The I/O procedure can use the **adwInfo** member to maintain any required state information.</span></span> <span data-ttu-id="152ac-133">I/o 程式不應該修改 **MMIOINFO** 結構中的任何其他成員。</span><span class="sxs-lookup"><span data-stu-id="152ac-133">The I/O procedure should not modify any other members in the **MMIOINFO** structure.</span></span>

 

 