---
description: 下列介面定義是以標準的形式提供，可在開發智慧卡服務提供者時遵循。
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: ISCardFileAccess 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850143"
---
# <a name="iscardfileaccess-interface"></a><span data-ttu-id="dc8f4-103">ISCardFileAccess 介面</span><span class="sxs-lookup"><span data-stu-id="dc8f4-103">ISCardFileAccess interface</span></span>

<span data-ttu-id="dc8f4-104">\[**ISCardFileAccess** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-104">\[The **ISCardFileAccess** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dc8f4-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dc8f4-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="dc8f4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dc8f4-107">下列介面定義是以標準的形式提供，可在開發 [*智慧卡*](../secgloss/s-gly.md)[*服務提供者*](../secgloss/c-gly.md)時遵循。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="dc8f4-108">**ISCardFileAccess** 介面可用來根據 ISO/IEC 7816-4 中定義的結構，使用基礎卡片檔案系統來對卡片型檔案系統執行高階介面。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-108">The **ISCardFileAccess** interface can be used to implement a high-level interface to a card-based file system with an underlying card file system based on the structure defined in ISO/IEC 7816-4.</span></span> <span data-ttu-id="dc8f4-109">其他實作為可能，但這應該是最常見的。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-109">Other implementations are possible, but this is expected to be the most common.</span></span>

<span data-ttu-id="dc8f4-110">**ISCardFileAccess** 介面可用來以對電腦環境中應用程式開發人員非常熟悉的方式來公開檔案系統實體。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-110">The **ISCardFileAccess** interface can be used to expose file system entities in a manner very familiar to application developers in the PC environment.</span></span> <span data-ttu-id="dc8f4-111">它提供了尋找特定檔案和執行一般作業（例如選取、讀取、寫入、建立和刪除）的機制。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-111">It provides mechanisms for locating specific files and performing common operations such as selecting, reading, writing, creating and deleting.</span></span> <span data-ttu-id="dc8f4-112">它會封裝和遮罩大部分的低層級詳細資料，包括在卡片層級執行這些作業。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-112">It encapsulates and masks much of the low-level detail involved in performing these operations at the card level.</span></span>

<span data-ttu-id="dc8f4-113">以下是 **ISCardFileAccess** 介面的一般用法。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-113">Following is a typical use of the **ISCardFileAccess** interface.</span></span> <span data-ttu-id="dc8f4-114">在此情況下， **ISCardFileAccess** 介面是用來選取、開啟和寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-114">In this case, the **ISCardFileAccess** interface is used to select, open, and write to a file.</span></span>

<span data-ttu-id="dc8f4-115">**寫入檔案**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-115">**To write to a file**</span></span>

1.  <span data-ttu-id="dc8f4-116">呼叫 [**ISCardManage：： CreateFileAccess**](iscardmanage-createfileaccess.md) 來建立 **ISCardFileAccess** 介面。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-116">Call [**ISCardManage::CreateFileAccess**](iscardmanage-createfileaccess.md) to create an **ISCardFileAccess** interface.</span></span>
2.  <span data-ttu-id="dc8f4-117">呼叫 [**Open**](iscardfileaccess-open.md) 以選取並開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-117">Call [**Open**](iscardfileaccess-open.md) to select and open the file.</span></span>
3.  <span data-ttu-id="dc8f4-118">呼叫 [**Write**](iscardfileaccess-write.md)。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-118">Call [**Write**](iscardfileaccess-write.md).</span></span>
4.  <span data-ttu-id="dc8f4-119">呼叫 [**Close**](iscardfileaccess-close.md)。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-119">Call [**Close**](iscardfileaccess-close.md).</span></span>
5.  <span data-ttu-id="dc8f4-120">釋放 **ISCardFileAccess** 介面。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-120">Release the **ISCardFileAccess** interface.</span></span>

## <a name="members"></a><span data-ttu-id="dc8f4-121">成員</span><span class="sxs-lookup"><span data-stu-id="dc8f4-121">Members</span></span>

<span data-ttu-id="dc8f4-122">**ISCardFileAccess** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-122">The **ISCardFileAccess** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="dc8f4-123">**ISCardFileAccess** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dc8f4-123">**ISCardFileAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="dc8f4-124">方法</span><span class="sxs-lookup"><span data-stu-id="dc8f4-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc8f4-125">方法</span><span class="sxs-lookup"><span data-stu-id="dc8f4-125">Methods</span></span>

<span data-ttu-id="dc8f4-126">**ISCardFileAccess** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-126">The **ISCardFileAccess** interface has these methods.</span></span>



| <span data-ttu-id="dc8f4-127">方法</span><span class="sxs-lookup"><span data-stu-id="dc8f4-127">Method</span></span>                                                              | <span data-ttu-id="dc8f4-128">描述</span><span class="sxs-lookup"><span data-stu-id="dc8f4-128">Description</span></span>                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc8f4-129">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-129">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)                     | <span data-ttu-id="dc8f4-130">將目前的智慧卡目錄變更為新指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-130">Changes the current smart card directory to the new specified directory.</span></span><br/>                                                          |
| [<span data-ttu-id="dc8f4-131">**關閉**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-131">**Close**</span></span>](iscardfileaccess-close.md)                             | <span data-ttu-id="dc8f4-132">關閉指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-132">Closes the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="dc8f4-133">**建立**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-133">**Create**</span></span>](iscardfileaccess-create.md)                           | <span data-ttu-id="dc8f4-134">在 ICC 檔案系統內的指定位置建立檔案。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-134">Creates a file at a given location within the ICC file system.</span></span><br/>                                                                    |
| [<span data-ttu-id="dc8f4-135">**刪除**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-135">**Delete**</span></span>](iscardfileaccess-delete.md)                           | <span data-ttu-id="dc8f4-136">刪除指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-136">Deletes a specified file.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="dc8f4-137">**目錄**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-137">**Directory**</span></span>](iscardfileaccess-directory.md)                     | <span data-ttu-id="dc8f4-138">抓取檔案清單。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-138">Retrieves a list of files.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="dc8f4-139">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-139">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)             | <span data-ttu-id="dc8f4-140">傳回目前所選目錄的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-140">Returns an absolute path to the currently selected directory.</span></span><br/>                                                                     |
| [<span data-ttu-id="dc8f4-141">**GetFileCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-141">**GetFileCapabilities**</span></span>](iscardfileaccess-getfilecapabilities.md) | <span data-ttu-id="dc8f4-142">捕獲檔案功能。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-142">Retrieves file capabilities.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="dc8f4-143">**GetProperties**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-143">**GetProperties**</span></span>](iscardfileaccess-getproperties.md)             | <span data-ttu-id="dc8f4-144">取得指定之物件的標記所參考的基本資料。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-144">Retrieves the primitive data referred by tags for the specified object.</span></span><br/>                                                           |
| [<span data-ttu-id="dc8f4-145">**無效**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-145">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)                   | <span data-ttu-id="dc8f4-146">使指定的檔案無效。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-146">Makes the specified file not valid.</span></span><br/>                                                                                               |
| [<span data-ttu-id="dc8f4-147">**打開**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-147">**Open**</span></span>](iscardfileaccess-open.md)                               | <span data-ttu-id="dc8f4-148">開啟指定的檔案以供進一步使用。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-148">Opens the specified file for further use.</span></span><br/>                                                                                         |
| [<span data-ttu-id="dc8f4-149">**讀**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-149">**Read**</span></span>](iscardfileaccess-read.md)                               | <span data-ttu-id="dc8f4-150">從指定的檔案讀取並傳回指定的資料。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-150">Reads and returns the specified data from a given file.</span></span><br/>                                                                           |
| [<span data-ttu-id="dc8f4-151">**恢復**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-151">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)               | <span data-ttu-id="dc8f4-152">使用不正確命令（可由應用程式存取），使檔案 (EF 或 DF) 。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-152">Makes a file (EF or DF), which has been previously made not valid by using the Invalidate command, accessible by the application.</span></span><br/> |
| [<span data-ttu-id="dc8f4-153">**Seek**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-153">**Seek**</span></span>](iscardfileaccess-seek.md)                               | <span data-ttu-id="dc8f4-154">選取將完成讀取/寫入權限的物件。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-154">Selects the object from which read/write permission will be done.</span></span><br/>                                                                 |
| [<span data-ttu-id="dc8f4-155">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-155">**SetProperties**</span></span>](iscardfileaccess-setproperties.md)             | <span data-ttu-id="dc8f4-156">設定指定之物件的標記所參考的基本資料。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-156">Sets the primitive data referred by tags for the specified object.</span></span><br/>                                                                |
| [<span data-ttu-id="dc8f4-157">**寫**</span><span class="sxs-lookup"><span data-stu-id="dc8f4-157">**Write**</span></span>](iscardfileaccess-write.md)                             | <span data-ttu-id="dc8f4-158">將資料寫入目前開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="dc8f4-158">Writes data to a current opened file.</span></span><br/>                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="dc8f4-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc8f4-159">Requirements</span></span>



| <span data-ttu-id="dc8f4-160">需求</span><span class="sxs-lookup"><span data-stu-id="dc8f4-160">Requirement</span></span> | <span data-ttu-id="dc8f4-161">值</span><span class="sxs-lookup"><span data-stu-id="dc8f4-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc8f4-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc8f4-162">Minimum supported client</span></span><br/> | <span data-ttu-id="dc8f4-163">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc8f4-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="dc8f4-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc8f4-164">Minimum supported server</span></span><br/> | <span data-ttu-id="dc8f4-165">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc8f4-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dc8f4-166">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="dc8f4-166">End of client support</span></span><br/>    | <span data-ttu-id="dc8f4-167">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc8f4-167">Windows XP</span></span><br/>                                |
| <span data-ttu-id="dc8f4-168">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="dc8f4-168">End of server support</span></span><br/>    | <span data-ttu-id="dc8f4-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc8f4-169">Windows Server 2003</span></span><br/>                       |



 

 
