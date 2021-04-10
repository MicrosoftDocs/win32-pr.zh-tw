---
title: 檔案和資料流程處理常式安裝
description: 檔案和資料流程處理常式安裝
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675264"
---
# <a name="file-and-stream-handler-installation"></a><span data-ttu-id="8028b-103">檔案和資料流程處理常式安裝</span><span class="sxs-lookup"><span data-stu-id="8028b-103">File and Stream Handler Installation</span></span>

<span data-ttu-id="8028b-104">AVIFile 程式庫會使用已安裝的資料流程和檔案處理常式，來讀取和寫入 AVI 檔案和資料流程。</span><span class="sxs-lookup"><span data-stu-id="8028b-104">The AVIFile library uses installed stream and file handlers for reading and writing AVI files and streams.</span></span> <span data-ttu-id="8028b-105">當處理常式位於 Windows 系統目錄中，且登錄包含描述和識別處理常式所需的下列資訊時，便會安裝處理常式：</span><span class="sxs-lookup"><span data-stu-id="8028b-105">A handler is installed when it resides in the Windows SYSTEM directory and the registry contains the following information needed to describe and identify a handler:</span></span>

-   <span data-ttu-id="8028b-106">處理常式的16位元組類別識別碼</span><span class="sxs-lookup"><span data-stu-id="8028b-106">The 16-byte class identifier for the handler</span></span>
-   <span data-ttu-id="8028b-107">處理常式的簡短描述</span><span class="sxs-lookup"><span data-stu-id="8028b-107">A brief description of the handler</span></span>
-   <span data-ttu-id="8028b-108">包含處理常式的檔案名</span><span class="sxs-lookup"><span data-stu-id="8028b-108">The name of the file containing the handler</span></span>
-   <span data-ttu-id="8028b-109">檔處理常式可以處理的副檔名</span><span class="sxs-lookup"><span data-stu-id="8028b-109">The file extension that a file handler can process</span></span>
-   <span data-ttu-id="8028b-110">檔案存取以及與檔案處理常式相關聯的其他屬性</span><span class="sxs-lookup"><span data-stu-id="8028b-110">File-access and other properties associated with a file handler</span></span>
-   <span data-ttu-id="8028b-111">四個字元的代碼，可識別串流處理常式可以處理的資料流程類型</span><span class="sxs-lookup"><span data-stu-id="8028b-111">Four-character codes identifying stream types that a stream handler can process</span></span>

<span data-ttu-id="8028b-112">AVIFile 程式庫會在開啟檔案和存取資料流程時，查詢應用程式外部的處理常式。</span><span class="sxs-lookup"><span data-stu-id="8028b-112">The AVIFile library queries the registry for handlers that are external to an application when opening files and accessing streams.</span></span> <span data-ttu-id="8028b-113">成功查詢的結果會傳回可處理查詢中所指定之檔案或資料流程類型的處理常式檔案名。</span><span class="sxs-lookup"><span data-stu-id="8028b-113">The result of a successful query returns the filename of a handler that can process the file or stream type specified in the query.</span></span> <span data-ttu-id="8028b-114">登錄會建立具有下列格式的三個專案，以列出每個處理常式：</span><span class="sxs-lookup"><span data-stu-id="8028b-114">The registry lists each handler by creating three entries that have the following form:</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



<span data-ttu-id="8028b-115">這些專案是由下列部分所組成。</span><span class="sxs-lookup"><span data-stu-id="8028b-115">These entries consist of the following parts.</span></span>



