---
title: 列舉檔案和目錄
description: 描述 ProjFS 提供者如何參與目錄列舉。
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2020
ms.locfileid: "103681530"
---
# <a name="enumerating-files-and-directories"></a><span data-ttu-id="e246d-103">列舉檔案和目錄</span><span class="sxs-lookup"><span data-stu-id="e246d-103">Enumerating Files and Directories</span></span>

<span data-ttu-id="e246d-104">當提供者先建立虛擬化根時，本機系統上就會是空的。</span><span class="sxs-lookup"><span data-stu-id="e246d-104">When a provider first creates a virtualization root it is empty on the local system.</span></span>  <span data-ttu-id="e246d-105">也就是說，支援資料存放區中的所有專案都尚未快取到磁片。</span><span class="sxs-lookup"><span data-stu-id="e246d-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span>  <span data-ttu-id="e246d-106">開啟每個專案時，它會快取，但在專案開啟之前，它只存在於支援資料存放區中。</span><span class="sxs-lookup"><span data-stu-id="e246d-106">As each item is opened it is cached, but until an item is opened it only exists in the backing data store.</span></span>

<span data-ttu-id="e246d-107">因為未開啟的專案沒有本機存在，所以一般目錄列舉不會向使用者顯示其存在。</span><span class="sxs-lookup"><span data-stu-id="e246d-107">Since unopened items have no local presence, normal directory enumeration would not reveal their existence to the user.</span></span>  <span data-ttu-id="e246d-108">因此，提供者必須將有關其支援資料存放區中專案的資訊傳回給 ProjFS，以參與目錄列舉。</span><span class="sxs-lookup"><span data-stu-id="e246d-108">Therefore the provider must participate in directory enumeration by returning information to ProjFS about items in its backing data store.</span></span>  <span data-ttu-id="e246d-109">ProjFS 會將來自提供者的資訊與本機檔案系統上的內容合併，以提供給使用者，以統一的目錄內容清單呈現給使用者。</span><span class="sxs-lookup"><span data-stu-id="e246d-109">ProjFS merges the information from the provider with what is on the local file system to present to the user a unified list of the contents of a directory.</span></span>

## <a name="directory-enumeration-callbacks"></a><span data-ttu-id="e246d-110">目錄列舉回呼</span><span class="sxs-lookup"><span data-stu-id="e246d-110">Directory Enumeration Callbacks</span></span>

<span data-ttu-id="e246d-111">若要參與目錄列舉，提供者必須執行 **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**、 **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** 和 **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** 回呼。</span><span class="sxs-lookup"><span data-stu-id="e246d-111">To participate in directory enumeration the provider must implement the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)**, and **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** callbacks.</span></span>  <span data-ttu-id="e246d-112">列舉提供者之虛擬化根下的目錄時，ProjFS 會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e246d-112">When a directory under the provider's virtualization root gets enumerated, ProjFS performs the following actions:</span></span>

