---
description: Win32 \_ ShortcutFile&\# 32;WMI 類別代表的檔案是其他檔案、目錄和命令的快捷方式。
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile
- Win32_ShortcutFile.Caption
- Win32_ShortcutFile.Description
- Win32_ShortcutFile.InstallDate
- Win32_ShortcutFile.Status
- Win32_ShortcutFile.AccessMask
- Win32_ShortcutFile.Archive
- Win32_ShortcutFile.Compressed
- Win32_ShortcutFile.CompressionMethod
- Win32_ShortcutFile.CreationClassName
- Win32_ShortcutFile.CreationDate
- Win32_ShortcutFile.CSCreationClassName
- Win32_ShortcutFile.CSName
- Win32_ShortcutFile.Drive
- Win32_ShortcutFile.EightDotThreeFileName
- Win32_ShortcutFile.Encrypted
- Win32_ShortcutFile.EncryptionMethod
- Win32_ShortcutFile.Name
- Win32_ShortcutFile.Extension
- Win32_ShortcutFile.FileName
- Win32_ShortcutFile.FileSize
- Win32_ShortcutFile.FileType
- Win32_ShortcutFile.FSCreationClassName
- Win32_ShortcutFile.FSName
- Win32_ShortcutFile.Hidden
- Win32_ShortcutFile.InUseCount
- Win32_ShortcutFile.LastAccessed
- Win32_ShortcutFile.LastModified
- Win32_ShortcutFile.Path
- Win32_ShortcutFile.Readable
- Win32_ShortcutFile.System
- Win32_ShortcutFile.Writeable
- Win32_ShortcutFile.Manufacturer
- Win32_ShortcutFile.Version
- Win32_ShortcutFile.Target
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b714b4c8119f92931235734664726123744064d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973984"
---
# <a name="win32_shortcutfile-class"></a><span data-ttu-id="ef1c7-103">Win32 \_ ShortcutFile 類別</span><span class="sxs-lookup"><span data-stu-id="ef1c7-103">Win32\_ShortcutFile class</span></span>

<span data-ttu-id="ef1c7-104">**Win32 \_ ShortcutFile** [WMI 類別](../wmisdk/retrieving-a-class.md)代表的檔案是其他檔案、目錄和命令的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-104">The **Win32\_ShortcutFile** [WMI class](../wmisdk/retrieving-a-class.md) represents files that are shortcuts to other files, directories, and commands.</span></span>