| <span data-ttu-id="8028b-116">部分</span><span class="sxs-lookup"><span data-stu-id="8028b-116">Part</span></span>                                   | <span data-ttu-id="8028b-117">描述</span><span class="sxs-lookup"><span data-stu-id="8028b-117">Description</span></span>                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8028b-118">HKEY \_ 類別 \_ 根目錄</span><span class="sxs-lookup"><span data-stu-id="8028b-118">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="8028b-119">識別登錄的根專案。</span><span class="sxs-lookup"><span data-stu-id="8028b-119">Identifies the root entry of the registry.</span></span>                                                                                                                                               |
| <span data-ttu-id="8028b-120">Clsid</span><span class="sxs-lookup"><span data-stu-id="8028b-120">Clsid</span></span>                                  | <span data-ttu-id="8028b-121">將此專案識別為類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-121">Identifies this entry as a class identifier.</span></span>                                                                                                                                             |
| <span data-ttu-id="8028b-122">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="8028b-122">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="8028b-123">指定 (IID) 或類別識別碼的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-123">Specifies an interface identifier (IID) or class identifier.</span></span> <span data-ttu-id="8028b-124">此值是唯一的16位元組識別碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-124">This value is a unique 16-byte identifier.</span></span> <span data-ttu-id="8028b-125"> (識別碼也可能在其他手冊中稱為 GUID 或 UUID。 ) </span><span class="sxs-lookup"><span data-stu-id="8028b-125">(The identifier might also be referred to as a GUID or a UUID in other manuals.)</span></span> |
| <span data-ttu-id="8028b-126">Wave 檔案讀取器/寫入器</span><span class="sxs-lookup"><span data-stu-id="8028b-126">Wave File reader/writer</span></span>                | <span data-ttu-id="8028b-127">指定描述處理常式的字串。</span><span class="sxs-lookup"><span data-stu-id="8028b-127">Specifies a string to describe the handler.</span></span> <span data-ttu-id="8028b-128">您可以在對話方塊中顯示此字串，以選取資料流程和檔案處理常式。</span><span class="sxs-lookup"><span data-stu-id="8028b-128">This string can be displayed in dialog boxes for selecting stream and file handlers.</span></span>                                                         |
| <span data-ttu-id="8028b-129">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="8028b-129">InProcServer32</span></span>                         | <span data-ttu-id="8028b-130">指定此範例中的檔案 (，WAVEFILE.DLL 可載入以處理這個類別的) 。</span><span class="sxs-lookup"><span data-stu-id="8028b-130">Specifies the file (in this example, WAVEFILE.DLL) that can be loaded to handle this class.</span></span>                                                                                              |
| <span data-ttu-id="8028b-131">AVIFile</span><span class="sxs-lookup"><span data-stu-id="8028b-131">AVIFile</span></span>                                | <span data-ttu-id="8028b-132">指定檔案處理常式的屬性。</span><span class="sxs-lookup"><span data-stu-id="8028b-132">Specifies the properties of a file handler.</span></span> <span data-ttu-id="8028b-133">在此範例中，處理常式可以讀取和寫入 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="8028b-133">In this example, the handler can read and write to an AVI file.</span></span>                                                                              |



 

<span data-ttu-id="8028b-134">檔案處理常式可以將其一或多個屬性儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="8028b-134">A file handler can have one or more of its properties stored in the registry.</span></span> <span data-ttu-id="8028b-135">下列常數會識別目前與檔案相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="8028b-135">The following constants identify the properties currently associated with a file.</span></span>



| <span data-ttu-id="8028b-136">常數</span><span class="sxs-lookup"><span data-stu-id="8028b-136">Constant</span></span>                        | <span data-ttu-id="8028b-137">描述</span><span class="sxs-lookup"><span data-stu-id="8028b-137">Description</span></span>                                                          |
|---------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="8028b-138">AVIFILEHANDLER \_ CANACCEPTNONRGB</span><span class="sxs-lookup"><span data-stu-id="8028b-138">AVIFILEHANDLER\_CANACCEPTNONRGB</span></span> | <span data-ttu-id="8028b-139">指出檔案處理常式可以處理 RGB 以外的影像資料。</span><span class="sxs-lookup"><span data-stu-id="8028b-139">Indicates that a file handler can process image data other than RGB.</span></span> |
| <span data-ttu-id="8028b-140">AVIFILEHANDLER \_ CANREAD</span><span class="sxs-lookup"><span data-stu-id="8028b-140">AVIFILEHANDLER\_CANREAD</span></span>         | <span data-ttu-id="8028b-141">指出檔案處理常式可以開啟具有讀取權限的檔案。</span><span class="sxs-lookup"><span data-stu-id="8028b-141">Indicates that a file handler can open a file with read access.</span></span>      |
| <span data-ttu-id="8028b-142">AVIFILEHANDLER \_ CANWRITE</span><span class="sxs-lookup"><span data-stu-id="8028b-142">AVIFILEHANDLER\_CANWRITE</span></span>        | <span data-ttu-id="8028b-143">指出檔案處理常式可以開啟具有寫入權限的檔案。</span><span class="sxs-lookup"><span data-stu-id="8028b-143">Indicates that a file handler can open a file with write access.</span></span>     |



 

<span data-ttu-id="8028b-144">建立檔案或資料流程處理常式時，您可以藉由執行 UUIDGEN.EXE 來取得新的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-144">When creating a file or stream handler, you can obtain a new identifier by running UUIDGEN.EXE.</span></span> <span data-ttu-id="8028b-145">請一律使用 UUIDGEN.EXE 來建立新的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-145">Always use UUIDGEN.EXE to create a new identifier.</span></span> <span data-ttu-id="8028b-146">這個可執行檔所建立的16位元組十六進位數位將會唯一識別您的處理常式。</span><span class="sxs-lookup"><span data-stu-id="8028b-146">The 16-byte hexadecimal number created by this executable will uniquely identify your handler.</span></span>

<span data-ttu-id="8028b-147">AVIFile 程式庫會使用登錄中的其他專案，根據檔案處理常式可以處理的副檔名，或是檔案或資料流程處理常式可以處理的四字元程式碼來識別類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-147">The AVIFile library uses additional entries in the registry to identify a class identifier based on the file extension that a file handler can process or a four-character code that a file or stream handler can process.</span></span> <span data-ttu-id="8028b-148">例如，下列專案會將類別識別碼與副檔名產生關聯。WAV 和四個字元的代碼「WAVE」：</span><span class="sxs-lookup"><span data-stu-id="8028b-148">For example, the following entries associate a class identifier with the file extension .WAV and the four-character code "WAVE":</span></span>


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



