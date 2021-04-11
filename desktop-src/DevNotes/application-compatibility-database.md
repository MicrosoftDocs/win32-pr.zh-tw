---
description: 相容性基礎結構會使用資料庫來識別應用程式相容性問題及其解決方案。
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: 應用程式相容性資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688660"
---
# <a name="application-compatibility-database"></a><span data-ttu-id="6f155-103">應用程式相容性資料庫</span><span class="sxs-lookup"><span data-stu-id="6f155-103">Application Compatibility Database</span></span>

<span data-ttu-id="6f155-104">相容性基礎結構會使用資料庫來識別應用程式相容性問題及其解決方案。</span><span class="sxs-lookup"><span data-stu-id="6f155-104">The compatibility infrastructure uses a database to identify application compatibility issues and their solutions.</span></span> <span data-ttu-id="6f155-105">此資料庫是具有 sdb 副檔名的索引二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="6f155-105">This database is an indexed binary file with an .sdb extension.</span></span> <span data-ttu-id="6f155-106">相容性基礎結構提供用來存取資料庫的程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="6f155-106">The compatibility infrastructure provides a programming interface to access the database.</span></span>

<span data-ttu-id="6f155-107">您可以在執行時間依應用程式來解決相容性問題。</span><span class="sxs-lookup"><span data-stu-id="6f155-107">Compatibility issues can be addressed on an application-by-application basis at run time.</span></span> <span data-ttu-id="6f155-108">資料庫中指定的每個應用程式都包含一或多個需要解決方案的元件。</span><span class="sxs-lookup"><span data-stu-id="6f155-108">Each application specified in the database contains one or more components that need a solution.</span></span> <span data-ttu-id="6f155-109">元件是一般使用其檔案屬性描述的可執行檔 (例如，總和檢查碼) 。</span><span class="sxs-lookup"><span data-stu-id="6f155-109">Components are executable files that are generally described using their file attributes (for example, checksum).</span></span>

<span data-ttu-id="6f155-110">資料庫查閱和決定每個應用程式之解決方案的程式，都稱為 *符合*。</span><span class="sxs-lookup"><span data-stu-id="6f155-110">The process of database lookup and determining the solutions for each application is called *matching*.</span></span> <span data-ttu-id="6f155-111">檔案屬性以及包含 .exe 檔案的資料夾或子資料夾中有相關聯的檔案，可以用來建立唯一的相符項。</span><span class="sxs-lookup"><span data-stu-id="6f155-111">The file attributes and the presence of associated files in the folder or subfolder containing the .exe file can be used to create a unique match.</span></span> <span data-ttu-id="6f155-112">相關聯的檔案稱為 *相符* 的檔案。</span><span class="sxs-lookup"><span data-stu-id="6f155-112">The associated files are called *matching files*.</span></span>

<span data-ttu-id="6f155-113">*標記* 是資料庫中專案和屬性的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f155-113">A *TAG* is a unique identifier for the entries and attributes in the database.</span></span> <span data-ttu-id="6f155-114">*標記類型* 表示與 [**標記**](tag.md)相關聯的資料格式。</span><span class="sxs-lookup"><span data-stu-id="6f155-114">The *TAG type* indicates the format of the data associated with the [**TAG**](tag.md).</span></span> <span data-ttu-id="6f155-115">例如， **標記 \_ 名稱** 的類型為 **tag \_ 類型 \_ STRINGREF**; 標籤 **\_ 名稱** 的資料是名稱字串。</span><span class="sxs-lookup"><span data-stu-id="6f155-115">For example, **TAG\_NAME** is of type **TAG\_TYPE\_STRINGREF**; the data for **TAG\_NAME** is a name string.</span></span> <span data-ttu-id="6f155-116">*TAGID* 是特定資料庫中專案的指標。</span><span class="sxs-lookup"><span data-stu-id="6f155-116">A *TAGID* is a pointer to an entry in a particular database.</span></span> <span data-ttu-id="6f155-117">*TAGREF* 是可跨多個資料庫使用之專案的指標。</span><span class="sxs-lookup"><span data-stu-id="6f155-117">A *TAGREF* is a pointer to an entry that can be used across multiple databases.</span></span>

<span data-ttu-id="6f155-118">*檔案屬性* 是與磁片上的檔案相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6f155-118">*File attributes* are metadata associated with a file on disk.</span></span> <span data-ttu-id="6f155-119">這些屬性包括檔案名、檔案大小、總和檢查碼、版本和日期。</span><span class="sxs-lookup"><span data-stu-id="6f155-119">These attributes include the file name, file size, checksum, version, and date.</span></span> <span data-ttu-id="6f155-120">這些屬性是用來判斷系統載入的檔案是否符合資料庫專案。</span><span class="sxs-lookup"><span data-stu-id="6f155-120">These attributes are used to determine whether a file being loaded by the system matches a database entry.</span></span> <span data-ttu-id="6f155-121">因此，這些檔案屬性也稱為 *相符的屬性*。</span><span class="sxs-lookup"><span data-stu-id="6f155-121">Therefore, these file attributes are also called *matching attributes*.</span></span>