<span data-ttu-id="ef1c7-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ef1c7-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1c7-107">語法</span><span class="sxs-lookup"><span data-stu-id="ef1c7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE466-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_ShortcutFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
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
  string   Name;
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
  string   Manufacturer;
  string   Version;
  string   Target;
};
```

## <a name="members"></a><span data-ttu-id="ef1c7-108">成員</span><span class="sxs-lookup"><span data-stu-id="ef1c7-108">Members</span></span>

<span data-ttu-id="ef1c7-109">**Win32 \_ ShortcutFile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ef1c7-109">The **Win32\_ShortcutFile** class has these types of members:</span></span>

-   [<span data-ttu-id="ef1c7-110">方法</span><span class="sxs-lookup"><span data-stu-id="ef1c7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ef1c7-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ef1c7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ef1c7-112">方法</span><span class="sxs-lookup"><span data-stu-id="ef1c7-112">Methods</span></span>

<span data-ttu-id="ef1c7-113">**Win32 \_ ShortcutFile** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-113">The **Win32\_ShortcutFile** class has these methods.</span></span>



| <span data-ttu-id="ef1c7-114">方法</span><span class="sxs-lookup"><span data-stu-id="ef1c7-114">Method</span></span>                                                                                                | <span data-ttu-id="ef1c7-115">描述</span><span class="sxs-lookup"><span data-stu-id="ef1c7-115">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef1c7-116">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-116">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | <span data-ttu-id="ef1c7-117">類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-117">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="ef1c7-118">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-118">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | <span data-ttu-id="ef1c7-119">類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="ef1c7-120">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-120">**Compress**</span></span>](compress-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="ef1c7-121">類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-121">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="ef1c7-122">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-122">**CompressEx**</span></span>](compressex-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="ef1c7-123">類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="ef1c7-124">**複製**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-124">**Copy**</span></span>](copy-method-in-class-win32-shortcutfile.md)                                               | <span data-ttu-id="ef1c7-125">類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-125">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="ef1c7-126">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-126">**CopyEx**</span></span>](copyex-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="ef1c7-127">類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到 *FileName* 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-127">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                |
| [<span data-ttu-id="ef1c7-128">**刪除**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-128">**Delete**</span></span>](delete-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="ef1c7-129">類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-129">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="ef1c7-130">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-130">**DeleteEx**</span></span>](deleteex-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="ef1c7-131">類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="ef1c7-132">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-132">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | <span data-ttu-id="ef1c7-133">類別方法，這個方法會判斷呼叫端是否有許可權引數所指定的匯總許可權，不只是在檔案物件上，而是在共用上的檔案或目錄位於共用) 的 (。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-133">Class method that determines whether the caller has the aggregated permissions specified by the Permission argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="ef1c7-134">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-134">**Rename**</span></span>](rename-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="ef1c7-135">類別方法，會將物件路徑中指定的邏輯檔案 (或目錄) 重新命名。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-135">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="ef1c7-136">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-136">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-shortcutfile.md)                             | <span data-ttu-id="ef1c7-137">取得物件路徑中所指定之邏輯檔案擁有權的類別方法。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-137">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="ef1c7-138">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-138">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-shortcutfile.md)                         | <span data-ttu-id="ef1c7-139">取得物件路徑中所指定之邏輯檔案擁有權的類別方法。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="ef1c7-140">**解壓**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-140">**Uncompress**</span></span>](uncompress-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="ef1c7-141">Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-141">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="ef1c7-142">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-142">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-shortcutfile.md)                               | <span data-ttu-id="ef1c7-143">Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="ef1c7-144">屬性</span><span class="sxs-lookup"><span data-stu-id="ef1c7-144">Properties</span></span>

<span data-ttu-id="ef1c7-145">**Win32 \_ ShortcutFile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-145">The **Win32\_ShortcutFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef1c7-146">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-146">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-149">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "存取權限" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-149">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-150">位元遮罩，表示存取或執行檔案上特定作業所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-150">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="ef1c7-151">如需位值，請參閱檔案 [**和目錄存取權限常數**](../wmisdk/file-and-directory-access-rights-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-151">For bit values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="ef1c7-152">在 FAT 磁片區上，會改為傳回 **完整 \_ 存取** 值，表示物件上未設定任何安全性。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-152">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="ef1c7-153">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-153">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ef1c7-154">**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-154">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="ef1c7-155">**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-155">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ef1c7-156">**檔案 \_\_將資料附加)  (檔案或檔案 \_ 新增 \_ 子目錄 (目錄)** (4) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-156">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="ef1c7-157">**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-157">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="ef1c7-158">**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-158">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="ef1c7-159">**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-159">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="ef1c7-160">**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-160">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="ef1c7-161">**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-161">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="ef1c7-162">**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-162">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="ef1c7-163">**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-163">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="ef1c7-164">**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-164">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="ef1c7-165">**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-165">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="ef1c7-166">**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-166">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="ef1c7-167">**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-167">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef1c7-168">**封存**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-168">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-169">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-171">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "應該封存" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-171">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-172">若 **為 True**，則表示應該封存檔案。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-172">If **True**, the file should be archived.</span></span>

<span data-ttu-id="ef1c7-173">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-173">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-174">**標題**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-177">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-177">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-178">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-178">A short textual description of the object.</span></span>

<span data-ttu-id="ef1c7-179">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-180">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-180">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-181">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-183">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( 「Win32」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-183">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-184">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-184">If **True**, the file is compressed.</span></span>

<span data-ttu-id="ef1c7-185">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-185">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-186">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-186">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-189">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Compression Method" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-190">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-190">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="ef1c7-191">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-191">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="ef1c7-192">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-192">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="ef1c7-193">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-193">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="ef1c7-194">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-194">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-198">限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-198">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-199">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-199">Name of the class.</span></span>

<span data-ttu-id="ef1c7-200">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-200">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-201">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-201">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-202">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-202">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-204">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "建立日期" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-204">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-205">建立檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-205">Date and time of the file's creation.</span></span>

<span data-ttu-id="ef1c7-206">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-206">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-207">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-207">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-210">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「電腦系統類別名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-210">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-211">電腦系統的類別。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-211">Class of the computer system.</span></span>

<span data-ttu-id="ef1c7-212">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-213">**CSName**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-213">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-216">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「電腦系統名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-216">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-217">電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-217">Name of the computer system.</span></span>

<span data-ttu-id="ef1c7-218">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-219">**說明**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-222">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-222">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-223">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-223">A textual description of the object.</span></span>

<span data-ttu-id="ef1c7-224">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-225">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-225">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-226">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-228">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Drive" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-228">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-229">磁碟機號 (包括在檔案的磁碟機號) 後面的冒號。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-229">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="ef1c7-230">範例： "c："</span><span class="sxs-lookup"><span data-stu-id="ef1c7-230">Example: "c:"</span></span>

<span data-ttu-id="ef1c7-231">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-232">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-232">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-235">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "八點三個檔案名" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-235">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-236">8.3 格式的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-236">File name in 8.3 format.</span></span>

<span data-ttu-id="ef1c7-237">範例： "c： \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="ef1c7-237">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="ef1c7-238">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-238">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-239">**已加密**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-239">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-240">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-242">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Encrypted" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-242">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-243">若 **為 True**，則表示檔案已加密。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-243">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="ef1c7-244">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-244">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-245">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-245">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-248">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Encryption Method" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-249">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-249">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="ef1c7-250">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-250">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="ef1c7-251">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-251">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="ef1c7-252">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-252">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="ef1c7-253">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-254">**分機**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-254">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-257">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Extension" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-257">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-258">沒有前一個期間的副檔名 (點) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-258">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="ef1c7-259">範例： "txt"、"mof"、"mdb"</span><span class="sxs-lookup"><span data-stu-id="ef1c7-259">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="ef1c7-260">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-261">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-261">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-262">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-264">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Name" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-264">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-265">不含副檔名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-265">File name without the file name extension.</span></span>

<span data-ttu-id="ef1c7-266">範例： "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="ef1c7-266">Example: "MyDataFile"</span></span>

<span data-ttu-id="ef1c7-267">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-267">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-268">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-268">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-269">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-271">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Size" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-271">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-272">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-272">Size of the file, in bytes.</span></span>

<span data-ttu-id="ef1c7-273">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-273">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="ef1c7-274">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-274">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-275">**FileType**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-275">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-278">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "檔案類型" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-278">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-279">表示 **擴充** 屬性所表示之檔案類型的描述元。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-279">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="ef1c7-280">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-280">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-284">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 檔案系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="ef1c7-284">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-285">檔案系統的類別。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-285">Class of the file system.</span></span>

<span data-ttu-id="ef1c7-286">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-287">**FSName**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-287">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-290">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) (" File System Name ") </span><span class="sxs-lookup"><span data-stu-id="ef1c7-290">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-291">檔案系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-291">Name of the file system.</span></span>

<span data-ttu-id="ef1c7-292">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-293">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-293">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-294">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-296">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( 「Win32」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「隱藏」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-297">若 **為 True**，則表示檔案已隱藏。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-297">If **True**, the file is hidden.</span></span>

<span data-ttu-id="ef1c7-298">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-299">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-299">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-300">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-300">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-302">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="ef1c7-302">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-303">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-303">Indicates when the object was installed.</span></span> <span data-ttu-id="ef1c7-304">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-304">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ef1c7-305">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-306">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-306">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-307">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-309">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「目前的檔案開啟計數」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-310">檔案目前作用中的「檔案開啟」數目。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-310">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="ef1c7-311">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-311">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="ef1c7-312">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-312">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-313">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-313">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-314">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-316">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「上次存取」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-316">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-317">上次存取檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-317">Date and time the file was last accessed.</span></span>

<span data-ttu-id="ef1c7-318">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-318">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-319">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-319">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-320">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-322">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「上次修改」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-322">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-323">上次修改檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-323">Date and time the file was last modified.</span></span>

<span data-ttu-id="ef1c7-324">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-324">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-325">**製造商**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-326">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-328">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "製造商" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-329">版本資源 (的製造商字串（如果有的話) ）。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-329">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="ef1c7-330">這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-330">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-331">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-332">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-334">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="ef1c7-334">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-335">Name 屬性是一個字串，代表繼承的名稱，做為檔案系統內的邏輯檔案實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-335">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="ef1c7-336">應提供完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-336">Full path names should be provided.</span></span>

<span data-ttu-id="ef1c7-337">範例： C： \\ Windows \\ system \\win.ini</span><span class="sxs-lookup"><span data-stu-id="ef1c7-337">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="ef1c7-338">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-339">**路徑**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-339">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-342">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Path" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-342">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-343">檔案的路徑，包括開頭和尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-343">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="ef1c7-344">範例： " \\ windows \\ system \\ "</span><span class="sxs-lookup"><span data-stu-id="ef1c7-344">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="ef1c7-345">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-345">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-346">**讀**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-346">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-347">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-347">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-349">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "可讀取" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-349">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-350">若 **為 True**，則表示可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-350">If **True**, the file can be read.</span></span>

<span data-ttu-id="ef1c7-351">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-352">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-355">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-355">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-356">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-356">String that indicates the current status of the object.</span></span> <span data-ttu-id="ef1c7-357">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-357">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ef1c7-358">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-358">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ef1c7-359">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-359">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ef1c7-360">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-360">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ef1c7-361">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-361">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ef1c7-362">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-362">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ef1c7-363">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-363">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ef1c7-364">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="ef1c7-364">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ef1c7-365">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-365">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ef1c7-366">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-366">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ef1c7-367">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-367">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef1c7-368">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-368">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ef1c7-369">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-369">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ef1c7-370">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-370">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ef1c7-371">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-371">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ef1c7-372">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-372">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ef1c7-373">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-373">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ef1c7-374">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-374">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ef1c7-375">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-375">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ef1c7-376">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-376">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef1c7-377">**系統**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-377">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-378">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-379">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-380">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "System File" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-380">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-381">若 **為 True**，表示檔案為系統檔案。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-381">If **True**, the file is a system file.</span></span>

<span data-ttu-id="ef1c7-382">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-383">**Target**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-383">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-384">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-386">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| \_ beginthreadex" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-386">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|\_beginthreadex")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-387">這是快捷方式的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-387">Name of the object that this is a shortcut to.</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-388">**版本**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-388">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-389">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-391">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Version" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-391">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-392">版本資源 (的版本字串（如果有的話）) 。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-392">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="ef1c7-393">這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-393">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef1c7-394">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-394">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef1c7-395">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef1c7-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef1c7-397">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "可寫入" ) </span><span class="sxs-lookup"><span data-stu-id="ef1c7-397">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="ef1c7-398">若 **為 True**，則表示可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-398">If **True**, the file can be written.</span></span>

<span data-ttu-id="ef1c7-399">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef1c7-400">備註</span><span class="sxs-lookup"><span data-stu-id="ef1c7-400">Remarks</span></span>

<span data-ttu-id="ef1c7-401">**Win32 \_ ShortcutFile** 類別衍生自 [**CIM \_ 資料檔案**](cim-datafile.md)。</span><span class="sxs-lookup"><span data-stu-id="ef1c7-401">The **Win32\_ShortcutFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1c7-402">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef1c7-402">Requirements</span></span>



| <span data-ttu-id="ef1c7-403">需求</span><span class="sxs-lookup"><span data-stu-id="ef1c7-403">Requirement</span></span> | <span data-ttu-id="ef1c7-404">值</span><span class="sxs-lookup"><span data-stu-id="ef1c7-404">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1c7-405">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef1c7-405">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1c7-406">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef1c7-406">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef1c7-407">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef1c7-407">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1c7-408">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef1c7-408">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef1c7-409">命名空間</span><span class="sxs-lookup"><span data-stu-id="ef1c7-409">Namespace</span></span><br/>                | <span data-ttu-id="ef1c7-410">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ef1c7-410">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef1c7-411">MOF</span><span class="sxs-lookup"><span data-stu-id="ef1c7-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef1c7-412"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef1c7-412"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef1c7-413">DLL</span><span class="sxs-lookup"><span data-stu-id="ef1c7-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1c7-414"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1c7-414"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1c7-415">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef1c7-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1c7-416">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="ef1c7-416">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ef1c7-417">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="ef1c7-417">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