<span data-ttu-id="8028b-149">這些專案是由下列部分所組成。</span><span class="sxs-lookup"><span data-stu-id="8028b-149">These entries consist of the following parts.</span></span>



| <span data-ttu-id="8028b-150">部分</span><span class="sxs-lookup"><span data-stu-id="8028b-150">Part</span></span>                                   | <span data-ttu-id="8028b-151">描述</span><span class="sxs-lookup"><span data-stu-id="8028b-151">Description</span></span>                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8028b-152">HKEY \_ 類別 \_ 根目錄</span><span class="sxs-lookup"><span data-stu-id="8028b-152">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="8028b-153">識別登錄的根專案。</span><span class="sxs-lookup"><span data-stu-id="8028b-153">Identifies the root entry of the registry.</span></span>                                                        |
| <span data-ttu-id="8028b-154">AVIFile</span><span class="sxs-lookup"><span data-stu-id="8028b-154">AVIFile</span></span>                                | <span data-ttu-id="8028b-155">將此專案識別為 AVIFile 所使用的專案。</span><span class="sxs-lookup"><span data-stu-id="8028b-155">Identifies this entry as an entry used by AVIFile.</span></span>                                                |
| <span data-ttu-id="8028b-156">延伸模組</span><span class="sxs-lookup"><span data-stu-id="8028b-156">Extensions</span></span>                             | <span data-ttu-id="8028b-157">指定在此範例中 (的副檔名。檔案處理常式可以處理的 WAV) 。</span><span class="sxs-lookup"><span data-stu-id="8028b-157">Specifies the file extension (in this example, .WAV) that a file handler can process.</span></span>             |
| <span data-ttu-id="8028b-158">RIFFHandlers</span><span class="sxs-lookup"><span data-stu-id="8028b-158">RIFFHandlers</span></span>                           | <span data-ttu-id="8028b-159">指定此範例中的四個字元的程式碼 ("WAVE" ) 檔案或資料流程處理常式可以處理。</span><span class="sxs-lookup"><span data-stu-id="8028b-159">Specifies the four-character code (in this example, "WAVE") a file or stream handler can process.</span></span> |
| <span data-ttu-id="8028b-160">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="8028b-160">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="8028b-161">指定 (IID) 或類別識別碼的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-161">Specifies an interface identifier (IID) or class identifier.</span></span>                                      |



 

<span data-ttu-id="8028b-162">如果您在沒有安裝程式的情況下散發資料流程或檔案處理常式，以便將它安裝在使用者的系統中，則必須包含。REG 檔案，讓使用者可以安裝處理常式。</span><span class="sxs-lookup"><span data-stu-id="8028b-162">If you distribute your stream or file handler without a setup application to install it in the user's system, you must include a .REG file so the user can install the handler.</span></span> <span data-ttu-id="8028b-163">使用者將使用登錄編輯程式來建立您的資料流程或檔案處理常式的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="8028b-163">The user will use the registry editor to create registry entries for your stream or file handler.</span></span>

<span data-ttu-id="8028b-164">下列範例顯示一般的內容。REG 檔。</span><span class="sxs-lookup"><span data-stu-id="8028b-164">The following example shows the contents of a typical .REG file.</span></span> <span data-ttu-id="8028b-165">下列範例中的第一個專案是處理常式的描述字串。</span><span class="sxs-lookup"><span data-stu-id="8028b-165">The first entry in the following example is the descriptive string for the handler.</span></span> <span data-ttu-id="8028b-166">第二個專案會識別包含處理常式的檔案。</span><span class="sxs-lookup"><span data-stu-id="8028b-166">The second entry identifies the file containing the handler.</span></span> <span data-ttu-id="8028b-167">第三個專案會識別檔案處理常式的屬性 (在此案例中為檔案) 的唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="8028b-167">The third entry identifies the properties of the file handler (in this case, read-only access to files).</span></span> <span data-ttu-id="8028b-168">第四個專案會將處理常式所處理的檔案類型與在此案例中的檔案產生關聯 (。JPG 檔案名延伸) 具有類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-168">The fourth entry associates the type of file the handler processes (in this case, files with a .JPG filename extension) with the class identifier.</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



<span data-ttu-id="8028b-169">建立此檔案時，請將它儲存為。登錄延伸模組，用來將它識別為登錄的更新檔案。</span><span class="sxs-lookup"><span data-stu-id="8028b-169">When creating this file, save it with a .REG extension to identify it as an update file for the registry.</span></span> <span data-ttu-id="8028b-170">此外，請以唯一的 IID 取代範例中所用的16位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="8028b-170">Also, substitute a unique IID for the 16-byte code used in the example.</span></span>

 

 




