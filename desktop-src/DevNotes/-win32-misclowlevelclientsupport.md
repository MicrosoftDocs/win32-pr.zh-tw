---
description: 本主題包含 Windows 用戶端基礎結構所使用之低層級 Api 的相關資訊。
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: 其他 Low-Level 用戶端支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846916"
---
# <a name="miscellaneous-low-level-client-support"></a><span data-ttu-id="b96b2-103">其他 Low-Level 用戶端支援</span><span class="sxs-lookup"><span data-stu-id="b96b2-103">Miscellaneous Low-Level Client Support</span></span>

<span data-ttu-id="b96b2-104">本主題包含 Windows 用戶端基礎結構所使用之低層級 Api 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b96b2-104">This topic contains information about low-level APIs that are used by the Windows client infrastructure.</span></span>

### <a name="functions"></a><span data-ttu-id="b96b2-105">函式</span><span class="sxs-lookup"><span data-stu-id="b96b2-105">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b96b2-106">主題</span><span class="sxs-lookup"><span data-stu-id="b96b2-106">Topic</span></span></th>
<th><span data-ttu-id="b96b2-107">目錄</span><span class="sxs-lookup"><span data-stu-id="b96b2-107">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b96b2-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-109">_Lclose 函式會關閉指定的檔案，使其無法再供讀取或寫入。</span><span class="sxs-lookup"><span data-stu-id="b96b2-109">The _lclose function closes the specified file so that it is no longer available for reading or writing.</span></span> <span data-ttu-id="b96b2-110">這個函式是為了與16位版本的 Windows 相容而提供。</span><span class="sxs-lookup"><span data-stu-id="b96b2-110">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="b96b2-111">以 Win32 為基礎的應用程式應該使用 CloseHandle 函數。</span><span class="sxs-lookup"><span data-stu-id="b96b2-111">Win32-based applications should use the CloseHandle function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-113">_Lopen 函式會開啟現有的檔案，並將檔案指標設定為檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="b96b2-113">The _lopen function opens an existing file and sets the file pointer to the beginning of the file.</span></span> <span data-ttu-id="b96b2-114">這個函式是為了與16位版本的 Windows 相容而提供。</span><span class="sxs-lookup"><span data-stu-id="b96b2-114">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="b96b2-115">以 Win32 為基礎的應用程式應該使用 CreateFile 函數。</span><span class="sxs-lookup"><span data-stu-id="b96b2-115">Win32-based applications should use the CreateFile function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-117">_Lread 函數會從指定的檔案讀取資料。</span><span class="sxs-lookup"><span data-stu-id="b96b2-117">The _lread function reads data from the specified file.</span></span> <span data-ttu-id="b96b2-118">這個函式是為了與16位版本的 Windows 相容而提供。</span><span class="sxs-lookup"><span data-stu-id="b96b2-118">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="b96b2-119">以 Win32 為基礎的應用程式應該使用 ReadFile 函數。</span><span class="sxs-lookup"><span data-stu-id="b96b2-119">Win32-based applications should use the ReadFile function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-121">傳回值，這個值表示是否已在目前的裝置上啟用 DVD 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="b96b2-121">Returns a value indicating whether DVD codecs are enabled on the current device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-123">停用呼叫 GUI 進程的視窗重影功能。</span><span class="sxs-lookup"><span data-stu-id="b96b2-123">Disables the window ghosting feature for the calling GUI process.</span></span> <span data-ttu-id="b96b2-124">視窗重影是 Windows Manager 的功能，可讓使用者將沒有回應的應用程式主視窗最小化、移動或關閉。</span><span class="sxs-lookup"><span data-stu-id="b96b2-124">Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-126">針對安裝在符合指定需求之系統上的所有媒體編解碼器，傳回屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="b96b2-126">Returns a list of properties for all media codecs installed on the system that meet the specified requirements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-128">建立用來註冊媒體擴充功能的通訊 factory。</span><span class="sxs-lookup"><span data-stu-id="b96b2-128">Creates a communication factory for registering a media extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-130">在應用程式封裝中建立類別的實例。</span><span class="sxs-lookup"><span data-stu-id="b96b2-130">Creates an instance of a class in an application package.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-132">取得值，這個值表示是否已啟用與指定 GUID 相關聯的媒體行為。</span><span class="sxs-lookup"><span data-stu-id="b96b2-132">Gets a value indicating whether the media behavior associated with the specified GUID is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-134">已取代。</span><span class="sxs-lookup"><span data-stu-id="b96b2-134">Deprecated.</span></span> <span data-ttu-id="b96b2-135">此函數可用來關閉指定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b96b2-135">This function is used to close the specified handle.</span></span> <span data-ttu-id="b96b2-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> 被 <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>取代。</span><span class="sxs-lookup"><span data-stu-id="b96b2-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> is superseded by <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-138">已取代。</span><span class="sxs-lookup"><span data-stu-id="b96b2-138">Deprecated.</span></span> <span data-ttu-id="b96b2-139">為提供的緩衝區 (的) 建立描述項，並將不具類型的資料傳遞至與檔案控制代碼相關聯的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b96b2-139">Builds descriptors for the supplied buffer(s) and passes the untyped data to the device driver associated with the file handle.</span></span> <span data-ttu-id="b96b2-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> 被 <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>取代。</span><span class="sxs-lookup"><span data-stu-id="b96b2-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> is superseded by <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-142">已取代。</span><span class="sxs-lookup"><span data-stu-id="b96b2-142">Deprecated.</span></span> <span data-ttu-id="b96b2-143">等到指定的物件並達到狀態為止 <code>signaled</code> 。</span><span class="sxs-lookup"><span data-stu-id="b96b2-143">Waits until the specified object attains a state of <code>signaled</code>.</span></span> <span data-ttu-id="b96b2-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> 被 <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>取代。</span><span class="sxs-lookup"><span data-stu-id="b96b2-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> is superseded by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-146">將指定的 ANSI 來源字串轉換成 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="b96b2-146">Converts the specified ANSI source string into a Unicode string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-148">將字元字串轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="b96b2-148">Converts a character string to an integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-150">使用目前使用者之 SID 的字串表示，初始化提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b96b2-150">Initializes the supplied buffer with a string representation of the SID for the current user.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-152">釋放 <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>所配置的字串緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b96b2-152">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-154">釋放 <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>所配置的字串緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b96b2-154">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-156">釋放 <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> 或 <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>所配置的字串緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b96b2-156">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> or by <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-158">初始化已計算的字串。</span><span class="sxs-lookup"><span data-stu-id="b96b2-158">Initializes a counted string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-160">初始化已計算的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="b96b2-160">Initializes a counted Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-162">將指定的 Unicode 來源字串轉換成 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="b96b2-162">Converts the specified Unicode source string into an ANSI string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-164">此函數會將指定的 Unicode 來源字串轉換成 OEM 字串。</span><span class="sxs-lookup"><span data-stu-id="b96b2-164">This functions converts the specified Unicode source string into an OEM string.</span></span> <span data-ttu-id="b96b2-165">這項翻譯是與 OEM 字碼頁 (OCP) 相關。</span><span class="sxs-lookup"><span data-stu-id="b96b2-165">The translation is done with respect to the OEM code page (OCP).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-167">決定將 Unicode 字串表示為 ANSI 字串所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b96b2-167">Determines how many bytes are needed to represent a Unicode string as an ANSI string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-169"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a>函式會使用8位 Unicode 轉換格式 (utf-8) 字碼頁，將指定的 unicode 字串轉譯成新的字元字串。</span><span class="sxs-lookup"><span data-stu-id="b96b2-169">The <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> function translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-171"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a>函式會使用 utf-8 字碼頁，將指定的來源字串轉譯成 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="b96b2-171">The <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> function translates the specified source string into a Unicode string, using the UTF-8 code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b96b2-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-173">透過指定的子，指定輸入方法編輯器 (IME) 的動作或處理。</span><span class="sxs-lookup"><span data-stu-id="b96b2-173">Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b96b2-174">此函式已過時，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="b96b2-174">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b96b2-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="b96b2-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span></span></td>
<td><span data-ttu-id="b96b2-176">暫時啟用或停用 IME，同時開啟或關閉 IME 所擁有之所有視窗的顯示。</span><span class="sxs-lookup"><span data-stu-id="b96b2-176">Temporarily enables or disables an IME and, at the same time, turns on or off the display of all windows owned by the IME.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b96b2-177">此函式已過時，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="b96b2-177">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a><span data-ttu-id="b96b2-178">結構</span><span class="sxs-lookup"><span data-stu-id="b96b2-178">Structures</span></span>



