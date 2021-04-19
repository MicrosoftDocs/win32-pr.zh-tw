---
description: 使用 CreateFile 函數建立或開啟檔案的考慮。
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: 建立和開啟檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1430675862b10f9e9221d968242481525dc7632f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979985"
---
# <a name="creating-and-opening-files"></a><span data-ttu-id="fd640-103">建立和開啟檔案</span><span class="sxs-lookup"><span data-stu-id="fd640-103">Creating and Opening Files</span></span>

<span data-ttu-id="fd640-104">[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式可以建立新的檔案，或開啟現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="fd640-104">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function can create a new file or open an existing file.</span></span> <span data-ttu-id="fd640-105">您必須指定檔案名、建立指示和其他屬性。</span><span class="sxs-lookup"><span data-stu-id="fd640-105">You must specify the file name, creation instructions, and other attributes.</span></span> <span data-ttu-id="fd640-106">當應用程式建立新檔案時，作業系統會將它新增至指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="fd640-106">When an application creates a new file, the operating system adds it to the specified directory.</span></span>

<span data-ttu-id="fd640-107">作業系統會針對使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)開啟或建立的每個檔案，指派一個稱為 *控制碼* 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd640-107">The operating system assigns a unique identifier, called a *handle*, to each file that is opened or created using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span> <span data-ttu-id="fd640-108">應用程式可以使用此控制碼來處理讀取、寫入和描述檔案的函式。</span><span class="sxs-lookup"><span data-stu-id="fd640-108">An application can use this handle with functions that read from, write to, and describe the file.</span></span> <span data-ttu-id="fd640-109">它會一直有效，直到該控制碼的所有參考都已關閉為止。</span><span class="sxs-lookup"><span data-stu-id="fd640-109">It is valid until all references to that handle are closed.</span></span> <span data-ttu-id="fd640-110">當應用程式啟動時，如果將控制碼建立為可繼承，它就會從啟動它的進程繼承所有開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd640-110">When an application starts, it inherits all open handles from the process that started it if the handles were created as inheritable.</span></span>

<span data-ttu-id="fd640-111">應用程式應該先檢查 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 傳回的控制碼值，再嘗試使用控制碼來存取檔案。</span><span class="sxs-lookup"><span data-stu-id="fd640-111">An application should check the value of the handle returned by [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) before attempting to use the handle to access the file.</span></span> <span data-ttu-id="fd640-112">如果發生錯誤，控制碼值將會是 **不正確 \_ 控制碼 \_ 值** ，而且應用程式可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數來取得延伸的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="fd640-112">If an error occurs, the handle value will be **INVALID\_HANDLE\_VALUE** and the application can use the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function for extended error information.</span></span>

<span data-ttu-id="fd640-113">當應用程式使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)時，它必須使用 *dwDesiredAccess* 參數來指定是否要從檔案讀取、寫入檔案、讀取和寫入，或兩者皆非。</span><span class="sxs-lookup"><span data-stu-id="fd640-113">When an application uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), it must use the *dwDesiredAccess* parameter to specify whether it intends to read from the file, write to the file, both read and write, or neither.</span></span> <span data-ttu-id="fd640-114">這就是所謂的要求 *存取模式*。</span><span class="sxs-lookup"><span data-stu-id="fd640-114">This is known as requesting an *access mode*.</span></span> <span data-ttu-id="fd640-115">應用程式也必須使用 *dwCreationDisposition* 參數來指定檔案已存在時要採取的動作，稱為「 *建立* 配置」。</span><span class="sxs-lookup"><span data-stu-id="fd640-115">The application must also use the *dwCreationDisposition* parameter to specify what action to take if the file already exists, known as the *creation disposition*.</span></span> <span data-ttu-id="fd640-116">例如，應用程式可以呼叫 **CreateFile** ，並將 *dwCreationDisposition* 設定 **為 \_ 一律建立新** 檔案，即使已經存在相同名稱的檔案 (因此會覆寫現有的檔案) 。</span><span class="sxs-lookup"><span data-stu-id="fd640-116">For example, an application can call **CreateFile** with *dwCreationDisposition* set to **CREATE\_ALWAYS** to always create a new file, even if a file of the same name already exists (thus overwriting the existing file).</span></span> <span data-ttu-id="fd640-117">這是否成功或不取決於前一個檔案的屬性和安全性設定等因素 (如需) 詳細資訊，請參閱下列各節。</span><span class="sxs-lookup"><span data-stu-id="fd640-117">Whether this succeeds or not depends on factors such as the previous file's attributes and security settings (see the following sections for more information).</span></span>

