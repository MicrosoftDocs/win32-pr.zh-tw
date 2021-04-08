---
description: 在 NTFS 檔案系統磁片區上，每個檔案和目錄都有一個壓縮屬性。
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: 壓縮屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852976"
---
# <a name="compression-attribute"></a><span data-ttu-id="2b3c0-103">壓縮屬性</span><span class="sxs-lookup"><span data-stu-id="2b3c0-103">Compression Attribute</span></span>

<span data-ttu-id="2b3c0-104">在 NTFS 檔案系統磁片區上，每個檔案和目錄都有一個 *壓縮屬性*。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-104">On an NTFS file system volume, each file and directory has a *compression attribute*.</span></span> <span data-ttu-id="2b3c0-105">其他檔案系統也可以針對個別檔案和目錄執行壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-105">Other file systems may also implement a compression attribute for individual files and directories.</span></span>

<span data-ttu-id="2b3c0-106">您可以藉由呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式並檢查 **檔案 \_ \_ 壓縮** 位旗標，判斷檔案系統是否支援檔案和目錄的壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-106">You can determine whether a file system supports a compression attribute for files and directories by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_FILE\_COMPRESSION** bit flag.</span></span>

<span data-ttu-id="2b3c0-107">使用 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 或 [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) 函數來判斷檔案或目錄的壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-107">Use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function to determine the compression attribute of a file or directory.</span></span>

<span data-ttu-id="2b3c0-108">如果檔案的壓縮屬性設定 (**檔 \_ 屬性 \_ 壓縮**) ，則會壓縮檔案中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-108">If a file's compression attribute is set (**FILE\_ATTRIBUTE\_COMPRESSED**), all data in the file is compressed.</span></span> <span data-ttu-id="2b3c0-109">如果屬性為清除，則不會壓縮檔案中的任何資料。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-109">If the attribute is clear, none of the data in the file is compressed.</span></span> <span data-ttu-id="2b3c0-110">從使用者模式程式設計觀點來看，沒有部分壓縮的狀態;壓縮屬性是壓縮狀態的簡單布林指標。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-110">There is no partially compressed state from a user-mode programming perspective; the compression attribute is a simple Boolean indicator of compression state.</span></span>

<span data-ttu-id="2b3c0-111">目錄的壓縮屬性為新建立的檔案和子目錄提供預設的壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-111">A directory's compression attribute provides a default compression attribute for newly created files and subdirectories.</span></span> <span data-ttu-id="2b3c0-112">當您呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 或 [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) 來建立新的檔案或目錄時，新的檔案或目錄會繼承其父目錄的壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-112">When you call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) to create a new file or directory, the new file or directory inherits the compression attribute of its parent directory.</span></span>

<span data-ttu-id="2b3c0-113">若要修改檔案或目錄的 **檔 \_ 屬性 \_ 壓縮** 屬性，您必須搭配使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式和 [**FSCTL \_ SET \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) 控制程式代碼。</span><span class="sxs-lookup"><span data-stu-id="2b3c0-113">To modify the **FILE\_ATTRIBUTE\_COMPRESSED** attribute for a file or directory, you must use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b3c0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b3c0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b3c0-115">**檔案屬性常數**</span><span class="sxs-lookup"><span data-stu-id="2b3c0-115">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 
