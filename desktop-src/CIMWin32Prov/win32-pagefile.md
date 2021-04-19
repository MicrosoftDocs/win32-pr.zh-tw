---
description: Win32 \_ 分頁檔&\# 32;WMI 類別代表用來處理在 Win32 系統上交換虛擬記憶體檔案的檔案。 這個類別已被取代。
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Win32_PageFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb63c4242ae8fa3cca5133a25d2742d07210ca1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979716"
---
# <a name="win32_pagefile-class"></a><span data-ttu-id="3a046-104">Win32 \_ 分頁檔類別</span><span class="sxs-lookup"><span data-stu-id="3a046-104">Win32\_PageFile class</span></span>

<span data-ttu-id="3a046-105">**Win32 \_ 頁面** 檔 [WMI 類別](../wmisdk/retrieving-a-class.md)代表用來處理在 Win32 系統上交換虛擬記憶體檔案的檔案。</span><span class="sxs-lookup"><span data-stu-id="3a046-105">The **Win32\_PageFile** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="3a046-106">這個類別已被取代。</span><span class="sxs-lookup"><span data-stu-id="3a046-106">This class has been deprecated.</span></span>

<span data-ttu-id="3a046-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3a046-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3a046-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="3a046-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a046-109">語法</span><span class="sxs-lookup"><span data-stu-id="3a046-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="3a046-110">成員</span><span class="sxs-lookup"><span data-stu-id="3a046-110">Members</span></span>

<span data-ttu-id="3a046-111">**Win32 \_ 分頁檔** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3a046-111">The **Win32\_PageFile** class has these types of members:</span></span>

-   [<span data-ttu-id="3a046-112">方法</span><span class="sxs-lookup"><span data-stu-id="3a046-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a046-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3a046-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a046-114">方法</span><span class="sxs-lookup"><span data-stu-id="3a046-114">Methods</span></span>

<span data-ttu-id="3a046-115">**Win32 \_ 分頁檔** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3a046-115">The **Win32\_PageFile** class has these methods.</span></span>



| <span data-ttu-id="3a046-116">方法</span><span class="sxs-lookup"><span data-stu-id="3a046-116">Method</span></span>                                                                                            | <span data-ttu-id="3a046-117">描述</span><span class="sxs-lookup"><span data-stu-id="3a046-117">Description</span></span>                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a046-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="3a046-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-pagefile.md)     | <span data-ttu-id="3a046-119">類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="3a046-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3a046-120">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="3a046-120">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | <span data-ttu-id="3a046-121">類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="3a046-121">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3a046-122">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="3a046-122">**Compress**</span></span>](compress-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="3a046-123">類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="3a046-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="3a046-124">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="3a046-124">**CompressEx**</span></span>](compressex-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="3a046-125">類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="3a046-125">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="3a046-126">**複製**</span><span class="sxs-lookup"><span data-stu-id="3a046-126">**Copy**</span></span>](copy-method-in-class-win32-pagefile.md)                                               | <span data-ttu-id="3a046-127">類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="3a046-127">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                       |
| [<span data-ttu-id="3a046-128">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="3a046-128">**CopyEx**</span></span>](copyex-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3a046-129">類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到 FileName 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="3a046-129">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                                    |
| [<span data-ttu-id="3a046-130">**刪除**</span><span class="sxs-lookup"><span data-stu-id="3a046-130">**Delete**</span></span>](delete-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3a046-131">類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="3a046-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3a046-132">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="3a046-132">**DeleteEx**</span></span>](deleteex-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="3a046-133">類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="3a046-133">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3a046-134">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="3a046-134">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-pagefile.md)           | <span data-ttu-id="3a046-135">類別方法，這個方法會判斷呼叫端是否有 *許可權* 引數所指定的匯總許可權，不只是在檔案物件上，而是在共用上的檔案或目錄位於共用) 的 (。</span><span class="sxs-lookup"><span data-stu-id="3a046-135">Class method that determines whether the caller has the aggregated permissions specified by the *Permission* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="3a046-136">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="3a046-136">**Rename**</span></span>](rename-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3a046-137">類別方法，會將物件路徑中指定的邏輯檔案 (或目錄) 重新命名。</span><span class="sxs-lookup"><span data-stu-id="3a046-137">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3a046-138">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="3a046-138">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-pagefile.md)                             | <span data-ttu-id="3a046-139">取得物件路徑中所指定之邏輯檔案擁有權的類別方法。</span><span class="sxs-lookup"><span data-stu-id="3a046-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="3a046-140">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="3a046-140">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-pagefile.md)                         | <span data-ttu-id="3a046-141">取得物件路徑中所指定之邏輯檔案擁有權的類別方法。</span><span class="sxs-lookup"><span data-stu-id="3a046-141">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="3a046-142">**解壓**</span><span class="sxs-lookup"><span data-stu-id="3a046-142">**Uncompress**</span></span>](uncompress-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="3a046-143">Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="3a046-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="3a046-144">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="3a046-144">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-pagefile.md)                               | <span data-ttu-id="3a046-145">Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="3a046-145">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="3a046-146">屬性</span><span class="sxs-lookup"><span data-stu-id="3a046-146">Properties</span></span>

