---
description: 符號連結如何影響使用路徑名稱來指定一個或多個檔案的標準檔案函數。
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: 檔案系統函數的符號連結效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988370"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a><span data-ttu-id="eb086-103">檔案系統函數的符號連結效果</span><span class="sxs-lookup"><span data-stu-id="eb086-103">Symbolic Link Effects on File Systems Functions</span></span>

<span data-ttu-id="eb086-104">有數個使用路徑名稱來指定一個或多個檔案的標準檔案函式，會受到符號連結的使用所影響。</span><span class="sxs-lookup"><span data-stu-id="eb086-104">Several standard file functions that use path names to specify one or more files are affected by the use of symbolic links.</span></span> <span data-ttu-id="eb086-105">本主題將列出這些函式並描述行為的變更：</span><span class="sxs-lookup"><span data-stu-id="eb086-105">This topic lists those functions and describes the changes in behavior:</span></span>

-   [<span data-ttu-id="eb086-106">CopyFile 和 CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-106">CopyFile and CopyFileTransacted</span></span>](#copyfile-and-copyfiletransacted)
-   [<span data-ttu-id="eb086-107">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="eb086-107">CopyFileEx</span></span>](#copyfileex)
-   [<span data-ttu-id="eb086-108">CreateFile 和 CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-108">CreateFile and CreateFileTransacted</span></span>](#createfile-and-createfiletransacted)
-   [<span data-ttu-id="eb086-109">CreateHardLink 和 CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-109">CreateHardLink and CreateHardLinkTransacted</span></span>](#createhardlink-and-createhardlinktransacted)
-   [<span data-ttu-id="eb086-110">DeleteFile 和 DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-110">DeleteFile and DeleteFileTransacted</span></span>](#deletefile-and-deletefiletransacted)
-   [<span data-ttu-id="eb086-111">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="eb086-111">FindFirstChangeNotification</span></span>](#findfirstchangenotification)
-   [<span data-ttu-id="eb086-112">FindFirstFile 和 FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-112">FindFirstFile and FindFirstFileTransacted</span></span>](#findfirstfile-and-findfirstfiletransacted)
-   [<span data-ttu-id="eb086-113">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="eb086-113">FindFirstFileEx</span></span>](#findfirstfileex)
-   [<span data-ttu-id="eb086-114">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="eb086-114">FindNextFile</span></span>](#findnextfile)
-   [<span data-ttu-id="eb086-115">GetBinaryType</span><span class="sxs-lookup"><span data-stu-id="eb086-115">GetBinaryType</span></span>](#getbinarytype)
-   [<span data-ttu-id="eb086-116">GetCompressedFileSize 和 GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-116">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [<span data-ttu-id="eb086-117">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="eb086-117">GetDiskFreeSpace</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="eb086-118">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="eb086-118">GetDiskFreeSpaceEx</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="eb086-119">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="eb086-119">GetFileAttributes</span></span>](#getfileattributesex)
-   [<span data-ttu-id="eb086-120">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="eb086-120">GetFileAttributesEx</span></span>](#getfileattributesex)
-   [<span data-ttu-id="eb086-121">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="eb086-121">GetFileSecurity</span></span>](#getfilesecurity)
-   [<span data-ttu-id="eb086-122">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="eb086-122">GetTempPath</span></span>](#gettemppath)
-   [<span data-ttu-id="eb086-123">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="eb086-123">GetVolumeInformation</span></span>](#getvolumeinformation)
-   [<span data-ttu-id="eb086-124">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="eb086-124">SetFileAttributes</span></span>](#setfileattributes)
-   [<span data-ttu-id="eb086-125">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="eb086-125">SetFileSecurity</span></span>](#setfilesecurity)
-   [<span data-ttu-id="eb086-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb086-126">Related topics</span></span>](#related-topics)

<span data-ttu-id="eb086-127">在下列描述中，會使用下列詞彙：</span><span class="sxs-lookup"><span data-stu-id="eb086-127">In the descriptions below, the following terms are used:</span></span>

-   <span data-ttu-id="eb086-128">原始程式檔—要複製的原始檔案。</span><span class="sxs-lookup"><span data-stu-id="eb086-128">Source file—The original file that is to be copied.</span></span>
-   <span data-ttu-id="eb086-129">目的地檔案—新建立的檔案複本。</span><span class="sxs-lookup"><span data-stu-id="eb086-129">Destination file—The newly created copy of the file.</span></span>
-   <span data-ttu-id="eb086-130">目標：符號連結所指向的實體。</span><span class="sxs-lookup"><span data-stu-id="eb086-130">Target—The entity that a symbolic link points to.</span></span>

> [!Note]  
> <span data-ttu-id="eb086-131">接受使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式所建立之控制碼的函式行為（例如 [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)函式）會根據使用檔案旗標 **開啟重新 \_ \_ \_ 分析 \_ 點** 旗標來呼叫 **CreateFile** 函式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="eb086-131">The behavior of functions that accept a handle created using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, such as the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) function, will differ based on whether or not the **CreateFile** function was called using the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span> <span data-ttu-id="eb086-132">如需詳細資訊，請參閱 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 和下列 [CreateFile 和 CreateFileTransacted](#createfile-and-createfiletransacted) 一節。</span><span class="sxs-lookup"><span data-stu-id="eb086-132">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and the following [CreateFile and CreateFileTransacted](#createfile-and-createfiletransacted) section.</span></span>

 

## <a name="copyfile-and-copyfiletransacted"></a><span data-ttu-id="eb086-133">CopyFile 和 CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-133">CopyFile and CopyFileTransacted</span></span>

<span data-ttu-id="eb086-134">如果來源檔案是符號連結，則實際複製的檔案是符號連結的目標。</span><span class="sxs-lookup"><span data-stu-id="eb086-134">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

<span data-ttu-id="eb086-135">如果目的地檔案已經存在，而且是符號連結，則來源檔案會覆寫符號連結。</span><span class="sxs-lookup"><span data-stu-id="eb086-135">If the destination file already exists and is a symbolic link, the symbolic link is overwritten by the source file.</span></span>

## <a name="copyfileex"></a><span data-ttu-id="eb086-136">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="eb086-136">CopyFileEx</span></span>

<span data-ttu-id="eb086-137">如果已指定 **複製檔案 \_ 複製的 \_ \_ 符號** ，且：</span><span class="sxs-lookup"><span data-stu-id="eb086-137">If **COPY\_FILE\_COPY\_SYMLINK** is specified and:</span></span>

-   <span data-ttu-id="eb086-138">如果來源檔案是符號連結，則會複製符號連結，而不是目標檔。</span><span class="sxs-lookup"><span data-stu-id="eb086-138">If the source file is a symbolic link, the symbolic link is copied, not the target file.</span></span>
-   <span data-ttu-id="eb086-139">如果來源檔案不是符號連結，行為就不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="eb086-139">If the source file is not a symbolic link, there is no change in behavior.</span></span>
-   <span data-ttu-id="eb086-140">如果目的地檔案是現有的符號連結，則會覆寫符號連結，而不會覆寫目標檔案。</span><span class="sxs-lookup"><span data-stu-id="eb086-140">If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target file.</span></span>
-   <span data-ttu-id="eb086-141">如果也指定了 [ **\_ \_ \_ 如果 \_ 有的話，複製檔案失敗** ]，而目的地檔案是現有的符號連結，則在所有情況下作業都會失敗。</span><span class="sxs-lookup"><span data-stu-id="eb086-141">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails in all cases.</span></span>

<span data-ttu-id="eb086-142">如果未指定 **複製檔案 \_ 複製的 \_ \_ 符號** ，且：</span><span class="sxs-lookup"><span data-stu-id="eb086-142">If **COPY\_FILE\_COPY\_SYMLINK** is not specified and:</span></span>

-   <span data-ttu-id="eb086-143">如果也指定了 [ **\_ \_ \_ 如果 \_ 有的話，複製檔案失敗** ]，而目的地檔案是現有的符號連結，則只有在符號連結的目標存在時，作業才會失敗。</span><span class="sxs-lookup"><span data-stu-id="eb086-143">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails only if the target of the symbolic link exists.</span></span>
-   <span data-ttu-id="eb086-144">如果未指定 **\_ \_ \_ \_ EXISTS，複製檔案失敗** ，則行為不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="eb086-144">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is not specified, there is no change in behavior.</span></span>

<span data-ttu-id="eb086-145">**Windows Server 2003 和 WINDOWS XP：** 不支援 **複製檔案 \_ \_ 複製 \_ 符號** 旗標。</span><span class="sxs-lookup"><span data-stu-id="eb086-145">**Windows Server 2003 and Windows XP:** The **COPY\_FILE\_COPY\_SYMLINK** flag is not supported.</span></span> <span data-ttu-id="eb086-146">如果來源檔案是符號連結，則實際複製的檔案是符號連結的目標。</span><span class="sxs-lookup"><span data-stu-id="eb086-146">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

## <a name="createfile-and-createfiletransacted"></a><span data-ttu-id="eb086-147">CreateFile 和 CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-147">CreateFile and CreateFileTransacted</span></span>

<span data-ttu-id="eb086-148">如果對此函式的呼叫會建立新的檔案，則不會變更行為。</span><span class="sxs-lookup"><span data-stu-id="eb086-148">If the call to this function creates a new file, there is no change in behavior.</span></span>

<span data-ttu-id="eb086-149">如果指定了檔案旗標，則會指定，且： **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb086-149">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is specified and:</span></span>

-   <span data-ttu-id="eb086-150">如果現有的檔案已經開啟，而且是符號連結，則傳回的控制碼是符號連結的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb086-150">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the symbolic link.</span></span>
-   <span data-ttu-id="eb086-151">如果指定了 [ **\_ 永遠建立**]、[ **截斷 \_ 現有**] 或 [檔案] **旗標 \_ \_ 刪除 \_ \_** ，則會將受影響的檔案設為符號連結。</span><span class="sxs-lookup"><span data-stu-id="eb086-151">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is a symbolic link.</span></span>

<span data-ttu-id="eb086-152">如果未指定檔案旗標， **\_ 開啟重新 \_ \_ 分析 \_ 點** ，且：</span><span class="sxs-lookup"><span data-stu-id="eb086-152">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is not specified and:</span></span>

-   <span data-ttu-id="eb086-153">如果現有的檔案已經開啟，而且是符號連結，則傳回的控制碼就是目標的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb086-153">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the target.</span></span>
-   <span data-ttu-id="eb086-154">如果指定了 [ **\_ 永遠建立**]、[ **截斷 \_ 現有**] 或 [檔案] **旗標 \_ \_ 刪除 \_ \_** ，則會將受影響的檔案設為目標。</span><span class="sxs-lookup"><span data-stu-id="eb086-154">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is the target.</span></span>

## <a name="createhardlink-and-createhardlinktransacted"></a><span data-ttu-id="eb086-155">CreateHardLink 和 CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-155">CreateHardLink and CreateHardLinkTransacted</span></span>

<span data-ttu-id="eb086-156">如果路徑指向符號連結，此函式會建立目標的永久連結。</span><span class="sxs-lookup"><span data-stu-id="eb086-156">If the path points to a symbolic link, the function creates a hard link to the target.</span></span>

## <a name="deletefile-and-deletefiletransacted"></a><span data-ttu-id="eb086-157">DeleteFile 和 DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-157">DeleteFile and DeleteFileTransacted</span></span>

<span data-ttu-id="eb086-158">如果路徑指向符號連結，則會刪除符號連結，而不是目標。</span><span class="sxs-lookup"><span data-stu-id="eb086-158">If the path points to a symbolic link, the symbolic link is deleted, not the target.</span></span> <span data-ttu-id="eb086-159">若要刪除目標，您必須呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ，並 **\_ \_ \_ 在 \_ 關閉時** 指定檔案旗標刪除。</span><span class="sxs-lookup"><span data-stu-id="eb086-159">To delete a target, you must call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and specify **FILE\_FLAG\_DELETE\_ON\_CLOSE**.</span></span>

## <a name="findfirstchangenotification"></a><span data-ttu-id="eb086-160">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="eb086-160">FindFirstChangeNotification</span></span>

<span data-ttu-id="eb086-161">如果路徑指向符號連結，則會為目標建立通知控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb086-161">If the path points to a symbolic link, the notification handle is created for the target.</span></span> <span data-ttu-id="eb086-162">如果應用程式已註冊接收包含符號連結之目錄的變更通知，則只有在已變更符號連結，而非目標檔案時，才會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="eb086-162">If an application has registered to receive change notifications for a directory that contains symbolic links, the application is only notified when the symbolic links have been changed, not the target files.</span></span>

## <a name="findfirstfile-and-findfirstfiletransacted"></a><span data-ttu-id="eb086-163">FindFirstFile 和 FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-163">FindFirstFile and FindFirstFileTransacted</span></span>

<span data-ttu-id="eb086-164">如果路徑指向符號連結， [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) 緩衝區就會包含符號連結（而非目標）的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb086-164">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findfirstfileex"></a><span data-ttu-id="eb086-165">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="eb086-165">FindFirstFileEx</span></span>

<span data-ttu-id="eb086-166">如果路徑指向符號連結， [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) 緩衝區就會包含符號連結（而非目標）的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb086-166">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findnextfile"></a><span data-ttu-id="eb086-167">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="eb086-167">FindNextFile</span></span>

<span data-ttu-id="eb086-168">如果路徑指向符號連結， [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) 緩衝區就會包含符號連結（而非目標）的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb086-168">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="getbinarytype"></a><span data-ttu-id="eb086-169">GetBinaryType</span><span class="sxs-lookup"><span data-stu-id="eb086-169">GetBinaryType</span></span>

<span data-ttu-id="eb086-170">如果路徑指向符號連結，則會使用目標檔案。</span><span class="sxs-lookup"><span data-stu-id="eb086-170">If the path points to a symbolic link, the target file is used.</span></span>

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a><span data-ttu-id="eb086-171">GetCompressedFileSize 和 GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="eb086-171">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>

<span data-ttu-id="eb086-172">如果路徑指向符號連結，函數會傳回目標的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="eb086-172">If the path points to a symbolic link, the function returns the file size of the target.</span></span>

## <a name="getdiskfreespace"></a><span data-ttu-id="eb086-173">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="eb086-173">GetDiskFreeSpace</span></span>

<span data-ttu-id="eb086-174">如果路徑指向符號連結，則會在目標上執行操作。</span><span class="sxs-lookup"><span data-stu-id="eb086-174">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getdiskfreespaceex"></a><span data-ttu-id="eb086-175">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="eb086-175">GetDiskFreeSpaceEx</span></span>

<span data-ttu-id="eb086-176">如果路徑指向符號連結，則會在目標上執行操作。</span><span class="sxs-lookup"><span data-stu-id="eb086-176">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getfileattributes"></a><span data-ttu-id="eb086-177">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="eb086-177">GetFileAttributes</span></span>

<span data-ttu-id="eb086-178">如果路徑指向符號連結，函數會傳回符號連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb086-178">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfileattributesex"></a><span data-ttu-id="eb086-179">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="eb086-179">GetFileAttributesEx</span></span>

<span data-ttu-id="eb086-180">如果路徑指向符號連結，函數會傳回符號連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb086-180">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfilesecurity"></a><span data-ttu-id="eb086-181">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="eb086-181">GetFileSecurity</span></span>

<span data-ttu-id="eb086-182">如果路徑指向符號連結，函數會傳回符號連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb086-182">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="gettemppath"></a><span data-ttu-id="eb086-183">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="eb086-183">GetTempPath</span></span>

<span data-ttu-id="eb086-184">如果路徑指向符號連結，則暫存路徑名稱會維護任何符號連結。</span><span class="sxs-lookup"><span data-stu-id="eb086-184">If the path points to a symbolic link, the temp path name maintains any symbolic links.</span></span>

## <a name="getvolumeinformation"></a><span data-ttu-id="eb086-185">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="eb086-185">GetVolumeInformation</span></span>

<span data-ttu-id="eb086-186">如果路徑指向符號連結，此函數會傳回目標的磁片區資訊。</span><span class="sxs-lookup"><span data-stu-id="eb086-186">If the path points to a symbolic link, the function returns volume information for the target.</span></span>

## <a name="setfileattributes"></a><span data-ttu-id="eb086-187">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="eb086-187">SetFileAttributes</span></span>

<span data-ttu-id="eb086-188">如果路徑指向符號連結，則函式會抓取符號連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb086-188">If the path points to a symbolic link, the function retrieves attributes for the symbolic link.</span></span>

## <a name="setfilesecurity"></a><span data-ttu-id="eb086-189">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="eb086-189">SetFileSecurity</span></span>

<span data-ttu-id="eb086-190">如果路徑指向符號連結，函數會傳回符號連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb086-190">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb086-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb086-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb086-192">**CopyFile**</span><span class="sxs-lookup"><span data-stu-id="eb086-192">**CopyFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[<span data-ttu-id="eb086-193">**CopyFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="eb086-193">**CopyFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[<span data-ttu-id="eb086-194">**CopyFileEx**</span><span class="sxs-lookup"><span data-stu-id="eb086-194">**CopyFileEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[<span data-ttu-id="eb086-195">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="eb086-195">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="eb086-196">**CreateFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="eb086-196">**CreateFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[<span data-ttu-id="eb086-197">**CreateHardLink**</span><span class="sxs-lookup"><span data-stu-id="eb086-197">**CreateHardLink**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[<span data-ttu-id="eb086-198">**CreateHardLinkTransacted**</span><span class="sxs-lookup"><span data-stu-id="eb086-198">**CreateHardLinkTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[<span data-ttu-id="eb086-199">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="eb086-199">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[<span data-ttu-id="eb086-200">**DeleteFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="eb086-200">**DeleteFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[<span data-ttu-id="eb086-201">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="eb086-201">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[<span data-ttu-id="eb086-202">**FindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="eb086-202">**FindFirstFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[<span data-ttu-id="eb086-203">**FindFirstFileEx**</span><span class="sxs-lookup"><span data-stu-id="eb086-203">**FindFirstFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[<span data-ttu-id="eb086-204">**FindFirstFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="eb086-204">**FindFirstFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[<span data-ttu-id="eb086-205">**FindNextFile**</span><span class="sxs-lookup"><span data-stu-id="eb086-205">**FindNextFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[<span data-ttu-id="eb086-206">**GetBinaryType**</span><span class="sxs-lookup"><span data-stu-id="eb086-206">**GetBinaryType**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[<span data-ttu-id="eb086-207">**GetCompressedFileSize**</span><span class="sxs-lookup"><span data-stu-id="eb086-207">**GetCompressedFileSize**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[<span data-ttu-id="eb086-208">**GetCompressedFileSizeTransacted**</span><span class="sxs-lookup"><span data-stu-id="eb086-208">**GetCompressedFileSizeTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[<span data-ttu-id="eb086-209">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="eb086-209">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[<span data-ttu-id="eb086-210">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="eb086-210">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[<span data-ttu-id="eb086-211">**GetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="eb086-211">**GetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[<span data-ttu-id="eb086-212">**GetFileAttributesEx**</span><span class="sxs-lookup"><span data-stu-id="eb086-212">**GetFileAttributesEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[<span data-ttu-id="eb086-213">**GetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="eb086-213">**GetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[<span data-ttu-id="eb086-214">**GetTempPath**</span><span class="sxs-lookup"><span data-stu-id="eb086-214">**GetTempPath**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[<span data-ttu-id="eb086-215">**GetVolumeInformation**</span><span class="sxs-lookup"><span data-stu-id="eb086-215">**GetVolumeInformation**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[<span data-ttu-id="eb086-216">**SetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="eb086-216">**SetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[<span data-ttu-id="eb086-217">**SetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="eb086-217">**SetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
