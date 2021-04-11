---
description: Win32 \_ 目錄&\# 32;WMI 類別代表執行 Windows 的電腦系統上的目錄專案。
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Win32_Directory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190990"
---
# <a name="win32_directory-class"></a><span data-ttu-id="9e7fe-103">Win32 \_ 目錄類別</span><span class="sxs-lookup"><span data-stu-id="9e7fe-103">Win32\_Directory class</span></span>

<span data-ttu-id="9e7fe-104">**Win32 \_ 目錄** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 的電腦系統上的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-104">The **Win32\_Directory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a directory entry on a computer system running Windows.</span></span> <span data-ttu-id="9e7fe-105">目錄是一種以邏輯方式將資料檔案分組，並提供群組檔案之路徑資訊的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-105">A directory is a type of file that logically groups data files and provides path information for the grouped files.</span></span> <span data-ttu-id="9e7fe-106">範例： C： \\ TEMP。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-106">Example: C:\\TEMP.</span></span> <span data-ttu-id="9e7fe-107">**Win32 \_目錄** 不包含網路磁碟機機的目錄。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-107">**Win32\_Directory** does not include directories of network drives.</span></span>

<span data-ttu-id="9e7fe-108">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9e7fe-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7fe-110">語法</span><span class="sxs-lookup"><span data-stu-id="9e7fe-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
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
};
```

## <a name="members"></a><span data-ttu-id="9e7fe-111">成員</span><span class="sxs-lookup"><span data-stu-id="9e7fe-111">Members</span></span>

<span data-ttu-id="9e7fe-112">**Win32 \_ 目錄** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9e7fe-112">The **Win32\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="9e7fe-113">方法</span><span class="sxs-lookup"><span data-stu-id="9e7fe-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="9e7fe-114">屬性</span><span class="sxs-lookup"><span data-stu-id="9e7fe-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9e7fe-115">方法</span><span class="sxs-lookup"><span data-stu-id="9e7fe-115">Methods</span></span>

<span data-ttu-id="9e7fe-116">**Win32 \_ 目錄** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-116">The **Win32\_Directory** class has these methods.</span></span>



| <span data-ttu-id="9e7fe-117">方法</span><span class="sxs-lookup"><span data-stu-id="9e7fe-117">Method</span></span>                                                                                             | <span data-ttu-id="9e7fe-118">描述</span><span class="sxs-lookup"><span data-stu-id="9e7fe-118">Description</span></span>                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e7fe-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-directory.md)     | <span data-ttu-id="9e7fe-120">類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-120">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="9e7fe-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-directory.md) | <span data-ttu-id="9e7fe-122">類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-122">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="9e7fe-123">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-123">**Compress**</span></span>](compress-method-in-class-win32-directory.md)                                       | <span data-ttu-id="9e7fe-124">類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-124">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="9e7fe-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-125">**CompressEx**</span></span>](compressex-method-in-class-win32-directory.md)                                   | <span data-ttu-id="9e7fe-126">類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-126">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="9e7fe-127">**複製**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-127">**Copy**</span></span>](copy-method-in-class-win32-directory.md)                                               | <span data-ttu-id="9e7fe-128">類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-128">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                        |
| [<span data-ttu-id="9e7fe-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-129">**CopyEx**</span></span>](copyex-method-in-class-win32-directory.md)                                           | <span data-ttu-id="9e7fe-130">類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到 *FileName* 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-130">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                   |
| [<span data-ttu-id="9e7fe-131">**刪除**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-131">**Delete**</span></span>](delete-method-in-class-win32-directory.md)                                           | <span data-ttu-id="9e7fe-132">類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-132">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="9e7fe-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-directory.md)                                       | <span data-ttu-id="9e7fe-134">類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-134">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="9e7fe-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-directory.md)           | <span data-ttu-id="9e7fe-136">類別方法，這個方法會判斷呼叫端是否有 *許可權* 引數所指定的匯總許可權，不只是在檔案物件上，而是在共用上的檔案或目錄位於共用) 的 (。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-136">Class method that determines whether the caller has the aggregated permissions specified by the *Permissions* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="9e7fe-137">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-137">**Rename**</span></span>](rename-method-in-class-win32-directory.md)                                           | <span data-ttu-id="9e7fe-138">類別方法，會將物件路徑中指定的邏輯檔案 (或目錄) 重新命名。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="9e7fe-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-directory.md)                             | <span data-ttu-id="9e7fe-140">取得物件路徑中所指定之邏輯檔案擁有權的類別方法。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-140">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="9e7fe-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-directory.md)                         | <span data-ttu-id="9e7fe-142">取得物件路徑中所指定之邏輯檔案擁有權的類別方法。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="9e7fe-143">**解壓**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)                                   | <span data-ttu-id="9e7fe-144">Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-144">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="9e7fe-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-directory.md)                               | <span data-ttu-id="9e7fe-146">Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-146">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="9e7fe-147">屬性</span><span class="sxs-lookup"><span data-stu-id="9e7fe-147">Properties</span></span>

<span data-ttu-id="9e7fe-148">**Win32 \_ 目錄** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-148">The **Win32\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e7fe-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-152">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-153">位元遮罩，表示存取或執行目錄上特定作業所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-153">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="9e7fe-154">如需位值，請參閱檔案 [**和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="9e7fe-155">在 FAT 磁片區上，會改為傳回 **完整 \_ 存取** 值，表示物件上未設定任何安全性。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="9e7fe-156">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="9e7fe-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-158">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-158">Grants the right to read data from the file.</span></span> <span data-ttu-id="9e7fe-159">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-159">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="9e7fe-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-161">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-161">Grants the right to write data to the file.</span></span> <span data-ttu-id="9e7fe-162">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-162">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="9e7fe-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**檔案 \_\_將資料附加)  (檔案，或 \_ 將檔案新增 \_ 子目錄** (4) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-164">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-164">Grants the right to append data to the file.</span></span> <span data-ttu-id="9e7fe-165">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-165">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="9e7fe-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-167">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-167">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="9e7fe-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-169">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-169">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="9e7fe-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-171">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-171">Grants the right to execute a file.</span></span> <span data-ttu-id="9e7fe-172">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-172">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="9e7fe-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-174">授與刪除目錄的許可權，以及它所包含的所有檔案 (其子) ，即使檔案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-174">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="9e7fe-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-176">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-176">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="9e7fe-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-178">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-178">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="9e7fe-179"><span id="DELETE"></span><span id="delete"></span>**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-179"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-180">授與刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-180">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="9e7fe-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-182">授與安全描述項和擁有者的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-182">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="9e7fe-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-184">授與任意 ACL 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-184">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="9e7fe-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-186">指派寫入擁有者。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-186">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="9e7fe-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-188">同步存取，並允許進程等候物件進入已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-188">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span data-ttu-id="9e7fe-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**存取 \_SYSTEM \_ SECURITY** (18809343) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**ACCESS\_SYSTEM\_SECURITY** (18809343)</span></span>


</dt> <dd>

<span data-ttu-id="9e7fe-190">控制取得或設定物件安全描述項中 SACL 的能力。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-190">Controls the ability to get or set the SACL in an object's security descriptor.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9e7fe-191">**封存**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-191">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-192">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-194">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "應該封存" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-194">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-195">指出是否已設定資料夾的封存位。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-195">Indicates whether the archive bit on the folder has been set.</span></span> <span data-ttu-id="9e7fe-196">備份程式會使用封存位來識別應該備份的檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-196">The archive bit is used by backup programs to identify files that should be backed up.</span></span> <span data-ttu-id="9e7fe-197">若 **為 True**，則表示應該封存檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-197">If **True**, the file should be archived.</span></span>

<span data-ttu-id="9e7fe-198">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-198">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-199">**標題**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-202">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-203">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-203">A short textual description of the object.</span></span>

<span data-ttu-id="9e7fe-204">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-205">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-205">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-206">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-208">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-208">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-209">指出資料夾是否已壓縮。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-209">Indicates whether or not the folder has been compressed.</span></span> <span data-ttu-id="9e7fe-210">WMI 會辨識使用 WMI 本身或使用圖形化使用者介面壓縮的資料夾;但是，它並不會辨識。壓縮的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-210">WMI recognizes folders compressed using WMI itself or using the graphical user interface; it does not, however, recognize .ZIP files as being compressed.</span></span> <span data-ttu-id="9e7fe-211">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-211">If **True**, the file is compressed.</span></span>

<span data-ttu-id="9e7fe-212">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-213">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-213">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-216">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Compression Method" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-216">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-217">演算法或工具 (通常是) 用來壓縮邏輯檔案的方法。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-217">Algorithm or tool (usually a method) used to compress the logical file.</span></span> <span data-ttu-id="9e7fe-218">若無法 (或不需要的) 描述壓縮配置 (可能因為不知道) ，請使用下列文字：「未知」表示不知道邏輯檔案是否已壓縮;「已壓縮」表示壓縮檔案，但其壓縮配置未知或未洩漏;和「未壓縮」表示邏輯檔案未壓縮。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-218">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed; "Compressed" to represent that the file is compressed, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="9e7fe-219">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-220">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-220">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-223">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-223">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-224">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-224">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9e7fe-225">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-225">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9e7fe-226">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-226">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-227">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-227">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-228">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-230">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建立日期" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-231">檔案系統物件的建立日期。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-231">Date that the file system object was created.</span></span> <span data-ttu-id="9e7fe-232">如需使用 WMI 日期和時間格式的詳細資訊，請參閱 [wmi 工作：日期和時間](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-232">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="9e7fe-233">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-234">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-234">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-237">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統類別名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-237">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-238">範圍電腦系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-238">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="9e7fe-239">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-239">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-240">**CSName**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-240">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-243">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-244">儲存檔案系統物件的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-244">Name of the computer where the file system object is stored.</span></span>

<span data-ttu-id="9e7fe-245">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-245">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-246">**說明**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-249">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-250">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-250">A textual description of the object.</span></span>

<span data-ttu-id="9e7fe-251">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-252">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-252">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-253">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-255">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Drive" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-255">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-256">磁片磁碟機的磁碟機號 (包括儲存檔案系統物件的冒號) 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-256">Drive letter of the drive (including colon) where the file system object is stored.</span></span>

<span data-ttu-id="9e7fe-257">範例： "c："</span><span class="sxs-lookup"><span data-stu-id="9e7fe-257">Example: "c:"</span></span>

<span data-ttu-id="9e7fe-258">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-258">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-259">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-259">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-262">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "八點三個檔案名" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-262">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-263">資料夾的 MS-DOS 相容名稱。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-263">MS-DOS -compatible name for the folder.</span></span>

<span data-ttu-id="9e7fe-264">範例： "c： \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="9e7fe-264">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="9e7fe-265">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-266">**已加密**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-266">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-267">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-269">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encrypted" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-269">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-270">指出資料夾是否已加密。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-270">Indicates whether or not the folder has been encrypted.</span></span> <span data-ttu-id="9e7fe-271">若 **為 True**，則會加密資料夾。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-271">If **True**, the folder is encrypted.</span></span>

<span data-ttu-id="9e7fe-272">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-273">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-273">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-276">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encryption Method" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-277">用來加密邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-277">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="9e7fe-278">如果 (或不需要的) 描述加密配置 (可能基於安全性理由) ，請使用下列文字：「未知」表示不知道邏輯檔案是否已加密;「已加密」表示檔案已加密，但其加密配置不知道或未洩漏;和「未加密」表示邏輯檔案未加密。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-278">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted; "Encrypted" to represent that the file is encrypted, but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="9e7fe-279">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-280">**分機**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-280">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-283">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Extension" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-283">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-284">檔案系統物件的副檔名，不包括點 (。 ) ，可將副檔名與檔案名分隔開來。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-284">File name extension for the file system object, not including the dot (.) that separates the extension from the file name.</span></span>

<span data-ttu-id="9e7fe-285">範例： "txt"、"mof"、"mdb"</span><span class="sxs-lookup"><span data-stu-id="9e7fe-285">Examples: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="9e7fe-286">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-287">**FileName**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-287">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-290">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-290">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-291">檔案名 (沒有檔案的點或副檔名) 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-291">File name (without the dot or extension) of the file.</span></span>

<span data-ttu-id="9e7fe-292">範例： "autoexec"</span><span class="sxs-lookup"><span data-stu-id="9e7fe-292">Example: "autoexec"</span></span>

<span data-ttu-id="9e7fe-293">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-293">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-294">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-294">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-295">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-297">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-298">檔案系統物件的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-298">Size of the file system object, in bytes.</span></span> <span data-ttu-id="9e7fe-299">雖然資料夾具有 **FileSize** 屬性，但一律會傳回值0。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-299">Although folders possess a **FileSize** property, the value 0 is always returned.</span></span> <span data-ttu-id="9e7fe-300">若要判斷資料夾的大小，請使用 FileSystemObject，或新增資料夾中儲存的所有檔案大小。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-300">To determine the size of a folder, use the FileSystemObject or add up the size of all the files stored in the folder.</span></span>

<span data-ttu-id="9e7fe-301">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9e7fe-302">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-303">**FileType**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-303">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-306">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "檔案類型" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-307">**延伸** 模組屬性) 指定的檔案類型 (。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-307">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="9e7fe-308">例如，.mdb 檔案可能會有 Microsoft Access 應用程式的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-308">For example, an .mdb file is likely to have the file type Microsoft Access Application.</span></span> <span data-ttu-id="9e7fe-309">.Asp 檔可能會有檔案類型的 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-309">An .asp file likely has the file type HTML Document.</span></span> <span data-ttu-id="9e7fe-310">資料夾通常是以資料夾的形式來報告。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-310">Folders are typically reported simply as Folder.</span></span>

<span data-ttu-id="9e7fe-311">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-311">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-312">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-312">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-315">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 檔案系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="9e7fe-315">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-316">檔案系統的類別。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-316">Class of the file system.</span></span>

<span data-ttu-id="9e7fe-317">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-317">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-318">**FSName**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-318">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-321">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" File System Name ") </span><span class="sxs-lookup"><span data-stu-id="9e7fe-321">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-322">檔案系統的類型 (NTFS、FAT、FAT32) 安裝在檔案或資料夾所在的磁片磁碟機上。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-322">Type of file system (NTFS, FAT, FAT32) installed on the drive where the file or folder is located.</span></span>

<span data-ttu-id="9e7fe-323">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-324">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-324">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-325">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-327">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「隱藏」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-327">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-328">指出是否隱藏檔案系統物件。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-328">Indicates whether the file system object is hidden.</span></span> <span data-ttu-id="9e7fe-329">若 **為 True**，則表示檔案已隱藏。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-329">If **True**, the file is hidden.</span></span>

<span data-ttu-id="9e7fe-330">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-331">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-331">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-332">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-334">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="9e7fe-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-335">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-335">Indicates when the object was installed.</span></span> <span data-ttu-id="9e7fe-336">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-336">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9e7fe-337">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-338">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-338">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-339">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-341">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「目前的檔案開啟計數」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-341">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-342">檔案目前作用中的「檔案開啟」數目。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-342">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="9e7fe-343">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-343">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="9e7fe-344">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-345">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-345">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-346">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-346">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-348">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次存取」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-349">上次存取檔案的日期。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-349">Date the file was last accessed.</span></span> <span data-ttu-id="9e7fe-350">如需使用 WMI 日期和時間格式的詳細資訊，請參閱 [wmi 工作：日期和時間](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-350">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="9e7fe-351">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-352">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-352">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-353">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-353">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-355">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次修改」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-356">上次修改檔案的日期。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-356">Date the file was last modified.</span></span> <span data-ttu-id="9e7fe-357">如需使用 WMI 日期和時間格式的詳細資訊，請參閱 [wmi 工作：日期和時間](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-357">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="9e7fe-358">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-358">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-359">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-359">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-362">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9e7fe-362">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-363">Name 屬性是一個字串，代表繼承的名稱，做為檔案系統內的邏輯檔案實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-363">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="9e7fe-364">應提供完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-364">Full path names should be provided.</span></span> <span data-ttu-id="9e7fe-365">範例： C： \\ Windows \\ system \\win.ini</span><span class="sxs-lookup"><span data-stu-id="9e7fe-365">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="9e7fe-366">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-366">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-367">**路徑**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-368">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-370">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Path" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-371">檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-371">Path for the file.</span></span> <span data-ttu-id="9e7fe-372">路徑包括開頭和尾端的反斜線，而不是磁碟機號或資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-372">The path includes the leading and trailing backslashes, but not the drive letter or the folder name.</span></span>

<span data-ttu-id="9e7fe-373">針對 c： \\ windows \\ system32 wbem 資料夾 \\ ，路徑為 \\ windows \\ system32 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-373">For the folder c:\\windows\\system32\\wbem, the path is \\windows\\system32\\.</span></span> <span data-ttu-id="9e7fe-374">針對資料夾 c： \\ 腳本，路徑為 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-374">For the folder c:\\scripts, the path is \\.</span></span>

<span data-ttu-id="9e7fe-375">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-375">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-376">**讀**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-376">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-377">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-379">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可讀取" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-379">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-380">指出您是否可以讀取資料夾中的專案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-380">Indicates whether you can read items in the folder.</span></span> <span data-ttu-id="9e7fe-381">若 **為 True**，則表示可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-381">If **True**, the file can be read.</span></span>

<span data-ttu-id="9e7fe-382">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-383">**狀態**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-383">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-384">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-386">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-386">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-387">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-387">String that indicates the current status of the object.</span></span>

<span data-ttu-id="9e7fe-388">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9e7fe-389">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="9e7fe-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9e7fe-390">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9e7fe-391">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9e7fe-392">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e7fe-393">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9e7fe-394">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9e7fe-395">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9e7fe-396">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9e7fe-397">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9e7fe-398">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9e7fe-399">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9e7fe-400">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9e7fe-401">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e7fe-402">**系統**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-402">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-403">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-403">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-405">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "System File" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-405">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-406">指出物件是否為系統檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-406">Indicates whether the object is a system file.</span></span> <span data-ttu-id="9e7fe-407">若 **為 True**，表示檔案是系統檔案</span><span class="sxs-lookup"><span data-stu-id="9e7fe-407">If **True**, the file is a system file</span></span>

<span data-ttu-id="9e7fe-408">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-408">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e7fe-409">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-409">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e7fe-410">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-410">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e7fe-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e7fe-412">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可寫入" ) </span><span class="sxs-lookup"><span data-stu-id="9e7fe-412">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="9e7fe-413">若 **為 True**，則表示可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-413">If **True**, the file can be written.</span></span>

<span data-ttu-id="9e7fe-414">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-414">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e7fe-415">備註</span><span class="sxs-lookup"><span data-stu-id="9e7fe-415">Remarks</span></span>

<span data-ttu-id="9e7fe-416">**Win32 \_ 目錄** 類別衍生自 [**CIM \_ 目錄**](cim-directory.md)。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-416">The **Win32\_Directory** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

<span data-ttu-id="9e7fe-417">**概觀**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-417">**Overview**</span></span>

<span data-ttu-id="9e7fe-418">資料夾是設計來包含其他檔案系統物件的檔案系統物件。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-418">Folders are file system objects designed to contain other file system objects.</span></span> <span data-ttu-id="9e7fe-419">但是，這並不表示所有資料夾都是一樣的。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-419">This does not mean that all folders are alike, however.</span></span> <span data-ttu-id="9e7fe-420">相反地，資料夾會有相當大的差異。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-420">Instead, folders can vary considerably.</span></span> <span data-ttu-id="9e7fe-421">某些資料夾是操作系統資料夾，通常不應由腳本修改。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-421">Some folders are operating system folders, which generally should not be modified by a script.</span></span> <span data-ttu-id="9e7fe-422">某些資料夾是唯讀的，這表示使用者可以存取該資料夾的內容，但無法新增、刪除或修改這些內容。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-422">Some folders are read-only, which means that users can access the contents of that folder but cannot add to, delete from, or modify those contents.</span></span> <span data-ttu-id="9e7fe-423">某些資料夾會針對最佳儲存體進行壓縮，而其他資料夾則會被隱藏，使用者看不到。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-423">Some folders are compressed for optimal storage, while others are hidden and not visible to users.</span></span>

<span data-ttu-id="9e7fe-424">WMI 使用 **Win32 \_ 目錄** 類別來管理資料夾。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-424">WMI uses the **Win32\_Directory** class to manage folders.</span></span> <span data-ttu-id="9e7fe-425">此類別中提供的屬性和方法明顯與 [**CIM \_ 資料檔案**](cim-datafile.md) 類別中可用的屬性和方法相同，後者是用來管理檔案的類別。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-425">Significantly, the properties and methods available in this class are identical to the properties and methods available in the [**CIM\_DataFile**](cim-datafile.md) class, the class used to manage files.</span></span> <span data-ttu-id="9e7fe-426">這表示在您學到如何使用 WMI 管理資料夾之後，您將不需要任何額外的工作，也知道如何管理檔案。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-426">This means that after you have learned how to manage folders using WMI, you will, without any extra work, also know how to manage files.</span></span>

<span data-ttu-id="9e7fe-427">[**Win32 \_ 子目錄**](win32-subdirectory.md)關聯類別也用來管理檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-427">The [**Win32\_Subdirectory**](win32-subdirectory.md) association class is also used to manage files and folders.</span></span> <span data-ttu-id="9e7fe-428">**Win32 \_ 子目錄** 類別會關聯資料夾及其直屬子資料夾。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-428">The **Win32\_Subdirectory** class relates a folder and its immediate subfolders.</span></span> <span data-ttu-id="9e7fe-429">例如，在資料夾結構 C： \\ scripts 記錄檔中 \\ ，記錄是腳本的子資料夾，而腳本是根資料夾 C：的子資料夾 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-429">For example, in the folder structure C:\\Scripts\\Logs, Logs is a subfolder of Scripts, and Scripts is a subfolder of the root folder C:\\.</span></span> <span data-ttu-id="9e7fe-430">不過，記錄不會被視為 C：的子資料夾 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-430">However, Logs is not considered a subfolder of C:\\.</span></span>

<span data-ttu-id="9e7fe-431">您可以使用 **Win32 \_ 目錄** 類別取出檔案系統中任何資料夾的屬性。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-431">You can retrieve the properties of any folder in the file system using the **Win32\_Directory** class.</span></span> <span data-ttu-id="9e7fe-432">使用這個類別的可用屬性會顯示在表11.1 中。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-432">The properties available using this class are shown in Table 11.1.</span></span> <span data-ttu-id="9e7fe-433">若要抓取單一資料夾的屬性，請將 Windows 查詢語言 (WQL) Query 中的 **Win32 \_ 目錄** 類別，確定您包含資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-433">To retrieve the properties for a single folder, construct a Windows Query Language (WQL) query for the **Win32\_Directory** class, making sure that you include the name of the folder.</span></span> <span data-ttu-id="9e7fe-434">例如，此查詢系結至資料夾 D： \\ Archive：</span><span class="sxs-lookup"><span data-stu-id="9e7fe-434">For example, this query binds to the folder D:\\Archive:</span></span>

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

<span data-ttu-id="9e7fe-435">在 WQL 查詢中指定檔案或資料夾名稱時，請確定您使用兩個反斜線 (\\ \\) 來分隔路徑元件。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-435">When specifying a file or folder name in a WQL query, be sure you use two backslashes (\\\\) to separate path components.</span></span>

<span data-ttu-id="9e7fe-436">如果您想要限制單一磁片磁碟機的資料抓取，請包含指定磁碟機號的 Where 子句。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-436">If you want to limit data retrieval to a single disk drive, include a Where clause specifying the drive letter.</span></span> <span data-ttu-id="9e7fe-437">例如，此查詢會傳回磁片磁碟機 C：上所有資料夾的清單。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-437">For example, this query returns a list of all the folders on drive C:</span></span>

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

<span data-ttu-id="9e7fe-438">如果您需要列舉電腦上的所有資料夾，請注意此查詢可能需要花費很長的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-438">If you need to enumerate all the folders on a computer, be aware that this query can take an extended time to complete.</span></span>

## <a name="examples"></a><span data-ttu-id="9e7fe-439">範例</span><span class="sxs-lookup"><span data-stu-id="9e7fe-439">Examples</span></span>

<span data-ttu-id="9e7fe-440">下列 VBScript 範例會抓取資料夾 C：腳本的屬性 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-440">The following VBScript sample retrieves properties for the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



<span data-ttu-id="9e7fe-441">下列 VBScript 範例會傳回電腦上所有隱藏資料夾的清單。</span><span class="sxs-lookup"><span data-stu-id="9e7fe-441">The following VBScript sample returns a list of all the hidden folders on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="9e7fe-442">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e7fe-442">Requirements</span></span>



| <span data-ttu-id="9e7fe-443">需求</span><span class="sxs-lookup"><span data-stu-id="9e7fe-443">Requirement</span></span> | <span data-ttu-id="9e7fe-444">值</span><span class="sxs-lookup"><span data-stu-id="9e7fe-444">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7fe-445">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e7fe-445">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7fe-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e7fe-446">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e7fe-447">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e7fe-447">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7fe-448">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e7fe-448">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e7fe-449">命名空間</span><span class="sxs-lookup"><span data-stu-id="9e7fe-449">Namespace</span></span><br/>                | <span data-ttu-id="9e7fe-450">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9e7fe-450">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e7fe-451">MOF</span><span class="sxs-lookup"><span data-stu-id="9e7fe-451">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e7fe-452"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e7fe-452"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e7fe-453">DLL</span><span class="sxs-lookup"><span data-stu-id="9e7fe-453">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e7fe-454"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e7fe-454"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e7fe-455">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e7fe-455">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7fe-456">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="9e7fe-456">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dt>

<span data-ttu-id="9e7fe-457">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e7fe-457">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