<span data-ttu-id="3a046-147">**Win32 \_ 分頁檔** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3a046-147">The **Win32\_PageFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a046-148">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="3a046-148">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3a046-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-151">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "存取權限" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-151">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-152">位元遮罩，表示存取或執行檔案上特定作業所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="3a046-152">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="3a046-153">如需值，請參閱檔案 [**和目錄存取權限常數**](../wmisdk/file-and-directory-access-rights-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-153">For values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

<span data-ttu-id="3a046-154">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-154">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="3a046-155">**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="3a046-155">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="3a046-156">**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="3a046-156">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="3a046-157">**檔案 \_\_將資料附加)  (檔案或檔案 \_ 新增 \_ 子目錄 (目錄)** (4) </span><span class="sxs-lookup"><span data-stu-id="3a046-157">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="3a046-158">**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="3a046-158">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="3a046-159">**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="3a046-159">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="3a046-160">**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="3a046-160">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="3a046-161">**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="3a046-161">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="3a046-162">**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="3a046-162">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="3a046-163">**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="3a046-163">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="3a046-164">**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="3a046-164">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="3a046-165">**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="3a046-165">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="3a046-166">**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="3a046-166">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="3a046-167">**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="3a046-167">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="3a046-168">**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="3a046-168">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a046-169">**封存**</span><span class="sxs-lookup"><span data-stu-id="3a046-169">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-170">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a046-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-172">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "應該封存" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-172">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-173">若 **為 True**，則表示應該封存檔案。</span><span class="sxs-lookup"><span data-stu-id="3a046-173">If **True**, the file should be archived.</span></span>

<span data-ttu-id="3a046-174">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-174">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-175">**標題**</span><span class="sxs-lookup"><span data-stu-id="3a046-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-178">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-178">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-179">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="3a046-179">A short textual description of the object.</span></span>

<span data-ttu-id="3a046-180">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-181">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="3a046-181">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-182">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a046-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-184">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( 「Win32」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-184">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-185">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="3a046-185">If **True**, the file is compressed.</span></span>

<span data-ttu-id="3a046-186">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-186">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-187">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3a046-187">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-190">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Compression Method" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-190">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-191">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="3a046-191">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="3a046-192">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="3a046-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="3a046-193">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="3a046-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="3a046-194">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="3a046-194">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="3a046-195">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3a046-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-199">限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-199">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-200">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a046-200">Name of the class.</span></span>

<span data-ttu-id="3a046-201">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-202">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="3a046-202">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-203">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3a046-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-205">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "建立日期" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-205">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-206">建立檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3a046-206">Date and time of the file's creation.</span></span>

<span data-ttu-id="3a046-207">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-207">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-208">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3a046-208">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-211">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「電腦系統類別名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-211">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-212">電腦系統的類別。</span><span class="sxs-lookup"><span data-stu-id="3a046-212">Class of the computer system.</span></span>

<span data-ttu-id="3a046-213">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-213">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-214">**CSName**</span><span class="sxs-lookup"><span data-stu-id="3a046-214">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-217">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「電腦系統名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-217">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-218">電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a046-218">Name of the computer system.</span></span>

<span data-ttu-id="3a046-219">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-220">**說明**</span><span class="sxs-lookup"><span data-stu-id="3a046-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-223">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-224">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="3a046-224">A textual description of the object.</span></span>

<span data-ttu-id="3a046-225">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-226">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="3a046-226">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-229">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Drive" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-229">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-230">磁碟機號 (包括在檔案的磁碟機號) 後面的冒號。</span><span class="sxs-lookup"><span data-stu-id="3a046-230">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="3a046-231">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="3a046-232">範例： "c："</span><span class="sxs-lookup"><span data-stu-id="3a046-232">Example: "c:"</span></span>

<span data-ttu-id="3a046-233">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-234">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="3a046-234">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-237">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "八點三個檔案名" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-237">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-238">DOS 相容的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3a046-238">DOS-compatible file name.</span></span>

