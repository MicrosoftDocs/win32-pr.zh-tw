---
description: 檔案系統辨識的目標是要讓 Windows 作業系統擁有另一個選項，以供有效但無法辨識的檔案系統使用，而不是 &\# 0034;原始&\# 0034;。
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: 檔案系統識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 457d4146588ba2db2b75d06c7afac10ecb18e87c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997113"
---
# <a name="file-system-recognition"></a><span data-ttu-id="03279-103">檔案系統識別</span><span class="sxs-lookup"><span data-stu-id="03279-103">File System Recognition</span></span>

<span data-ttu-id="03279-104">檔案系統辨識的目標是要讓 Windows 作業系統擁有一個額外的選項，以供有效但無法辨識的檔案系統（非「原始」）使用。</span><span class="sxs-lookup"><span data-stu-id="03279-104">The goal of file system recognition is to allow the Windows operating system to have an additional option for a valid but unrecognized file system other than "RAW".</span></span> <span data-ttu-id="03279-105">為了達成此目的，從 Windows 7 和 Windows Server 2008 R2 開始，系統會定義固定的資料結構類型，此類型可寫入至已啟用的技術（改變檔案系統格式）的媒體。</span><span class="sxs-lookup"><span data-stu-id="03279-105">To achieve this, beginning with Windows 7 and Windows Server 2008 R2, the system defines a fixed data structure type that can be written to the media on which an enabled technology that alters the file system format is active.</span></span> <span data-ttu-id="03279-106">此資料結構（如果存在於邏輯磁片磁區0）將會被作業系統辨識，並通知使用者媒體包含有效但無法辨識的檔案系統，而且如果未安裝檔案系統的驅動程式，則不是原始卷。</span><span class="sxs-lookup"><span data-stu-id="03279-106">This data structure, if present on logical disk sector zero, would then be recognized by the operating system and notify the user that the media contains a valid but unrecognized file system and is not a RAW volume if the drivers for the file system are not installed.</span></span>

## <a name="file-system-recognition-features-and-use"></a><span data-ttu-id="03279-107">檔案系統識別功能與使用</span><span class="sxs-lookup"><span data-stu-id="03279-107">File System Recognition Features and Use</span></span>

<span data-ttu-id="03279-108">有幾項最新的儲存技術已改變磁片檔案系統格式，使這些技術啟用的媒體無法辨識至舊版的 Windows，因為檔案系統驅動程式在發行特定舊版的 Windows 時並不會存在。</span><span class="sxs-lookup"><span data-stu-id="03279-108">Several recent storage technologies have altered the on-disk file system format such that the media on which these technologies are enabled become unrecognizable to earlier versions of Windows due to the file system drivers not existing when a particular earlier version of Windows was released.</span></span> <span data-ttu-id="03279-109">此案例中先前的預設行為如下所示。</span><span class="sxs-lookup"><span data-stu-id="03279-109">The previous default behavior in this scenario was as follows.</span></span> <span data-ttu-id="03279-110">當存放裝置媒體不是已知的檔案系統時，它會被識別為 RAW，然後傳播至 Windows Shell，其中會以使用者介面 (UI) 的格式來提示自動播放提示。</span><span class="sxs-lookup"><span data-stu-id="03279-110">When storage media is not a known file system, it is identified as RAW, and then propagated to the Windows Shell, where Autoplay prompts with the format user interface (UI).</span></span> <span data-ttu-id="03279-111">如果新檔案系統的作者正確地將適當的 [**資料結構**](file-system-recognition-structure.md) 寫入磁片，檔案系統辨識可解決此問題。</span><span class="sxs-lookup"><span data-stu-id="03279-111">File system recognition can solve this if the authors of the new file system correctly write the proper [**data structure**](file-system-recognition-structure.md) to the disk.</span></span>

<span data-ttu-id="03279-112">檔案系統識別會在作業系統內使用下列功能和層級，以達成其目標：</span><span class="sxs-lookup"><span data-stu-id="03279-112">File system recognition uses the following features and layers within the operating system to achieve its goals:</span></span>