| <span data-ttu-id="b96b2-179">主題</span><span class="sxs-lookup"><span data-stu-id="b96b2-179">Topic</span></span>                                 | <span data-ttu-id="b96b2-180">目錄</span><span class="sxs-lookup"><span data-stu-id="b96b2-180">Contents</span></span>                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b96b2-181">**IMESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="b96b2-181">**IMESTRUCT**</span></span>](/windows/win32/api/ime/ns-ime-imestruct) | <span data-ttu-id="b96b2-182">[**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa)用來指定要在 IME 訊息及其參數中執行的子。</span><span class="sxs-lookup"><span data-stu-id="b96b2-182">Used by [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) to specify the subfunction to be executed in the IME message and its parameters.</span></span> <span data-ttu-id="b96b2-183">此結構也用來接收來自這些稱為的傳回值。</span><span class="sxs-lookup"><span data-stu-id="b96b2-183">This structure is also used to receive return values from those subfunctions.</span></span><br/> |
| [<span data-ttu-id="b96b2-184">**字串**</span><span class="sxs-lookup"><span data-stu-id="b96b2-184">**STRING**</span></span>](/windows/desktop/api/Winternl/ns-winternl-string)       | <span data-ttu-id="b96b2-185">此結構會與 [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b96b2-185">This structure is used with the [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) function.</span></span> <br/>                                                                                                              |



 

### <a name="compiler-routines"></a><span data-ttu-id="b96b2-186">編譯器常式</span><span class="sxs-lookup"><span data-stu-id="b96b2-186">Compiler Routines</span></span>



| <span data-ttu-id="b96b2-187">主題</span><span class="sxs-lookup"><span data-stu-id="b96b2-187">Topic</span></span>                                                             | <span data-ttu-id="b96b2-188">目錄</span><span class="sxs-lookup"><span data-stu-id="b96b2-188">Contents</span></span>                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b96b2-189">**\_\_C \_ 特定 \_ 處理常式常式**</span><span class="sxs-lookup"><span data-stu-id="b96b2-189">**\_\_C\_specific\_handler Routine**</span></span>](--c-specific-handler2.md) | <span data-ttu-id="b96b2-190">[**\_ \_ C \_ 特定 \_ 處理常式**](--c-specific-handler2.md)是 c 編譯器的 helper 常式。</span><span class="sxs-lookup"><span data-stu-id="b96b2-190">[**\_\_C\_specific\_handler**](--c-specific-handler2.md) is a helper routine for the C compiler.</span></span><br/> |
| [<span data-ttu-id="b96b2-191">\_alldiv 常式</span><span class="sxs-lookup"><span data-stu-id="b96b2-191">\_alldiv Routine</span></span>](-win32-alldiv.md)                             | <span data-ttu-id="b96b2-192">[ \_ alldiv 常式](-win32-alldiv.md)是 C 編譯器的 helper 常式。</span><span class="sxs-lookup"><span data-stu-id="b96b2-192">[\_alldiv Routine](-win32-alldiv.md) is a helper routine for the C compiler.</span></span><br/>                     |
| [<span data-ttu-id="b96b2-193">\_allmul</span><span class="sxs-lookup"><span data-stu-id="b96b2-193">\_allmul</span></span>](-win32-allmul.md) | <span data-ttu-id="b96b2-194">將兩個 **LONGLONG** 或 **ULONGLONG** 相乘。</span><span class="sxs-lookup"><span data-stu-id="b96b2-194">Multiplies two **LONGLONG** or **ULONGLONG**.</span></span> |
| [<span data-ttu-id="b96b2-195">\_aulldiv</span><span class="sxs-lookup"><span data-stu-id="b96b2-195">\_aulldiv</span></span>](-win32-aulldiv.md) | <span data-ttu-id="b96b2-196">將兩個 **ULONGLONG** 整數相除。</span><span class="sxs-lookup"><span data-stu-id="b96b2-196">Divides two **ULONGLONG** integers.</span></span> |
| [<span data-ttu-id="b96b2-197">\_chkstk 常式</span><span class="sxs-lookup"><span data-stu-id="b96b2-197">\_chkstk Routine</span></span>](-win32-chkstk.md)                             | <span data-ttu-id="b96b2-198">[ \_ chkstk 常式](-win32-chkstk.md)是 C 編譯器的 helper 常式。</span><span class="sxs-lookup"><span data-stu-id="b96b2-198">[\_chkstk Routine](-win32-chkstk.md) is a helper routine for the C compiler.</span></span><br/>                     |