<span data-ttu-id="fd640-118">應用程式也會使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 來指定是否要共用檔案以進行讀取、寫入、或兩者皆非。</span><span class="sxs-lookup"><span data-stu-id="fd640-118">An application also uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to specify whether it wants to share the file for reading, writing, both, or neither.</span></span> <span data-ttu-id="fd640-119">這就是所謂的 *共用模式*。</span><span class="sxs-lookup"><span data-stu-id="fd640-119">This is known as the *sharing mode*.</span></span> <span data-ttu-id="fd640-120">未共用的開啟檔案 (*dwShareMode* 設為零) 無法再由開啟它的應用程式或其他應用程式重新開啟，直到其控制碼關閉為止。</span><span class="sxs-lookup"><span data-stu-id="fd640-120">An open file that is not shared (*dwShareMode* set to zero) cannot be opened again, either by the application that opened it or by another application, until its handle has been closed.</span></span> <span data-ttu-id="fd640-121">這也稱為獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="fd640-121">This is also referred to as exclusive access.</span></span>

<span data-ttu-id="fd640-122">當進程使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 嘗試開啟已在共用模式中開啟的檔案 (*dwShareMode* 設定為有效的非零) 值時，系統會將所要求的存取和共用模式，與開啟檔案時所指定的模式進行比較。</span><span class="sxs-lookup"><span data-stu-id="fd640-122">When a process uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to attempt to open a file that has already been opened in a sharing mode (*dwShareMode* set to a valid nonzero value), the system compares the requested access and sharing modes to those specified when the file was opened.</span></span> <span data-ttu-id="fd640-123">如果您指定的存取或共用模式與先前呼叫中指定的模式衝突， **CreateFile** 就會失敗。</span><span class="sxs-lookup"><span data-stu-id="fd640-123">If you specify an access or sharing mode that conflicts with the modes specified in the previous call, **CreateFile** fails.</span></span>