## <a name="solutions"></a><span data-ttu-id="6f155-122">方案</span><span class="sxs-lookup"><span data-stu-id="6f155-122">Solutions</span></span>

<span data-ttu-id="6f155-123">套用至應用程式元件的最常見方案是 Apphelp 和 Appfix。</span><span class="sxs-lookup"><span data-stu-id="6f155-123">The most common solutions applied to the components of an application are Apphelp and Appfix.</span></span>

<span data-ttu-id="6f155-124">使用 Apphelp 時，會顯示自訂當地語系化訊息通知，通常是在安裝或啟動應用程式時。</span><span class="sxs-lookup"><span data-stu-id="6f155-124">With Apphelp, a custom localized message notification is displayed, typically when the application is installed or started.</span></span> <span data-ttu-id="6f155-125">其中包含簡短的文字，說明相容性問題，並提供可讓您繼續執行應用程式的選項。</span><span class="sxs-lookup"><span data-stu-id="6f155-125">It contains brief text that explains the compatibility issue and provides the option to continue running the application.</span></span> <span data-ttu-id="6f155-126">不過，有些應用程式會大幅失敗，而無法執行;Apphelp 不會提供使用者繼續執行這些應用程式的選項。</span><span class="sxs-lookup"><span data-stu-id="6f155-126">However, some applications will fail dramatically is allowed to run; Apphelp will not give the user the option to continue running these applications.</span></span>

<span data-ttu-id="6f155-127">使用 Appfix 時，會為應用程式的元件所呼叫的 Api 安裝勾點。</span><span class="sxs-lookup"><span data-stu-id="6f155-127">With Appfix, hooks are installed for APIs called by the components of the application.</span></span> <span data-ttu-id="6f155-128">這些勾點指向可以呼叫的存根函式，而不是系統函數 (也稱為 *填充碼銜接*) 。</span><span class="sxs-lookup"><span data-stu-id="6f155-128">These hooks point to stub functions that can be called instead of the system functions (also known as *shimming*).</span></span> <span data-ttu-id="6f155-129">存根函式會執行必要的作業，讓應用程式可以在已安裝的 Windows 版本上執行。</span><span class="sxs-lookup"><span data-stu-id="6f155-129">The stub functions perform operations needed to enable the application to run on the installed version of Windows.</span></span> <span data-ttu-id="6f155-130">每個存根函式在完成其工作之後，可以選擇性地呼叫系統函數。</span><span class="sxs-lookup"><span data-stu-id="6f155-130">Each stub function may optionally call the system function after completing its work.</span></span> <span data-ttu-id="6f155-131">*相容性層* 或 *模式* 包含一或多個填充碼和旗標。</span><span class="sxs-lookup"><span data-stu-id="6f155-131">A *compatibility layer* or *mode* contains one or more shims and flags.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6f155-132">本節內容</span><span class="sxs-lookup"><span data-stu-id="6f155-132">In this section</span></span>