1. <span data-ttu-id="e246d-113">ProjFS 會呼叫提供者的 **PRJ_START_DIRECTORY_ENUMERATION_CB** 回呼，以啟動列舉會話。</span><span class="sxs-lookup"><span data-stu-id="e246d-113">ProjFS calls the provider's **PRJ_START_DIRECTORY_ENUMERATION_CB** callback to start an enumeration session.</span></span>

    <span data-ttu-id="e246d-114">在處理此回呼的過程中，提供者應該準備執行列舉。</span><span class="sxs-lookup"><span data-stu-id="e246d-114">As part of processing this callback the provider should prepare to perform the enumeration.</span></span>  <span data-ttu-id="e246d-115">例如，它應該配置任何記憶體，它可能需要在其支援資料存放區中追蹤列舉的進度。</span><span class="sxs-lookup"><span data-stu-id="e246d-115">For example, it should allocate any memory it may need to track the progress of the enumeration in its backing data store.</span></span>

    <span data-ttu-id="e246d-116">ProjFS 會識別在回呼的 _callbackData_ 參數的 **FilePathName** 成員中列舉的目錄。</span><span class="sxs-lookup"><span data-stu-id="e246d-116">ProjFS identifies the directory being enumerated in the **FilePathName** member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="e246d-117">這會指定為相對於虛擬化根的路徑。</span><span class="sxs-lookup"><span data-stu-id="e246d-117">This is specified as a path relative to the virtualization root.</span></span>  <span data-ttu-id="e246d-118">例如，如果虛擬化根位於 `C:\virtRoot` ，且要列舉的目錄是 `C:\virtRoot\dir1\dir2` ，則 **FilePathName** 成員會包含 `dir1\dir2` 。</span><span class="sxs-lookup"><span data-stu-id="e246d-118">For example, if the virtualization root is located at `C:\virtRoot`, and the directory being enumerated is `C:\virtRoot\dir1\dir2`, the **FilePathName** member will contain `dir1\dir2`.</span></span>  <span data-ttu-id="e246d-119">提供者將準備在其支援資料存放區中列舉該路徑。</span><span class="sxs-lookup"><span data-stu-id="e246d-119">The provider will prepare to enumerate that path in its backing data store.</span></span>  <span data-ttu-id="e246d-120">視提供者備份存放區的功能而定，在 **PRJ_START_DIRECTORY_ENUMERATION_CB** 回呼中執行備份存放區列舉可能是合理的。</span><span class="sxs-lookup"><span data-stu-id="e246d-120">Depending on the capabilities of a provider's backing store it may make sense to perform the backing store enumeration in the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback.</span></span>

    <span data-ttu-id="e246d-121">由於多個列舉可能會在相同的目錄中平行執行，因此每個列舉回呼都有一個 _enumerationId_ 引數，可讓提供者將回呼調用與單一列舉會話產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e246d-121">Because multiple enumerations may occur in parallel in the same directory, each enumeration callback has an _enumerationId_ argument to enable the provider to associate the callback invocations into a single enumeration session.</span></span>

    <span data-ttu-id="e246d-122">如果提供者從 **PRJ_START_DIRECTORY_ENUMERATION_CB** 回呼傳回 S_OK，它必須在 ProjFS 叫用具有相同 _enumerationId_ 值的 **PRJ_END_DIRECTORY_ENUMERATION_CB** 回呼之前，維持它所擁有的任何列舉會話資訊。</span><span class="sxs-lookup"><span data-stu-id="e246d-122">If the provider returns S_OK from the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback, it must maintain any enumeration session information it has until ProjFS invokes the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback with the same value for _enumerationId_.</span></span>  <span data-ttu-id="e246d-123">如果提供者從 **PRJ_START_DIRECTORY_ENUMERATION_CB** 傳回錯誤，則 ProjFS 將不會叫用該 _enumerationId_ 的 **PRJ_END_DIRECTORY_ENUMERATION_CB** 回呼。</span><span class="sxs-lookup"><span data-stu-id="e246d-123">If the provider returns an error from **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS will not invoke the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback for that _enumerationId_.</span></span>