<span data-ttu-id="3a046-239">範例： "c： \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="3a046-239">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="3a046-240">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-240">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-241">**已加密**</span><span class="sxs-lookup"><span data-stu-id="3a046-241">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-242">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a046-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-244">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Encrypted" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-244">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-245">若 **為 True**，則表示檔案已加密。</span><span class="sxs-lookup"><span data-stu-id="3a046-245">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="3a046-246">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-247">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="3a046-247">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-250">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Encryption Method" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-250">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-251">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="3a046-251">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="3a046-252">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="3a046-252">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="3a046-253">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="3a046-253">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="3a046-254">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="3a046-254">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="3a046-255">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-256">**分機**</span><span class="sxs-lookup"><span data-stu-id="3a046-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-259">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Extension" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-259">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-260">沒有前一個期間的副檔名 (點) 。</span><span class="sxs-lookup"><span data-stu-id="3a046-260">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="3a046-261">範例： "txt"、"mof"、"mdb"</span><span class="sxs-lookup"><span data-stu-id="3a046-261">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="3a046-262">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="3a046-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-266">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Name" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-266">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-267">不含副檔名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3a046-267">File name without the file name extension.</span></span> <span data-ttu-id="3a046-268">範例： "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="3a046-268">Example: "MyDataFile"</span></span>

<span data-ttu-id="3a046-269">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="3a046-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-271">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3a046-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-273">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Size" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-273">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-274">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a046-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="3a046-275">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3a046-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="3a046-276">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-276">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="3a046-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-280">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "檔案類型" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-281">表示 **擴充** 屬性所表示之檔案類型的描述元。</span><span class="sxs-lookup"><span data-stu-id="3a046-281">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="3a046-282">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-283">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="3a046-283">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-284">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3a046-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-286">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Memory Management 結構 \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-286">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwAvailPageFile"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-287">分頁檔案中的可用空間。</span><span class="sxs-lookup"><span data-stu-id="3a046-287">Space available in the paging file.</span></span> <span data-ttu-id="3a046-288">作業系統可以視需要擴大分頁檔，最多可達使用者所加諸的限制。</span><span class="sxs-lookup"><span data-stu-id="3a046-288">The operating system can enlarge the paging file as necessary, up to the limit imposed by the user.</span></span> <span data-ttu-id="3a046-289">這個屬性會顯示目前認可的記憶體大小與目前頁面檔案大小之間的差異;它不會顯示分頁檔案的最大可能大小。</span><span class="sxs-lookup"><span data-stu-id="3a046-289">This property shows the difference between the size of current committed memory and the current size of the paging file; it does not show the largest possible size of the paging file.</span></span>

</dd> <dt>

<span data-ttu-id="3a046-290">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3a046-290">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-291">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-293">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 檔案系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="3a046-293">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-294">檔案系統的類別。</span><span class="sxs-lookup"><span data-stu-id="3a046-294">Class of the file system.</span></span>

<span data-ttu-id="3a046-295">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-295">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-296">**FSName**</span><span class="sxs-lookup"><span data-stu-id="3a046-296">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-299">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) (" File System Name ") </span><span class="sxs-lookup"><span data-stu-id="3a046-299">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-300">檔案系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a046-300">Name of the file system.</span></span>

<span data-ttu-id="3a046-301">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-302">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="3a046-302">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-303">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a046-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-305">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( 「Win32」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「隱藏」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-306">若 **為 True**，則表示檔案已隱藏。</span><span class="sxs-lookup"><span data-stu-id="3a046-306">If **True**, the file is hidden.</span></span>

<span data-ttu-id="3a046-307">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-307">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-308">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="3a046-308">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-309">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3a046-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-311">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-311">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-312">分頁檔案的初始大小。</span><span class="sxs-lookup"><span data-stu-id="3a046-312">Initial size of the page file.</span></span>

</dd> <dt>

<span data-ttu-id="3a046-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3a046-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-314">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3a046-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-316">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="3a046-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-317">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="3a046-317">Indicates when the object was installed.</span></span> <span data-ttu-id="3a046-318">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="3a046-318">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3a046-319">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-320">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="3a046-320">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-321">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3a046-321">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-323">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「目前的檔案開啟計數」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-323">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-324">檔案目前作用中的「檔案開啟」數目。</span><span class="sxs-lookup"><span data-stu-id="3a046-324">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="3a046-325">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3a046-325">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="3a046-326">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-326">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-327">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="3a046-327">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-328">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3a046-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-330">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「上次存取」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-330">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-331">上次存取檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3a046-331">Date and time the file was last accessed.</span></span>

<span data-ttu-id="3a046-332">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-332">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-333">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="3a046-333">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-334">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3a046-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-336">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「上次修改」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-336">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-337">上次修改檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3a046-337">Date and time the file was last modified.</span></span>

<span data-ttu-id="3a046-338">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-339">**製造商**</span><span class="sxs-lookup"><span data-stu-id="3a046-339">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-342">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "製造商" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-342">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-343">版本資源 (的製造商字串（如果有的話) ）。</span><span class="sxs-lookup"><span data-stu-id="3a046-343">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="3a046-344">這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-344">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-345">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="3a046-345">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-346">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3a046-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-348">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Memory Management 結構 \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-348">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-349">使用者所設定之分頁檔的大小上限。</span><span class="sxs-lookup"><span data-stu-id="3a046-349">Maximum size of the page file as set by the user.</span></span> <span data-ttu-id="3a046-350">作業系統將不會允許分頁檔超過此限制。</span><span class="sxs-lookup"><span data-stu-id="3a046-350">The operating system will not allow the page file to exceed this limit.</span></span>