-   [<span data-ttu-id="6f155-133">**APPHELP \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6f155-133">**APPHELP\_DATA**</span></span>](apphelp-data.md)
-   [<span data-ttu-id="6f155-134">**ATTRINFO**</span><span class="sxs-lookup"><span data-stu-id="6f155-134">**ATTRINFO**</span></span>](attrinfo.md)
-   [<span data-ttu-id="6f155-135">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="6f155-135">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
-   [<span data-ttu-id="6f155-136">**尋找 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6f155-136">**FIND\_INFO**</span></span>](find-info.md)
-   [<span data-ttu-id="6f155-137">**INDEXID**</span><span class="sxs-lookup"><span data-stu-id="6f155-137">**INDEXID**</span></span>](indexid.md)
-   [<span data-ttu-id="6f155-138">**路徑 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6f155-138">**PATH\_TYPE**</span></span>](path-type.md)
-   [<span data-ttu-id="6f155-139">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-139">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
-   [<span data-ttu-id="6f155-140">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="6f155-140">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
-   [<span data-ttu-id="6f155-141">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="6f155-141">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
-   [<span data-ttu-id="6f155-142">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="6f155-142">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
-   [<span data-ttu-id="6f155-143">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="6f155-143">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
-   [<span data-ttu-id="6f155-144">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="6f155-144">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
-   [<span data-ttu-id="6f155-145">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-145">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
-   [<span data-ttu-id="6f155-146">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-146">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
-   [<span data-ttu-id="6f155-147">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-147">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
-   [<span data-ttu-id="6f155-148">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-148">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
-   [<span data-ttu-id="6f155-149">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="6f155-149">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
-   [<span data-ttu-id="6f155-150">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="6f155-150">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
-   [<span data-ttu-id="6f155-151">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="6f155-151">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
-   [<span data-ttu-id="6f155-152">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="6f155-152">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
-   [<span data-ttu-id="6f155-153">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="6f155-153">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
-   [<span data-ttu-id="6f155-154">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="6f155-154">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
-   [<span data-ttu-id="6f155-155">**SdbGetIndex**</span><span class="sxs-lookup"><span data-stu-id="6f155-155">**SdbGetIndex**</span></span>](sdbgetindex.md)
-   [<span data-ttu-id="6f155-156">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="6f155-156">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
-   [<span data-ttu-id="6f155-157">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="6f155-157">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
-   [<span data-ttu-id="6f155-158">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="6f155-158">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
-   [<span data-ttu-id="6f155-159">**SdbGetTagFromTagID**</span><span class="sxs-lookup"><span data-stu-id="6f155-159">**SdbGetTagFromTagID**</span></span>](sdbgettagfromtagid.md)
-   [<span data-ttu-id="6f155-160">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="6f155-160">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
-   [<span data-ttu-id="6f155-161">**SdbIsStandardDatabase**</span><span class="sxs-lookup"><span data-stu-id="6f155-161">**SdbIsStandardDatabase**</span></span>](sdbisstandarddatabase.md)
-   [<span data-ttu-id="6f155-162">**SdbMakeIndexKeyFromString**</span><span class="sxs-lookup"><span data-stu-id="6f155-162">**SdbMakeIndexKeyFromString**</span></span>](sdbmakeindexkeyfromstring.md)
-   [<span data-ttu-id="6f155-163">**SdbOpenApphelpDetailsDatabase**</span><span class="sxs-lookup"><span data-stu-id="6f155-163">**SdbOpenApphelpDetailsDatabase**</span></span>](sdbopenapphelpdetailsdatabase.md)
-   [<span data-ttu-id="6f155-164">**SdbOpenApphelpResourceFile**</span><span class="sxs-lookup"><span data-stu-id="6f155-164">**SdbOpenApphelpResourceFile**</span></span>](sdbopenapphelpresourcefile.md)
-   [<span data-ttu-id="6f155-165">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="6f155-165">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
-   [<span data-ttu-id="6f155-166">**SdbQueryDataExTagID**</span><span class="sxs-lookup"><span data-stu-id="6f155-166">**SdbQueryDataExTagID**</span></span>](sdbquerydataextagid.md)
-   [<span data-ttu-id="6f155-167">**SDBQUERYRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f155-167">**SDBQUERYRESULT**</span></span>](sdbqueryresult.md)
-   [<span data-ttu-id="6f155-168">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="6f155-168">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
-   [<span data-ttu-id="6f155-169">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-169">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
-   [<span data-ttu-id="6f155-170">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-170">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
-   [<span data-ttu-id="6f155-171">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-171">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
-   [<span data-ttu-id="6f155-172">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-172">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
-   [<span data-ttu-id="6f155-173">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="6f155-173">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
-   [<span data-ttu-id="6f155-174">**SdbReleaseDatabase**</span><span class="sxs-lookup"><span data-stu-id="6f155-174">**SdbReleaseDatabase**</span></span>](sdbreleasedatabase.md)
-   [<span data-ttu-id="6f155-175">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="6f155-175">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
-   [<span data-ttu-id="6f155-176">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="6f155-176">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
-   [<span data-ttu-id="6f155-177">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="6f155-177">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
-   [<span data-ttu-id="6f155-178">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="6f155-178">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
-   [<span data-ttu-id="6f155-179">**SdbTagToString**</span><span class="sxs-lookup"><span data-stu-id="6f155-179">**SdbTagToString**</span></span>](sdbtagtostring.md)
-   [<span data-ttu-id="6f155-180">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="6f155-180">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
-   [<span data-ttu-id="6f155-181">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-181">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
-   [<span data-ttu-id="6f155-182">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="6f155-182">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
-   [<span data-ttu-id="6f155-183">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-183">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
-   [<span data-ttu-id="6f155-184">**SdbWriteNullTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-184">**SdbWriteNULLTag**</span></span>](sdbwritenulltag.md)
-   [<span data-ttu-id="6f155-185">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-185">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
-   [<span data-ttu-id="6f155-186">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-186">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
-   [<span data-ttu-id="6f155-187">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="6f155-187">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
-   [<span data-ttu-id="6f155-188">**填充碼資料庫類型**</span><span class="sxs-lookup"><span data-stu-id="6f155-188">**Shim Database Types**</span></span>](shim-database-types.md)
-   [<span data-ttu-id="6f155-189">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="6f155-189">**ShimFlushCache**</span></span>](shimflushcache.md)
-   [<span data-ttu-id="6f155-190">**標記**</span><span class="sxs-lookup"><span data-stu-id="6f155-190">**TAG**</span></span>](tag.md)
-   [<span data-ttu-id="6f155-191">**標記類型**</span><span class="sxs-lookup"><span data-stu-id="6f155-191">**TAG Types**</span></span>](tag-types.md)
-   [<span data-ttu-id="6f155-192">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="6f155-192">**TAGID**</span></span>](tagid.md)
-   [<span data-ttu-id="6f155-193">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="6f155-193">**TAGREF**</span></span>](tagref.md)

 

 