1. <span data-ttu-id="e246d-124">ProjFS 會呼叫提供者的 **PRJ_GET_DIRECTORY_ENUMERATION_CB** 回呼一或多次，以從提供者取得目錄內容。</span><span class="sxs-lookup"><span data-stu-id="e246d-124">ProjFS calls the provider's **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback one or more times to get the directory contents from the provider.</span></span>

    <span data-ttu-id="e246d-125">為了回應此回呼，提供者會從其支援資料存放區傳回已排序的專案清單。</span><span class="sxs-lookup"><span data-stu-id="e246d-125">In response to this callback the provider returns a sorted list of items from its backing data store.</span></span>

    <span data-ttu-id="e246d-126">回呼可能會在其 _searchExpression_ 參數中提供搜尋運算式，讓提供者用來界定列舉的結果範圍。</span><span class="sxs-lookup"><span data-stu-id="e246d-126">The callback may provide a search expression in its _searchExpression_ parameter that the provider uses to scope the results of the enumeration.</span></span>  <span data-ttu-id="e246d-127">如果 _searchExpression_ 為 Null，則提供者會傳回所列舉之目錄中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="e246d-127">If _searchExpression_ is NULL, the provider returns all the entries in the directory being enumerated.</span></span>  <span data-ttu-id="e246d-128">如果非 Null，則提供者可以使用 **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** 來判斷運算式中是否有萬用字元。</span><span class="sxs-lookup"><span data-stu-id="e246d-128">If it is non-NULL, the provider can use **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** to determine whether there are wildcards in the expression.</span></span>  <span data-ttu-id="e246d-129">如果有，則提供者會使用 **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** 來判斷目錄中的專案是否符合搜尋運算式。</span><span class="sxs-lookup"><span data-stu-id="e246d-129">If there are, the provider uses **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** to determine whether an entry in the directory matches the search expression.</span></span>

    <span data-ttu-id="e246d-130">提供者應該在此回呼的第一個調用上，捕捉 _searchExpression_ 的值。</span><span class="sxs-lookup"><span data-stu-id="e246d-130">The provider should capture the value of _searchExpression_ on the first invocation of this callback.</span></span>  <span data-ttu-id="e246d-131">除非在回呼的 _callbackData_ 參數的 [**旗標**] 欄位中設定 PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN，否則它會在相同列舉會話中任何後續的回呼調用中使用捕捉到的值。</span><span class="sxs-lookup"><span data-stu-id="e246d-131">It uses the captured value on any subsequent invocation of the callback in the same enumeration session, unless PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN is set in the **Flags** field of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="e246d-132">在這種情況下，應該重新捕獲 _searchExpression_ 的值。</span><span class="sxs-lookup"><span data-stu-id="e246d-132">In that case it should recapture the value of _searchExpression_.</span></span>

    <span data-ttu-id="e246d-133">如果其備份存放區中沒有相符專案，則提供者會直接從回呼傳回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="e246d-133">If there are no matching entries in its backing store, the provider simply returns S_OK from the callback.</span></span>  <span data-ttu-id="e246d-134">否則，提供者會將其備份存放區中的每個相符專案格式化為 **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** 結構，然後使用 **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** 來填滿回呼的 _dirEntryBufferHandle_ 參數所提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e246d-134">Otherwise the provider formats each matching entry from its backing store into a **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** structure, and then uses **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="e246d-135">提供者會持續新增專案，直到其全部加入，或直到 **PrjFillDirEntryBuffer** 傳回 HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) 為止。</span><span class="sxs-lookup"><span data-stu-id="e246d-135">The provider keeps adding entries until it has added them all or until **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).</span></span>  <span data-ttu-id="e246d-136">然後，提供者會從回呼傳回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="e246d-136">Then the provider returns S_OK from the callback.</span></span>  <span data-ttu-id="e246d-137">請注意，提供者必須以正確的排序次序將專案加入至 _dirEntryBufferHandle_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e246d-137">Note that the provider must add the entries to the _dirEntryBufferHandle_ buffer in the correct sort order.</span></span>  <span data-ttu-id="e246d-138">提供者應該使用 **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** 來判斷正確的排序次序。</span><span class="sxs-lookup"><span data-stu-id="e246d-138">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** to determine the correct sort order.</span></span>

    > <span data-ttu-id="e246d-139">提供者必須提供 **PRJ_FILE_BASIC_INFO** 之 **IsDirectory** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="e246d-139">The provider must supply a value for the **IsDirectory** member of **PRJ_FILE_BASIC_INFO**.</span></span>  <span data-ttu-id="e246d-140">如果 **IsDirectory** 為 FALSE，則提供者也必須提供 **FileSize** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="e246d-140">If **IsDirectory** is FALSE, the provider must also supply a value for the **FileSize** member.</span></span>
    >
    > <span data-ttu-id="e246d-141">如果提供者未提供 **CreationTime**、 **LastAccessTime**、 **LastWriteTime** 和 **ChangeTime** 成員的值，ProjFS 將會使用目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="e246d-141">If the provider does not supply values for the **CreationTime**, **LastAccessTime**, **LastWriteTime**, and **ChangeTime** members, ProjFS will use the current system time.</span></span>
    >
    > <span data-ttu-id="e246d-142">ProjFS 會使用任何 FILE_ATTRIBUTE 旗標 **FileAttributes** 成員中的提供者集合，但 FILE_ATTRIBUTE_DIRECTORY 除外;它會根據所提供的 **IsDirectory** 成員值，設定 **FileAttributes** 成員中 FILE_ATTRIBUTE_DIRECTORY 的正確值。</span><span class="sxs-lookup"><span data-stu-id="e246d-142">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileAttributes** member except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileAttributes** member according to the supplied value of the **IsDirectory** member.</span></span>

    <span data-ttu-id="e246d-143">如果 **PrjFillDirEntryBuffer** 在提供者用完要加入的專案之前，傳回 HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) ，則提供者必須在收到錯誤時追蹤嘗試加入的專案。</span><span class="sxs-lookup"><span data-stu-id="e246d-143">If **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) before the provider runs out of entries to add to it, the provider must keep track of the entry it was trying to add when it received the error.</span></span>  <span data-ttu-id="e246d-144">下次 ProjFS 呼叫相同列舉會話的 **PRJ_GET_DIRECTORY_ENUMERATION_CB** 回呼時，提供者必須繼續將專案加入至 _dirEntryBufferHandle_ 緩衝區，並將其新增至其嘗試加入的專案。</span><span class="sxs-lookup"><span data-stu-id="e246d-144">The next time ProjFS calls the **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback for the same enumeration session, the provider must resume adding entries to the _dirEntryBufferHandle_ buffer with the entry it was trying to add.</span></span>

    > <span data-ttu-id="e246d-145">如果支援存放區支援符號連結，則提供者必須使用 **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** 來填滿回呼的 _dirEntryBufferHandle_ 參數所提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e246d-145">If the backing store supports symbolic links, the provider must use **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="e246d-146">**PrjFillDirEntryBuffer2** 支援額外的緩衝區輸入，可讓提供者指定列舉專案是符號連結和其目標。</span><span class="sxs-lookup"><span data-stu-id="e246d-146">**PrjFillDirEntryBuffer2** supports an extra buffer input that allows the provider to specify that the enumeration entry is a symbolic link and what its target is.</span></span>  <span data-ttu-id="e246d-147">否則， **PrjFillDirEntryBuffer** 會如上面所述運作。</span><span class="sxs-lookup"><span data-stu-id="e246d-147">It otherwise behaves as described above for **PrjFillDirEntryBuffer**.</span></span>  <span data-ttu-id="e246d-148">下列範例會使用 **PrjFillDirEntryBuffer2** 來說明符號連結的支援。</span><span class="sxs-lookup"><span data-stu-id="e246d-148">The following sample uses **PrjFillDirEntryBuffer2** to illustrate support for symbolic links.</span></span>
    >
    > <span data-ttu-id="e246d-149">請注意，Windows 10 2004 版才支援 **PrjFillDirEntryBuffer2** 。</span><span class="sxs-lookup"><span data-stu-id="e246d-149">Note that **PrjFillDirEntryBuffer2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="e246d-150">提供者應該探查是否存在 **PrjFillDirEntryBuffer2**，例如使用 **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**。</span><span class="sxs-lookup"><span data-stu-id="e246d-150">A provider should probe for the existence of **PrjFillDirEntryBuffer2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. <span data-ttu-id="e246d-151">ProjFS 會呼叫提供者的 **PRJ_END_DIRECTORY_ENUMERATION_CB** 回呼，以結束列舉會話。</span><span class="sxs-lookup"><span data-stu-id="e246d-151">ProjFS calls the provider's **PRJ_END_DIRECTORY_ENUMERATION_CB** callback to end the enumeration session.</span></span>

    <span data-ttu-id="e246d-152">提供者應該執行任何必須執行的清除作業，以結束列舉會話，例如將配置的記憶體解除配置為處理 **PRJ_START_DIRECTORY_ENUMERATION_CB** 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e246d-152">The provider should perform any cleanup it needs to do to end the enumeration session, such as deallocate memory allocated as part of processing **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span></span>