</dd> <dt>

<span data-ttu-id="3a046-351">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3a046-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-354">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)，覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Name" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemPageFileInformation \| PageFileName" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-354">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemPageFileInformation\|PageFileName")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-355">分頁檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a046-355">Name of the page file.</span></span>

<span data-ttu-id="3a046-356">範例： "C： \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="3a046-356">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="3a046-357">**路徑**</span><span class="sxs-lookup"><span data-stu-id="3a046-357">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-360">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Path" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-360">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-361">檔案的路徑，包括開頭和尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="3a046-361">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="3a046-362">範例： " \\ windows \\ system \\ "</span><span class="sxs-lookup"><span data-stu-id="3a046-362">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="3a046-363">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-363">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-364">**讀**</span><span class="sxs-lookup"><span data-stu-id="3a046-364">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-365">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a046-365">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-367">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "可讀取" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-367">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-368">若 **為 True**，則表示可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="3a046-368">If **True**, the file can be read.</span></span>

<span data-ttu-id="3a046-369">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-369">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-370">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3a046-370">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-371">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-373">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-373">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-374">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="3a046-374">String that indicates the current status of the object.</span></span>

<span data-ttu-id="3a046-375">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3a046-376">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="3a046-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3a046-377">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="3a046-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3a046-378">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3a046-379">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a046-380">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3a046-381">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3a046-382">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3a046-383">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3a046-384">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3a046-385">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3a046-386">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3a046-387">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3a046-388">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="3a046-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a046-389">**系統**</span><span class="sxs-lookup"><span data-stu-id="3a046-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-390">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a046-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-392">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "System File" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-392">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-393">若 **為 True**，表示檔案為系統檔案。</span><span class="sxs-lookup"><span data-stu-id="3a046-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="3a046-394">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-395">**版本**</span><span class="sxs-lookup"><span data-stu-id="3a046-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-396">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a046-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-398">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Version" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-398">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-399">版本資源 (的版本字串（如果有的話）) 。</span><span class="sxs-lookup"><span data-stu-id="3a046-399">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="3a046-400">這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a046-401">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="3a046-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a046-402">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a046-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a046-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a046-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a046-404">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "可寫入" ) </span><span class="sxs-lookup"><span data-stu-id="3a046-404">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="3a046-405">若 **為 True**，則表示可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="3a046-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="3a046-406">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a046-407">備註</span><span class="sxs-lookup"><span data-stu-id="3a046-407">Remarks</span></span>

<span data-ttu-id="3a046-408">**Win32 \_ 分頁檔** 類別衍生自 [**CIM \_ 目錄**](cim-directory.md)。</span><span class="sxs-lookup"><span data-stu-id="3a046-408">The **Win32\_PageFile** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3a046-409">範例</span><span class="sxs-lookup"><span data-stu-id="3a046-409">Examples</span></span>

<span data-ttu-id="3a046-410">下列 VBScript 程式碼範例示範如何從 **Win32 \_ 頁面** 檔的實例中取出分頁檔統計資料。</span><span class="sxs-lookup"><span data-stu-id="3a046-410">The following VBScript code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



<span data-ttu-id="3a046-411">下列 Perl 程式碼範例示範如何從 **Win32 \_ 頁面** 檔的實例中取出分頁檔統計資料。</span><span class="sxs-lookup"><span data-stu-id="3a046-411">The following Perl code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="3a046-412">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a046-412">Requirements</span></span>



| <span data-ttu-id="3a046-413">需求</span><span class="sxs-lookup"><span data-stu-id="3a046-413">Requirement</span></span> | <span data-ttu-id="3a046-414">值</span><span class="sxs-lookup"><span data-stu-id="3a046-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a046-415">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a046-415">Minimum supported client</span></span><br/> | <span data-ttu-id="3a046-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a046-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a046-417">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a046-417">Minimum supported server</span></span><br/> | <span data-ttu-id="3a046-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a046-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a046-419">命名空間</span><span class="sxs-lookup"><span data-stu-id="3a046-419">Namespace</span></span><br/>                | <span data-ttu-id="3a046-420">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3a046-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a046-421">MOF</span><span class="sxs-lookup"><span data-stu-id="3a046-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a046-422"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a046-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a046-423">DLL</span><span class="sxs-lookup"><span data-stu-id="3a046-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a046-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a046-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a046-425">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a046-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a046-426">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="3a046-426">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="3a046-427">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="3a046-427">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