<span data-ttu-id="fd640-124">下表說明使用各種存取模式來 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 兩個呼叫的有效組合，以及 (*dwDesiredAccess*、 *dwShareMode* 分別) 的共用模式。</span><span class="sxs-lookup"><span data-stu-id="fd640-124">The following table illustrates the valid combinations of two calls to [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) using various access modes and sharing modes (*dwDesiredAccess*, *dwShareMode* respectively).</span></span> <span data-ttu-id="fd640-125">進行 **CreateFile** 呼叫的順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="fd640-125">It does not matter in which order the **CreateFile** calls are made.</span></span> <span data-ttu-id="fd640-126">不過，每個檔案控制代碼上的任何後續檔案 i/o 作業仍會受限於與該特定檔案控制代碼相關聯的目前存取和共用模式。</span><span class="sxs-lookup"><span data-stu-id="fd640-126">However, any subsequent file I/O operations on each file handle will still be constrained by the current access and sharing modes associated with that particular file handle.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd640-127">第一次呼叫<a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="fd640-127">First call to <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"><strong>CreateFile</strong></a></span></span></th>
<th><span data-ttu-id="fd640-128">CreateFile 的有效第二次呼叫<a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong></strong></a></span><span class="sxs-lookup"><span data-stu-id="fd640-128">Valid second calls to <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"><strong>CreateFile</strong></a></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd640-129"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-129"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-130"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-130"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></span></span></li>
<li><span data-ttu-id="fd640-131"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-131"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd640-132"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-132"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-133"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-133"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></span></span></li>
<li><span data-ttu-id="fd640-134"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-134"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd640-135"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-135"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-136"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-136"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></span></span></li>
<li><span data-ttu-id="fd640-137"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-137"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-138"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-138"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></span></span></li>
<li><span data-ttu-id="fd640-139"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-139"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-140"><strong>GENERIC_READ</strong>  | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-140"><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></span></span></li>
<li><span data-ttu-id="fd640-141"><strong>GENERIC_READ</strong>  | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-141"><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd640-142"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-142"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-143"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-143"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-144"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-144"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd640-145"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-145"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-146"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-146"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-147"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-147"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd640-148"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-148"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-149"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-149"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-150"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-150"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-151"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-151"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-152"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-152"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-153"><strong>GENERIC_READ</strong>  | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-153"><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-154"><strong>GENERIC_READ</strong>  | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-154"><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd640-155"><strong>GENERIC_READ</strong>  | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-155"><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-156"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-156"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd640-157"><strong>GENERIC_READ</strong>  | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-157"><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-158"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-158"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd640-159"><strong>GENERIC_READ</strong>  | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-159"><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fd640-160"><strong>GENERIC_READ</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-160"><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-161"><strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-161"><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
<li><span data-ttu-id="fd640-162"><strong>GENERIC_READ</strong>  | <strong>GENERIC_WRITE</strong>， <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="fd640-162"><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fd640-163">除了標準檔案屬性之外，您也可以將 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構的指標包含為 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)的第四個參數，以指定安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="fd640-163">In addition to the standard file attributes, you can also specify security attributes by including a pointer to a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure as the fourth parameter of [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span> <span data-ttu-id="fd640-164">不過，基礎檔案系統必須支援安全性，才能產生任何影響 (例如，NTFS 檔案系統支援它，但不) 各種 FAT 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="fd640-164">However, the underlying file system must support security for this to have any effect (for example, the NTFS file system supports it but the various FAT file systems do not).</span></span> <span data-ttu-id="fd640-165">如需安全性屬性的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="fd640-165">For more information about security attributes, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="fd640-166">建立新檔案的應用程式可以提供範本檔案的選擇性控制碼， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 會從中取得檔案屬性和擴充屬性，以建立新檔案。</span><span class="sxs-lookup"><span data-stu-id="fd640-166">An application creating a new file can supply an optional handle to a template file, from which [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) takes file attributes and extended attributes for creation of the new file.</span></span>

## <a name="createfile-scenarios"></a><span data-ttu-id="fd640-167">CreateFile 案例</span><span class="sxs-lookup"><span data-stu-id="fd640-167">CreateFile Scenarios</span></span>

<span data-ttu-id="fd640-168">有幾個基本案例可以使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式來初始存取檔案。</span><span class="sxs-lookup"><span data-stu-id="fd640-168">There are several fundamental scenarios for initiating access to a file using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="fd640-169">這些摘要如下所示：</span><span class="sxs-lookup"><span data-stu-id="fd640-169">These are summarized as:</span></span>

-   <span data-ttu-id="fd640-170">當同名的檔案不存在時，建立新的檔案。</span><span class="sxs-lookup"><span data-stu-id="fd640-170">Creating a new file when a file with that name does not already exist.</span></span>
-   <span data-ttu-id="fd640-171">即使已經存在相同名稱的檔案，也會建立新檔案，清除其資料並開始空白。</span><span class="sxs-lookup"><span data-stu-id="fd640-171">Creating a new file even if a file of the same name already exists, clearing its data and starting empty.</span></span>
-   <span data-ttu-id="fd640-172">只有在現有檔案存在時才會開啟，而且只有完整檔案。</span><span class="sxs-lookup"><span data-stu-id="fd640-172">Opening an existing file only if it exists, and only intact.</span></span>
-   <span data-ttu-id="fd640-173">開啟現有的檔案（如果有的話），並將它截斷為空白。</span><span class="sxs-lookup"><span data-stu-id="fd640-173">Opening an existing file only if it exists, truncating it to be empty.</span></span>
-   <span data-ttu-id="fd640-174">開啟檔案一律為：依原樣存在，如果存在，則建立新的檔案（如果不存在的話）。</span><span class="sxs-lookup"><span data-stu-id="fd640-174">Opening a file always: as-is if it exists, creating a new one if it does not exist.</span></span>