-   <span data-ttu-id="03279-113">儲存媒體，其中固定的資料結構會以一系列的位元組順序存在，這些位元組會在內部以預先定義的結構（稱為 [**檔 \_ 系統辨識 \_ \_ 結構**](file-system-recognition-structure.md) 資料結構）排列。</span><span class="sxs-lookup"><span data-stu-id="03279-113">Storage media, where a fixed data structure resides as a sequence of bytes arranged internally in a predefined structure called the [**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**](file-system-recognition-structure.md) data structure.</span></span> <span data-ttu-id="03279-114">檔案系統開發人員必須負責適當地建立此磁片上的結構。</span><span class="sxs-lookup"><span data-stu-id="03279-114">It is the responsibility of the file system developer to create this on-disk structure properly.</span></span>
-   <span data-ttu-id="03279-115">應用層級的檔案系統識別，透過使用 [**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) 裝置 i/o 控制程式代碼來達成。</span><span class="sxs-lookup"><span data-stu-id="03279-115">File system recognition at the application level, achieved via the use of the [**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) device I/O control code.</span></span> <span data-ttu-id="03279-116">如需如何使用此控制項程式碼的範例，請參閱 [取得檔案系統識別資訊](obtaining-file-system-recognition-information.md)。</span><span class="sxs-lookup"><span data-stu-id="03279-116">For an example of how to use this control code, see [Obtaining File System Recognition Information](obtaining-file-system-recognition-information.md).</span></span>
-   <span data-ttu-id="03279-117">總和檢查碼驗證碼，儲存在 [**檔 \_ 系統 \_ 識別 \_ 結構**](file-system-recognition-structure.md) 資料結構內。</span><span class="sxs-lookup"><span data-stu-id="03279-117">Checksum validation code, stored within the [**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**](file-system-recognition-structure.md) data structure.</span></span> <span data-ttu-id="03279-118">如需如何計算此總和檢查碼的範例，請參閱 [計算檔案系統識別總和檢查](computing-a-file-system-recognition-checksum.md)碼。</span><span class="sxs-lookup"><span data-stu-id="03279-118">For an example of how to compute this checksum, see [Computing a File System Recognition Checksum](computing-a-file-system-recognition-checksum.md).</span></span>
-   <span data-ttu-id="03279-119">Windows Shell UI 使用先前列出的功能，為無法辨識的檔案系統提供更具彈性且健全的自動播放和相關支援，但只有當 [**檔 \_ 系統 \_ 辨識 \_ 結構**](file-system-recognition-structure.md) 資料結構存在於邏輯磁片磁區0時才能運作。</span><span class="sxs-lookup"><span data-stu-id="03279-119">The Windows Shell UI uses the previously listed features to provide more flexible and robust Autoplay and related support for unrecognized file systems, but it can work only if the [**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**](file-system-recognition-structure.md) data structure exists in logical disk sector zero.</span></span> <span data-ttu-id="03279-120">執行新檔案系統的開發人員應該利用這個系統來確保其檔案系統不會被誤假設為「RAW」類型。</span><span class="sxs-lookup"><span data-stu-id="03279-120">Developers implementing new file systems should utilize this system to ensure that their file system is not mistakenly assumed to be of type "RAW".</span></span>

## <a name="related-topics"></a><span data-ttu-id="03279-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="03279-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03279-122">計算檔案系統識別總和檢查碼</span><span class="sxs-lookup"><span data-stu-id="03279-122">Computing a File System Recognition Checksum</span></span>](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[<span data-ttu-id="03279-123">取得檔案系統識別資訊</span><span class="sxs-lookup"><span data-stu-id="03279-123">Obtaining File System Recognition Information</span></span>](obtaining-file-system-recognition-information.md)
</dt> <dt>

[<span data-ttu-id="03279-124">取得磁片區資訊</span><span class="sxs-lookup"><span data-stu-id="03279-124">Obtaining Volume Information</span></span>](obtaining-volume-information.md)
</dt> </dl>

 

 
