---
description: 磁片區上的每個檔案和目錄都支援個別檔案和目錄的壓縮，都有壓縮狀態。
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: 壓縮狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192995"
---
# <a name="compression-state"></a><span data-ttu-id="36f00-103">壓縮狀態</span><span class="sxs-lookup"><span data-stu-id="36f00-103">Compression State</span></span>

<span data-ttu-id="36f00-104">磁片區上的每個檔案和目錄都支援個別檔案和目錄的壓縮，都有 *壓縮狀態*。</span><span class="sxs-lookup"><span data-stu-id="36f00-104">Each file and directory on a volume that supports compression for individual files and directories has a *compression state*.</span></span>

<span data-ttu-id="36f00-105">檔案或目錄的壓縮屬性只會指出檔案或目錄是否已壓縮或未壓縮，而壓縮狀態也會指定任何壓縮資料的格式。</span><span class="sxs-lookup"><span data-stu-id="36f00-105">Whereas the compression attribute of a file or directory indicates simply whether the file or directory is compressed or not compressed, the compression state also specifies the format of any compressed data.</span></span>

<span data-ttu-id="36f00-106">使用 [**FSCTL \_ 取得 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) 控制程式代碼來判斷檔案或目錄的壓縮狀態。</span><span class="sxs-lookup"><span data-stu-id="36f00-106">Use the [**FSCTL\_GET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) control code to determine the compression state of a file or directory.</span></span>

<span data-ttu-id="36f00-107">壓縮狀態會編碼為16位值。</span><span class="sxs-lookup"><span data-stu-id="36f00-107">Compression state is encoded as a 16-bit value.</span></span> <span data-ttu-id="36f00-108">壓縮格式的壓縮狀態值 \_ [ \_ 無] 表示不壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="36f00-108">A compression state value of COMPRESSION\_FORMAT\_NONE indicates that a file is not compressed.</span></span> <span data-ttu-id="36f00-109">壓縮 \_ 格式 \_ 預設值表示使用預設壓縮格式壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="36f00-109">A value of COMPRESSION\_FORMAT\_DEFAULT indicates that a file is compressed, using the default compression format.</span></span> <span data-ttu-id="36f00-110">任何其他值則表示壓縮檔案，使用壓縮狀態值指定的壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="36f00-110">Any other value indicates that a file is compressed, using the compression format specified by the compression state value.</span></span>

<span data-ttu-id="36f00-111">使用 [**FSCTL \_ 設定 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) 控制程式代碼來設定檔案或目錄的壓縮狀態。</span><span class="sxs-lookup"><span data-stu-id="36f00-111">Use the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code to set the compression state of a file or directory.</span></span> <span data-ttu-id="36f00-112">此操作也會設定檔案或目錄的壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="36f00-112">This operation also sets the compression attribute of the file or directory.</span></span>

<span data-ttu-id="36f00-113">將檔案的壓縮狀態設定為非零值，會使用壓縮狀態值所編碼的壓縮格式來壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="36f00-113">Setting the compression state of a file to a nonzero value compresses the file, using the compression format encoded by the compression state value.</span></span> <span data-ttu-id="36f00-114">將檔案的壓縮狀態設定為零會解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="36f00-114">Setting a file's compression state to zero decompresses the file.</span></span> <span data-ttu-id="36f00-115">這些是同步作業。</span><span class="sxs-lookup"><span data-stu-id="36f00-115">These are synchronous operations.</span></span> <span data-ttu-id="36f00-116">當您設定壓縮狀態時，就會立即壓縮或解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="36f00-116">The file is compressed or decompressed immediately when you set its compression state.</span></span>

<span data-ttu-id="36f00-117">設定目錄的壓縮狀態不會造成任何立即壓縮或解壓縮。</span><span class="sxs-lookup"><span data-stu-id="36f00-117">Setting a directory's compression state does not cause any immediate compression or decompression.</span></span> <span data-ttu-id="36f00-118">相反地，設定目錄的壓縮狀態會設定預設壓縮狀態，以提供給所有新建立的檔案和子目錄。</span><span class="sxs-lookup"><span data-stu-id="36f00-118">Instead, setting a directory's compression state sets a default compression state that will be given to all newly created files and subdirectories.</span></span>

 

 