<span data-ttu-id="fd640-175">這些案例是由適當使用 *dwCreationDisposition* 參數所控制。</span><span class="sxs-lookup"><span data-stu-id="fd640-175">These scenarios are controlled by the proper use of the *dwCreationDisposition* parameter.</span></span> <span data-ttu-id="fd640-176">以下是這些案例如何對應至這個參數的值，以及使用時所發生的情況的明細。</span><span class="sxs-lookup"><span data-stu-id="fd640-176">Below is a breakdown of how these scenarios map to values for this parameter and what happens when they are used.</span></span>

<span data-ttu-id="fd640-177">當您在使用該名稱的檔案不存在時建立或開啟新檔案 (*dwCreationDisposition* 設定為 [ **建立 \_ 新** 的]、[ **建立 \_ 永遠**] 或 [ **開啟 \_ always**) ] 時， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="fd640-177">When creating or opening a new file when a file with that name does not already exist (*dwCreationDisposition* set to either **CREATE\_NEW**, **CREATE\_ALWAYS**, or **OPEN\_ALWAYS**), the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function performs the following actions:</span></span>

-   <span data-ttu-id="fd640-178">將 *dwFlagsAndAttributes* 指定的檔案屬性和旗標與 **檔 \_ 屬性 \_** 封存合併。</span><span class="sxs-lookup"><span data-stu-id="fd640-178">Combines the file attributes and flags specified by *dwFlagsAndAttributes* with **FILE\_ATTRIBUTE\_ARCHIVE**.</span></span>
-   <span data-ttu-id="fd640-179">將檔案長度設定為零。</span><span class="sxs-lookup"><span data-stu-id="fd640-179">Sets the file length to zero.</span></span>
-   <span data-ttu-id="fd640-180">如果指定了 *hTemplateFile* 參數，則會將範本檔案提供的擴充屬性複製到新檔案 (這會覆寫先前) 指定的所有 \**檔 \_ 屬性 \_ \** _ 旗標。</span><span class="sxs-lookup"><span data-stu-id="fd640-180">Copies the extended attributes supplied by the template file to the new file if the *hTemplateFile* parameter is specified (this overrides all \**FILE\_ATTRIBUTE\_\** _ flags specified earlier).</span></span>
-   <span data-ttu-id="fd640-181">設定 _ *bInheritHandle*\* 成員所指定的繼承旗標，以及 *LpSecurityAttributes* 參數的 **lpSecurityDescriptor** 成員所指定的安全描述項， ([**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構) （如果有提供的話）。</span><span class="sxs-lookup"><span data-stu-id="fd640-181">Sets the inherit flag specified by the _ *bInheritHandle*\* member and the security descriptor specified by the **lpSecurityDescriptor** member of the *lpSecurityAttributes* parameter ([**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure), if supplied.</span></span>

<span data-ttu-id="fd640-182">當您建立新檔案時，即使已經有相同名稱的檔案 (*dwCreationDisposition* 設定為 [ **建立 \_ 永遠**) ]， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="fd640-182">When creating a new file even if a file of the same name already exists (*dwCreationDisposition* set to **CREATE\_ALWAYS**), the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function performs the following actions:</span></span>

-   <span data-ttu-id="fd640-183">檢查目前的檔案屬性和安全性設定是否有寫入權限，如果拒絕，則失敗。</span><span class="sxs-lookup"><span data-stu-id="fd640-183">Checks current file attributes and security settings for write access, failing if denied.</span></span>
-   <span data-ttu-id="fd640-184">結合 *dwFlagsAndAttributes* 指定的檔案屬性和旗標與 **檔 \_ 屬性 \_** 封存和現有的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="fd640-184">Combines the file attributes and flags specified by *dwFlagsAndAttributes* with **FILE\_ATTRIBUTE\_ARCHIVE** and the existing file attributes.</span></span>
-   <span data-ttu-id="fd640-185">將檔案長度設定為零 (也就是說，檔案中的任何資料都無法再使用，且檔案是空的) 。</span><span class="sxs-lookup"><span data-stu-id="fd640-185">Sets the file length to zero (that is, any data that was in the file is no longer available and the file is empty).</span></span>
-   <span data-ttu-id="fd640-186">如果指定了 *hTemplateFile* 參數，則會將範本檔案提供的擴充屬性複製到新檔案 (這會覆寫先前) 指定的所有 \**檔 \_ 屬性 \_ \** _ 旗標。</span><span class="sxs-lookup"><span data-stu-id="fd640-186">Copies the extended attributes supplied by the template file to the new file if the *hTemplateFile* parameter is specified (this overrides all \**FILE\_ATTRIBUTE\_\** _ flags specified earlier).</span></span>
-   <span data-ttu-id="fd640-187">設定 *lpSecurityAttributes* 參數的 _ *bInheritHandle*\* 成員所指定的 Inherit 旗標 ([**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構) （如果有提供的話），但忽略 **安全性 \_ 屬性** 結構的 **lpSecurityDescriptor** 成員。</span><span class="sxs-lookup"><span data-stu-id="fd640-187">Sets the inherit flag specified by the _ *bInheritHandle*\* member of the *lpSecurityAttributes* parameter ([**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure) if supplied, but ignores the **lpSecurityDescriptor** member of the **SECURITY\_ATTRIBUTES** structure.</span></span>
-   <span data-ttu-id="fd640-188">否則，如果 (成功，則 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)會傳回有效的控制碼) ，呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)將會產生程式碼錯誤，即使在這個特定的使用案例中，如果您想要建立 "new" (空白的) 檔案來取代現有的) 檔案，也不會造成 (錯誤。 **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="fd640-188">If otherwise successful (that is, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) returns a valid handle), calling [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will yield the code **ERROR\_ALREADY\_EXISTS**, even though for this particular use-case it is not actually an error as such (if you intended to create a "new" (empty) file in place of the existing one).</span></span>

<span data-ttu-id="fd640-189">開啟現有的檔案時 (*dwCreationDisposition* 設定為 [ **開啟 \_ 現有** 的]、[ **\_ 永遠開啟**] 或 [ **截斷 \_ 現有** 的) ] 時， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="fd640-189">When opening an existing file (*dwCreationDisposition* set to either **OPEN\_EXISTING**, **OPEN\_ALWAYS**, or **TRUNCATE\_EXISTING**), the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function performs the following actions:</span></span>

-   <span data-ttu-id="fd640-190">檢查目前的檔案屬性和安全性設定是否有要求的存取權，失敗（若已拒絕）。</span><span class="sxs-lookup"><span data-stu-id="fd640-190">Checks current file attributes and security settings for requested access, failing if denied.</span></span>
-   <span data-ttu-id="fd640-191">將 _dwFlagsAndAttributes \* 指定的檔案旗標 (檔案 **\_ 旗 \_ \** 標 _) 與現有的檔案屬性結合，並忽略) \* 指定的任何檔案屬性 ( \* \* 檔 \_ 屬性 \_ \** _ _dwFlagsAndAttributes。</span><span class="sxs-lookup"><span data-stu-id="fd640-191">Combines the file flags (**FILE\_FLAG\_\** _) specified by _dwFlagsAndAttributes* with existing file attributes, and ignores any file attributes (**FILE\_ATTRIBUTE\_\** _) specified by _dwFlagsAndAttributes*.</span></span>
-   <span data-ttu-id="fd640-192">只有當 *dwCreationDisposition* 設定為 **截斷 \_ 現有** 的時，才會將檔案長度設定為零，否則會維護目前的檔案長度，並依原樣開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="fd640-192">Sets the file length to zero only if *dwCreationDisposition* is set to **TRUNCATE\_EXISTING**, otherwise the current file length is maintained and the file is opened as-is.</span></span>
-   <span data-ttu-id="fd640-193">忽略 *hTemplateFile* 參數。</span><span class="sxs-lookup"><span data-stu-id="fd640-193">Ignores the *hTemplateFile* parameter.</span></span>
-   <span data-ttu-id="fd640-194">設定 *lpSecurityAttributes* 參數的 **bInheritHandle** 成員所指定的繼承旗標 ([**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構) （如果有提供的話），但忽略 **安全性 \_ 屬性** 結構的 **lpSecurityDescriptor** 成員。</span><span class="sxs-lookup"><span data-stu-id="fd640-194">Sets the inherit flag specified by the **bInheritHandle** member of the *lpSecurityAttributes* parameter ([**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure) if supplied, but ignores the **lpSecurityDescriptor** member of the **SECURITY\_ATTRIBUTES** structure.</span></span>

## <a name="file-attributes-and-directories"></a><span data-ttu-id="fd640-195">檔案屬性和目錄</span><span class="sxs-lookup"><span data-stu-id="fd640-195">File Attributes and Directories</span></span>

<span data-ttu-id="fd640-196">檔案屬性是與檔案或目錄相關聯之中繼資料的一部分，而且每個屬性都有自己的用途，以及如何設定和變更的規則。</span><span class="sxs-lookup"><span data-stu-id="fd640-196">File attributes are part of the metadata associated with a file or directory, each with its own purpose and rules on how it can be set and changed.</span></span> <span data-ttu-id="fd640-197">其中有些屬性只適用于檔案，有些只適用于目錄。</span><span class="sxs-lookup"><span data-stu-id="fd640-197">Some of these attributes apply only to files, and some only to directories.</span></span> <span data-ttu-id="fd640-198">例如， **file \_ attribute \_ DIRECTORY** 屬性只適用于目錄：檔案系統會使用它來判斷磁片上的物件是否為目錄，但無法針對現有的檔案系統物件加以變更。</span><span class="sxs-lookup"><span data-stu-id="fd640-198">For example, the **FILE\_ATTRIBUTE\_DIRECTORY** attribute applies only to directories: It is used by the file system to determine whether an object on disk is a directory, but it cannot be changed for an existing file system object.</span></span>

<span data-ttu-id="fd640-199">某些檔案屬性可以設定為目錄，但只有在該目錄中建立的檔案才有意義，作為預設屬性。</span><span class="sxs-lookup"><span data-stu-id="fd640-199">Some file attributes can be set for a directory but have meaning only for files created in that directory, acting as default attributes.</span></span> <span data-ttu-id="fd640-200">例如，您可以在目錄物件上設定 **檔 \_ 屬性 \_ 壓縮** 的，但因為目錄物件本身不包含任何實際的資料，所以不會真正壓縮; 不過，以這個屬性標記的目錄會告訴檔案系統將任何新增的檔案壓縮到該目錄中。</span><span class="sxs-lookup"><span data-stu-id="fd640-200">For example, **FILE\_ATTRIBUTE\_COMPRESSED** can be set on a directory object, but because the directory object itself contains no actual data, it is not truly compressed; however, directories marked with this attribute tell the file system to compress any new files added to that directory.</span></span> <span data-ttu-id="fd640-201">可以在目錄上設定的任何檔案屬性，也會針對新增至該目錄的新檔案進行設定，稱為 *繼承的屬性*。</span><span class="sxs-lookup"><span data-stu-id="fd640-201">Any file attribute that can be set on a directory and will also be set for new files added to that directory is referred to as an *inherited attribute*.</span></span>

<span data-ttu-id="fd640-202">[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式會在建立檔案時，提供用來設定特定檔案屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="fd640-202">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function provides a parameter for setting certain file attributes when a file is created.</span></span> <span data-ttu-id="fd640-203">一般而言，這些屬性是應用程式在檔案建立時最常見的使用方式，但並非所有可能的檔案屬性都可供 **CreateFile**。</span><span class="sxs-lookup"><span data-stu-id="fd640-203">In general, these attributes are the most common for an application to use at file creation time, but not all possible file attributes are available to **CreateFile**.</span></span> <span data-ttu-id="fd640-204">某些檔案屬性需要在檔案已存在之後使用其他函式，例如 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)、 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)或 [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) 。</span><span class="sxs-lookup"><span data-stu-id="fd640-204">Some file attributes require the use of other functions, such as [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa), [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol), or [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) after the file already exists.</span></span> <span data-ttu-id="fd640-205">在 **檔 \_ 屬性 \_ 目錄** 的案例中， [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) 函數是在建立時需要的，因為 **CreateFile** 無法建立目錄。</span><span class="sxs-lookup"><span data-stu-id="fd640-205">In the case of **FILE\_ATTRIBUTE\_DIRECTORY**, the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) function is required at creation time because **CreateFile** cannot create directories.</span></span> <span data-ttu-id="fd640-206">其他需要特殊處理的檔案屬性是 **檔 \_ 屬性重新 \_ 分析 \_ 點** 和 **檔 \_ 屬性 \_ 的 \_ 稀疏** 檔案（需要 **DeviceIoControl**）。</span><span class="sxs-lookup"><span data-stu-id="fd640-206">The other file attributes that require special handling are **FILE\_ATTRIBUTE\_REPARSE\_POINT** and **FILE\_ATTRIBUTE\_SPARSE\_FILE**, which require **DeviceIoControl**.</span></span> <span data-ttu-id="fd640-207">如需詳細資訊，請參閱 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)。</span><span class="sxs-lookup"><span data-stu-id="fd640-207">For more information, see [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).</span></span>

<span data-ttu-id="fd640-208">如先前所述，當檔案建立時，會從檔案所在的目錄屬性讀取檔案屬性，以繼承檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="fd640-208">As stated previously, file attribute inheritance occurs when a file is created with file attributes read from the directory attributes where the file will be located.</span></span> <span data-ttu-id="fd640-209">下表摘要說明這些繼承的屬性，以及它們與 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 功能的關聯性。</span><span class="sxs-lookup"><span data-stu-id="fd640-209">The following table summarizes these inherited attributes and how they relate to [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) capabilities.</span></span>



| <span data-ttu-id="fd640-210">目錄屬性狀態</span><span class="sxs-lookup"><span data-stu-id="fd640-210">Directory attribute state</span></span>                                      | <span data-ttu-id="fd640-211">[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 新檔案的繼承覆寫功能</span><span class="sxs-lookup"><span data-stu-id="fd640-211">[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) inheritance override capability for new files</span></span>      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fd640-212">**檔案 \_屬性 \_ 壓縮** 集。</span><span class="sxs-lookup"><span data-stu-id="fd640-212">**FILE\_ATTRIBUTE\_COMPRESSED** set.</span></span><br/>                | <span data-ttu-id="fd640-213">沒有控制項。</span><span class="sxs-lookup"><span data-stu-id="fd640-213">No control.</span></span> <span data-ttu-id="fd640-214">使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 清除。</span><span class="sxs-lookup"><span data-stu-id="fd640-214">Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to clear.</span></span><br/>    |
| <span data-ttu-id="fd640-215">**檔案 \_未設定屬性 \_ 壓縮** 。</span><span class="sxs-lookup"><span data-stu-id="fd640-215">**FILE\_ATTRIBUTE\_COMPRESSED** not set.</span></span><br/>            | <span data-ttu-id="fd640-216">沒有控制項。</span><span class="sxs-lookup"><span data-stu-id="fd640-216">No control.</span></span> <span data-ttu-id="fd640-217">使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 設定。</span><span class="sxs-lookup"><span data-stu-id="fd640-217">Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to set.</span></span><br/>      |
| <span data-ttu-id="fd640-218">**檔案 \_屬性 \_ 加密** 集。</span><span class="sxs-lookup"><span data-stu-id="fd640-218">**FILE\_ATTRIBUTE\_ENCRYPTED** set.</span></span><br/>                 | <span data-ttu-id="fd640-219">沒有控制項。</span><span class="sxs-lookup"><span data-stu-id="fd640-219">No control.</span></span> <span data-ttu-id="fd640-220">使用 [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea)。</span><span class="sxs-lookup"><span data-stu-id="fd640-220">Use [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).</span></span><br/>                      |
| <span data-ttu-id="fd640-221">**檔案 \_未設定屬性 \_ 加密** 。</span><span class="sxs-lookup"><span data-stu-id="fd640-221">**FILE\_ATTRIBUTE\_ENCRYPTED** not set.</span></span><br/>             | <span data-ttu-id="fd640-222">可以使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)來設定。</span><span class="sxs-lookup"><span data-stu-id="fd640-222">Can be set using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span><br/>                       |
| <span data-ttu-id="fd640-223">**檔案 \_屬性 \_ 不是 \_ 內容 \_ 索引** 集。</span><span class="sxs-lookup"><span data-stu-id="fd640-223">**FILE\_ATTRIBUTE\_NOT\_CONTENT\_INDEXED** set.</span></span><br/>     | <span data-ttu-id="fd640-224">沒有控制項。</span><span class="sxs-lookup"><span data-stu-id="fd640-224">No control.</span></span> <span data-ttu-id="fd640-225">使用 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) 清除。</span><span class="sxs-lookup"><span data-stu-id="fd640-225">Use [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) to clear.</span></span><br/> |
| <span data-ttu-id="fd640-226">**檔案 \_未 \_ 設定 \_ 內容 \_ 編制索引的屬性** 。</span><span class="sxs-lookup"><span data-stu-id="fd640-226">**FILE\_ATTRIBUTE\_NOT\_CONTENT\_INDEXED** not set.</span></span><br/> | <span data-ttu-id="fd640-227">沒有控制項。</span><span class="sxs-lookup"><span data-stu-id="fd640-227">No control.</span></span> <span data-ttu-id="fd640-228">使用 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) 設定。</span><span class="sxs-lookup"><span data-stu-id="fd640-228">Use [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) to set.</span></span><br/>   |



 

