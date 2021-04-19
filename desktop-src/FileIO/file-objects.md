---
description: 檔案物件可作為核心和使用者模式進程之間的邏輯介面，以及位於實體磁片上的檔案資料。
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: File 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e37793ad6c31ac86809047a3ec0d34afc3efc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971722"
---
# <a name="file-objects"></a><span data-ttu-id="b9ac6-103">File 物件</span><span class="sxs-lookup"><span data-stu-id="b9ac6-103">File Objects</span></span>

<span data-ttu-id="b9ac6-104">檔案 *物件* 可作為核心和使用者模式進程之間的邏輯介面，以及位於實體磁片上的檔案資料。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-104">*File objects* function as the logical interface between kernel and user-mode processes and the file data that resides on the physical disk.</span></span> <span data-ttu-id="b9ac6-105">File 物件包含寫入檔案的資料，以及下列一組核心維護的屬性。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-105">A file object contains both the data written to the file and the following set of kernel-maintained attributes.</span></span>



| <span data-ttu-id="b9ac6-106">資訊類型</span><span class="sxs-lookup"><span data-stu-id="b9ac6-106">Information type</span></span>                                              | <span data-ttu-id="b9ac6-107">目的</span><span class="sxs-lookup"><span data-stu-id="b9ac6-107">Purpose</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ac6-108">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="b9ac6-108">File name</span></span>                                                     | <span data-ttu-id="b9ac6-109">為對應的實體檔案命名。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-109">Names the corresponding physical file.</span></span>                                                                                                                                                          |
| <span data-ttu-id="b9ac6-110">目前位元組位移</span><span class="sxs-lookup"><span data-stu-id="b9ac6-110">Current byte offset</span></span>                                           | <span data-ttu-id="b9ac6-111">用於同步檔案 i/o (本節稍後所述) 識別讀取和寫入作業目前的開始位置。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-111">Used in synchronous file I/O (described later in this section) to identify the current starting location of read and write operations.</span></span>                                                          |
| <span data-ttu-id="b9ac6-112">共用模式</span><span class="sxs-lookup"><span data-stu-id="b9ac6-112">Share mode</span></span>                                                    | <span data-ttu-id="b9ac6-113">指定第二個進程是否可以在初始進程仍在存取時，開啟檔案以進行讀取、寫入或刪除存取。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-113">Specifies whether a second process can open a file for read, write, or delete access while the initial process is still accessing it.</span></span>                                                           |
| <span data-ttu-id="b9ac6-114">I/o 模式</span><span class="sxs-lookup"><span data-stu-id="b9ac6-114">I/O mode</span></span>                                                      | <span data-ttu-id="b9ac6-115">指定初始進程是否開啟檔案以進行 [同步或非同步 i/o](synchronous-and-asynchronous-i-o.md)、快取或未快取 i/o、連續或隨機 i/o 等等。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-115">Specifies whether the initial process opened the file for [synchronous or asynchronous I/O](synchronous-and-asynchronous-i-o.md), cached or uncached I/O, sequential or random I/O, and so on.</span></span> |
| <span data-ttu-id="b9ac6-116">裝置物件的指標</span><span class="sxs-lookup"><span data-stu-id="b9ac6-116">Pointer to device object</span></span>                                      | <span data-ttu-id="b9ac6-117">識別檔案資料所在的實體裝置。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-117">Identifies the physical device the file data resides on.</span></span>                                                                                                                                        |
| <span data-ttu-id="b9ac6-118">磁片區參數區塊的指標，或 [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb)</span><span class="sxs-lookup"><span data-stu-id="b9ac6-118">Pointer to the volume parameter block, or [**VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb)</span></span> | <span data-ttu-id="b9ac6-119">識別檔案資料所在的磁片區或磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-119">Identifies the volume or partition the file data resides on.</span></span>                                                                                                                                    |
| <span data-ttu-id="b9ac6-120">區段物件指標的指標</span><span class="sxs-lookup"><span data-stu-id="b9ac6-120">Pointer to section object pointers</span></span>                            | <span data-ttu-id="b9ac6-121">識別描述 [對應](/windows/desktop/Memory/file-mapping)檔案的根結構。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-121">Identifies a root structure that describes a [mapped file](/windows/desktop/Memory/file-mapping).</span></span>                                                                                                                  |
| <span data-ttu-id="b9ac6-122">私人快取對應的指標</span><span class="sxs-lookup"><span data-stu-id="b9ac6-122">Pointer to private cache map</span></span>                                  | <span data-ttu-id="b9ac6-123">識別目前快取的檔案資料。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-123">Identifies the file data that is currently cached.</span></span>                                                                                                                                              |



 

<span data-ttu-id="b9ac6-124">在 Ntddk 中，這些屬性會定義為 [**FILE \_ 物件**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) 結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-124">These attributes are defined as part of the [**FILE\_OBJECT**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) structure in Ntddk.h.</span></span> <span data-ttu-id="b9ac6-125">請參閱 Windows 驅動程式套件 (WDK) 檔中此結構的定義，以瞭解值的資料長度和類型。</span><span class="sxs-lookup"><span data-stu-id="b9ac6-125">Refer to the definition of this structure in the Windows Driver Kit (WDK) documentation for the data lengths and types of the values.</span></span>

 

 