## <a name="related-topics"></a><span data-ttu-id="fd640-229">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd640-229">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd640-230">存取控制</span><span class="sxs-lookup"><span data-stu-id="fd640-230">Access Control</span></span>](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[<span data-ttu-id="fd640-231">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="fd640-231">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="fd640-232">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="fd640-232">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="fd640-233">**檔案屬性常數**</span><span class="sxs-lookup"><span data-stu-id="fd640-233">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> <dt>

[<span data-ttu-id="fd640-234">檔案壓縮和解壓縮</span><span class="sxs-lookup"><span data-stu-id="fd640-234">File Compression and Decompression</span></span>](file-compression-and-decompression.md)
</dt> <dt>

[<span data-ttu-id="fd640-235">檔案加密</span><span class="sxs-lookup"><span data-stu-id="fd640-235">File Encryption</span></span>](file-encryption.md)
</dt> <dt>

[<span data-ttu-id="fd640-236">檔案管理功能</span><span class="sxs-lookup"><span data-stu-id="fd640-236">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="fd640-237">控制碼和物件</span><span class="sxs-lookup"><span data-stu-id="fd640-237">Handles and Objects</span></span>](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[<span data-ttu-id="fd640-238">處理繼承</span><span class="sxs-lookup"><span data-stu-id="fd640-238">Handle Inheritance</span></span>](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[<span data-ttu-id="fd640-239">開啟檔案進行讀取或寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-239">Opening a File for Reading or Writing</span></span>](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[<span data-ttu-id="fd640-240">**SetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="fd640-240">**SetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

