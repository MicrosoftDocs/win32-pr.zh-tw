---
description: CIM 資料 \_ 檔類別代表資料的命名集合或可執行檔程式碼。 只會傳回本機固定磁片上的檔案實例。
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: CIM_DataFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile
- CIM_DataFile.Caption
- CIM_DataFile.Description
- CIM_DataFile.InstallDate
- CIM_DataFile.Status
- CIM_DataFile.AccessMask
- CIM_DataFile.Archive
- CIM_DataFile.Compressed
- CIM_DataFile.CompressionMethod
- CIM_DataFile.CreationClassName
- CIM_DataFile.CreationDate
- CIM_DataFile.CSCreationClassName
- CIM_DataFile.CSName
- CIM_DataFile.Drive
- CIM_DataFile.EightDotThreeFileName
- CIM_DataFile.Encrypted
- CIM_DataFile.EncryptionMethod
- CIM_DataFile.Name
- CIM_DataFile.Extension
- CIM_DataFile.FileName
- CIM_DataFile.FileSize
- CIM_DataFile.FileType
- CIM_DataFile.FSCreationClassName
- CIM_DataFile.FSName
- CIM_DataFile.Hidden
- CIM_DataFile.InUseCount
- CIM_DataFile.LastAccessed
- CIM_DataFile.LastModified
- CIM_DataFile.Path
- CIM_DataFile.Readable
- CIM_DataFile.System
- CIM_DataFile.Writeable
- CIM_DataFile.Manufacturer
- CIM_DataFile.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0badba05eafa5cba06e48b8494ca893936af360e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847368"
---
# <a name="cim_datafile-class"></a><span data-ttu-id="f9912-104">CIM \_ 資料檔案類別</span><span class="sxs-lookup"><span data-stu-id="f9912-104">CIM\_DataFile class</span></span>

<span data-ttu-id="f9912-105">**CIM 資料 \_ 檔** 類別代表資料的命名集合或可執行檔程式碼。</span><span class="sxs-lookup"><span data-stu-id="f9912-105">The **CIM\_DataFile** class represents a named collection of data or executable code.</span></span> <span data-ttu-id="f9912-106">只會傳回本機固定磁片上的檔案實例。</span><span class="sxs-lookup"><span data-stu-id="f9912-106">Only instances of files on local fixed disks will be returned.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9912-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f9912-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f9912-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f9912-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f9912-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f9912-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f9912-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f9912-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9912-111">語法</span><span class="sxs-lookup"><span data-stu-id="f9912-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
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
};
```

## <a name="members"></a><span data-ttu-id="f9912-112">成員</span><span class="sxs-lookup"><span data-stu-id="f9912-112">Members</span></span>

<span data-ttu-id="f9912-113">**CIM \_ 資料檔案** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f9912-113">The **CIM\_DataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="f9912-114">方法</span><span class="sxs-lookup"><span data-stu-id="f9912-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="f9912-115">屬性</span><span class="sxs-lookup"><span data-stu-id="f9912-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f9912-116">方法</span><span class="sxs-lookup"><span data-stu-id="f9912-116">Methods</span></span>

<span data-ttu-id="f9912-117">**CIM \_ 資料檔案** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f9912-117">The **CIM\_DataFile** class has these methods.</span></span>



| <span data-ttu-id="f9912-118">方法</span><span class="sxs-lookup"><span data-stu-id="f9912-118">Method</span></span>                                                                                          | <span data-ttu-id="f9912-119">描述</span><span class="sxs-lookup"><span data-stu-id="f9912-119">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9912-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="f9912-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)     | <span data-ttu-id="f9912-121">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="f9912-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="f9912-122">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-122">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="f9912-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="f9912-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md) | <span data-ttu-id="f9912-124">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="f9912-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="f9912-125">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-125">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="f9912-126">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="f9912-126">**Compress**</span></span>](compress-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="f9912-127">使用 NTFS 壓縮來壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-127">Uses NTFS compression to compress the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f9912-128">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-128">Implemented by WMI.</span></span><br/>                       |
| [<span data-ttu-id="f9912-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="f9912-129">**CompressEx**</span></span>](compressex-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="f9912-130">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f9912-131">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-131">Implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="f9912-132">**複製**</span><span class="sxs-lookup"><span data-stu-id="f9912-132">**Copy**</span></span>](copy-method-in-class-cim-datafile.md)                                               | <span data-ttu-id="f9912-133">將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="f9912-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="f9912-134">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-134">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="f9912-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="f9912-135">**CopyEx**</span></span>](copyex-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="f9912-136">將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="f9912-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="f9912-137">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-137">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="f9912-138">**刪除**</span><span class="sxs-lookup"><span data-stu-id="f9912-138">**Delete**</span></span>](delete-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="f9912-139">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f9912-140">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-140">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="f9912-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="f9912-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="f9912-142">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f9912-143">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-143">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="f9912-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="f9912-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-datafile.md)           | <span data-ttu-id="f9912-145">判斷呼叫端是否具有 **許可權** 引數所指定的匯總許可權。</span><span class="sxs-lookup"><span data-stu-id="f9912-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="f9912-146">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-146">Implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="f9912-147">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="f9912-147">**Rename**</span></span>](rename-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="f9912-148">重新命名在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f9912-149">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-149">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="f9912-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="f9912-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-datafile.md)                             | <span data-ttu-id="f9912-151">取得物件路徑中指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="f9912-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="f9912-152">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-152">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="f9912-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="f9912-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-datafile.md)                         | <span data-ttu-id="f9912-154">取得物件路徑中指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="f9912-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="f9912-155">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-155">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="f9912-156">**解壓**</span><span class="sxs-lookup"><span data-stu-id="f9912-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="f9912-157">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f9912-158">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-158">Implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="f9912-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="f9912-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-datafile.md)                               | <span data-ttu-id="f9912-160">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f9912-161">由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f9912-161">Implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="f9912-162">屬性</span><span class="sxs-lookup"><span data-stu-id="f9912-162">Properties</span></span>

<span data-ttu-id="f9912-163">**CIM \_ 資料檔案** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f9912-163">The **CIM\_DataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9912-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="f9912-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f9912-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-167">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-168">位元遮罩，表示存取或執行檔案上特定作業所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="f9912-168">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="f9912-169">如需位值，請參閱檔案 [**和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)。</span><span class="sxs-lookup"><span data-stu-id="f9912-169">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="f9912-170">在 FAT 磁片區上，會改為傳回 **完整 \_ 存取** 值，表示物件上未設定任何安全性。</span><span class="sxs-lookup"><span data-stu-id="f9912-170">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="f9912-171">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-171">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="f9912-172">**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="f9912-172">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="f9912-173">**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="f9912-173">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="f9912-174">**檔案 \_\_將資料附加)  (檔案或檔案 \_ 新增 \_ 子目錄 (目錄)** (4) </span><span class="sxs-lookup"><span data-stu-id="f9912-174">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="f9912-175">**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="f9912-175">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="f9912-176">**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="f9912-176">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="f9912-177">**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="f9912-177">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="f9912-178">**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="f9912-178">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="f9912-179">**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="f9912-179">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="f9912-180">**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="f9912-180">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="f9912-181">**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="f9912-181">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="f9912-182">**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="f9912-182">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="f9912-183">**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="f9912-183">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="f9912-184">**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="f9912-184">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="f9912-185">**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="f9912-185">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9912-186">**封存**</span><span class="sxs-lookup"><span data-stu-id="f9912-186">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-187">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f9912-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-189">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "應該封存" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-190">若 **為 True**，則表示應該封存檔案。</span><span class="sxs-lookup"><span data-stu-id="f9912-190">If **True**, the file should be archived.</span></span>

<span data-ttu-id="f9912-191">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-191">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-192">**標題**</span><span class="sxs-lookup"><span data-stu-id="f9912-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-195">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-196">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="f9912-196">A short textual description of the object.</span></span>

<span data-ttu-id="f9912-197">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-198">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="f9912-198">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-199">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f9912-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-201">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-202">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="f9912-202">If **True**, the file is compressed.</span></span>

<span data-ttu-id="f9912-203">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-203">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-204">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="f9912-204">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-207">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Compression Method" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-207">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-208">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="f9912-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="f9912-209">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="f9912-209">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="f9912-210">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="f9912-210">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="f9912-211">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="f9912-211">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="f9912-212">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-213">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f9912-213">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-216">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-216">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-217">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9912-217">Name of the class.</span></span>

<span data-ttu-id="f9912-218">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-219">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="f9912-219">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-220">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f9912-220">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-222">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建立日期" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-223">建立檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f9912-223">Date and time of the file's creation.</span></span>

<span data-ttu-id="f9912-224">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-224">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-225">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f9912-225">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-226">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-228">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統類別名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-228">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-229">電腦系統的類別。</span><span class="sxs-lookup"><span data-stu-id="f9912-229">Class of the computer system.</span></span>

<span data-ttu-id="f9912-230">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-230">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-231">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f9912-231">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-234">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-234">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-235">電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9912-235">Name of the computer system.</span></span>

<span data-ttu-id="f9912-236">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-236">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-237">**說明**</span><span class="sxs-lookup"><span data-stu-id="f9912-237">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-238">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-240">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-241">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="f9912-241">A textual description of the object.</span></span>

<span data-ttu-id="f9912-242">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-243">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="f9912-243">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-246">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Drive" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-246">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-247">磁碟機號 (包括在檔案的磁碟機號) 後面的冒號。</span><span class="sxs-lookup"><span data-stu-id="f9912-247">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="f9912-248">範例： "c："</span><span class="sxs-lookup"><span data-stu-id="f9912-248">Example: "c:"</span></span>

<span data-ttu-id="f9912-249">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-249">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-250">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="f9912-250">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-253">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "八點三個檔案名" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-253">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-254">DOS 相容的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f9912-254">DOS-compatible file name.</span></span>

<span data-ttu-id="f9912-255">範例： "c： \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="f9912-255">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="f9912-256">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-256">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-257">**已加密**</span><span class="sxs-lookup"><span data-stu-id="f9912-257">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-258">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f9912-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-260">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encrypted" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-260">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-261">若 **為 True**，則表示檔案已加密。</span><span class="sxs-lookup"><span data-stu-id="f9912-261">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="f9912-262">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-263">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="f9912-263">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-266">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encryption Method" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-267">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="f9912-267">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="f9912-268">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="f9912-268">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="f9912-269">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="f9912-269">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="f9912-270">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="f9912-270">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="f9912-271">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-271">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-272">**分機**</span><span class="sxs-lookup"><span data-stu-id="f9912-272">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-275">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Extension" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-275">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-276">沒有前一個期間的副檔名 (點) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-276">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="f9912-277">範例： "txt"、"mof"、"mdb"</span><span class="sxs-lookup"><span data-stu-id="f9912-277">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="f9912-278">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-278">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-279">**FileName**</span><span class="sxs-lookup"><span data-stu-id="f9912-279">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-280">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-282">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-282">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-283">不含副檔名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f9912-283">File name without the file name extension.</span></span> <span data-ttu-id="f9912-284">範例： "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="f9912-284">Example: "MyDataFile"</span></span>

<span data-ttu-id="f9912-285">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-285">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-286">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="f9912-286">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-287">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f9912-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-289">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-290">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f9912-290">Size of the file, in bytes.</span></span>

<span data-ttu-id="f9912-291">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="f9912-291">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f9912-292">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-293">**FileType**</span><span class="sxs-lookup"><span data-stu-id="f9912-293">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-296">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "檔案類型" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-296">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-297">表示 **擴充** 屬性所表示之檔案類型的描述元。</span><span class="sxs-lookup"><span data-stu-id="f9912-297">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="f9912-298">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-299">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f9912-299">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-302">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 檔案系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="f9912-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-303">檔案系統的類別。</span><span class="sxs-lookup"><span data-stu-id="f9912-303">Class of the file system.</span></span>

<span data-ttu-id="f9912-304">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-304">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-305">**FSName**</span><span class="sxs-lookup"><span data-stu-id="f9912-305">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-306">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-308">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" File System Name ") </span><span class="sxs-lookup"><span data-stu-id="f9912-308">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-309">檔案系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9912-309">Name of the file system.</span></span>

<span data-ttu-id="f9912-310">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-311">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="f9912-311">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-312">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f9912-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-314">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「隱藏」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-314">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-315">若 **為 True**，則表示檔案已隱藏。</span><span class="sxs-lookup"><span data-stu-id="f9912-315">If **True**, the file is hidden.</span></span>

<span data-ttu-id="f9912-316">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-316">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f9912-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-318">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f9912-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-320">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="f9912-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-321">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="f9912-321">Indicates when the object was installed.</span></span> <span data-ttu-id="f9912-322">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="f9912-322">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f9912-323">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-324">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="f9912-324">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-325">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f9912-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-327">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「目前的檔案開啟計數」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-328">檔案目前作用中的「檔案開啟」數目。</span><span class="sxs-lookup"><span data-stu-id="f9912-328">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="f9912-329">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="f9912-329">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f9912-330">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-331">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="f9912-331">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-332">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f9912-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-334">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次存取」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-335">上次存取檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f9912-335">Date and time the file was last accessed.</span></span>

<span data-ttu-id="f9912-336">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-337">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="f9912-337">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-338">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f9912-338">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-340">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次修改」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-341">上次修改檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f9912-341">Date and time the file was last modified.</span></span>

<span data-ttu-id="f9912-342">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-342">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-343">**製造商**</span><span class="sxs-lookup"><span data-stu-id="f9912-343">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-344">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-346">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "製造商" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-347">版本資源 (的製造商字串（如果有的話) ）。</span><span class="sxs-lookup"><span data-stu-id="f9912-347">Manufacturer string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-348">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f9912-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-351">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9912-351">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f9912-352">Name 屬性是一個字串，代表繼承的名稱，做為檔案系統內的邏輯檔案實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f9912-352">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="f9912-353">應提供完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="f9912-353">Full path names should be provided.</span></span>

<span data-ttu-id="f9912-354">範例： C： \\ Windows \\ system \\win.ini</span><span class="sxs-lookup"><span data-stu-id="f9912-354">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="f9912-355">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-355">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-356">**路徑**</span><span class="sxs-lookup"><span data-stu-id="f9912-356">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-357">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-359">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Path" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-359">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-360">檔案的路徑，包括開頭和尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="f9912-360">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="f9912-361">範例： " \\ windows \\ system \\ "</span><span class="sxs-lookup"><span data-stu-id="f9912-361">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="f9912-362">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-362">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-363">**讀**</span><span class="sxs-lookup"><span data-stu-id="f9912-363">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-364">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f9912-364">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-366">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可讀取" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-366">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-367">若 **為 True**，則表示可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="f9912-367">If **True**, the file can be read.</span></span>

<span data-ttu-id="f9912-368">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-368">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-369">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f9912-369">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-370">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-372">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-372">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-373">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="f9912-373">String that indicates the current status of the object.</span></span> <span data-ttu-id="f9912-374">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="f9912-374">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f9912-375">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="f9912-375">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f9912-376">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-376">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f9912-377">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="f9912-377">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f9912-378">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="f9912-378">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f9912-379">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="f9912-379">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f9912-380">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f9912-381">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="f9912-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f9912-382">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f9912-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f9912-383">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f9912-384">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f9912-385">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f9912-386">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f9912-387">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f9912-388">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f9912-389">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f9912-390">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f9912-391">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f9912-392">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f9912-393">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="f9912-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9912-394">**系統**</span><span class="sxs-lookup"><span data-stu-id="f9912-394">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-395">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f9912-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-397">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "System File" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-397">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-398">若 **為 True**，表示檔案為系統檔案。</span><span class="sxs-lookup"><span data-stu-id="f9912-398">If **True**, the file is a system file.</span></span>

<span data-ttu-id="f9912-399">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-400">**版本**</span><span class="sxs-lookup"><span data-stu-id="f9912-400">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9912-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-403">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Version" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-404">版本資源 (的版本字串（如果有的話）) 。</span><span class="sxs-lookup"><span data-stu-id="f9912-404">Version string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="f9912-405">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="f9912-405">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9912-406">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f9912-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9912-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9912-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9912-408">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可寫入" ) </span><span class="sxs-lookup"><span data-stu-id="f9912-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="f9912-409">若 **為 True**，則表示可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="f9912-409">If **True**, the file can be written.</span></span>

<span data-ttu-id="f9912-410">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9912-411">備註</span><span class="sxs-lookup"><span data-stu-id="f9912-411">Remarks</span></span>

<span data-ttu-id="f9912-412">**Cim \_ 資料檔案** 類別衍生自 [**cim \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f9912-412">The **CIM\_DataFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="f9912-413">WMI 會實行 **CIM \_ 資料檔案** 類別及其所有方法。</span><span class="sxs-lookup"><span data-stu-id="f9912-413">WMI implements the **CIM\_DataFile** class and all of its methods.</span></span> <span data-ttu-id="f9912-414">**CIM \_ 資料檔案** 類別是動態類別。</span><span class="sxs-lookup"><span data-stu-id="f9912-414">The **CIM\_DataFile** class is a dynamic class.</span></span>

<span data-ttu-id="f9912-415">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f9912-415">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f9912-416">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f9912-416">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="f9912-417">基於安全性考慮，WMI 不直接支援呼叫遠端電腦，並指示它將檔案複製到本身。</span><span class="sxs-lookup"><span data-stu-id="f9912-417">Due to security purposes, WMI does not directly support calling a remote computer and instructing it to copy files to itself.</span></span> <span data-ttu-id="f9912-418">不過，您可以使用相關的程式設計語言來呼叫 FTP 或 RoboCopy。</span><span class="sxs-lookup"><span data-stu-id="f9912-418">However, you can use the relevant programming language to call FTP or RoboCopy, for example.</span></span>

## <a name="examples"></a><span data-ttu-id="f9912-419">範例</span><span class="sxs-lookup"><span data-stu-id="f9912-419">Examples</span></span>

<span data-ttu-id="f9912-420">下列腳本中心程式 [代碼範例](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) 會使用 **CIM \_ 資料檔案** 類別作為較大應用程式的一部分，以使用 Powershell 來產生 exchange 環境報告。</span><span class="sxs-lookup"><span data-stu-id="f9912-420">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) uses a **CIM\_DataFile** class as part of a larger application to Generate exchange environment reports using Powershell.</span></span>

<span data-ttu-id="f9912-421">TechNet 元件庫中的 [Find files WITH WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) 程式碼範例會使用 **CIM \_ 資料檔案** 來搜尋多部電腦上的一個或多個檔案。</span><span class="sxs-lookup"><span data-stu-id="f9912-421">The [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) code sample in TechNet Gallery uses a **CIM\_DataFile** to search for one or more files across multiple computers.</span></span>

<span data-ttu-id="f9912-422">下列 VBS 程式碼範例說明如何在資料檔案上執行標準萬用字元搜尋。</span><span class="sxs-lookup"><span data-stu-id="f9912-422">The following VBS code sample describes how to perform a standard wildcard search on a datafile.</span></span> <span data-ttu-id="f9912-423">請注意，反斜線分隔符號必須以另一個反斜線 () 來進行轉義 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="f9912-423">Note that the backslash delimiters must be escaped with another backslash (\\\\).</span></span> <span data-ttu-id="f9912-424">此外，使用「**CIM \_ 資料檔案**」時。**FileName**"WHERE 子句中的 WMIPRVSE 進程會掃描任何可用儲存裝置上的所有目錄。</span><span class="sxs-lookup"><span data-stu-id="f9912-424">Also, when using "**CIM\_DataFile**.**FileName**" in the WHERE clause, the WMIPRVSE process will scan all directories on any available storage device.</span></span> <span data-ttu-id="f9912-425">這可能需要一些時間，特別是如果您已對應遠端共用，而且可能會觸發防毒軟體警告。</span><span class="sxs-lookup"><span data-stu-id="f9912-425">This may take some time, especially if you have mapped remote shares, and can trigger antivirus warnings.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



<span data-ttu-id="f9912-426">下列程式碼片段會將搜尋範圍限制為特定磁片磁碟機、路徑和副檔名。</span><span class="sxs-lookup"><span data-stu-id="f9912-426">The following snippet limits the search range to a specific drive, path, and file extension.</span></span>


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



<span data-ttu-id="f9912-427">下列 PowerShell 程式碼範例會捕獲單一屬性值。</span><span class="sxs-lookup"><span data-stu-id="f9912-427">The following PowerShell code sample retrieves a single attribute value.</span></span>


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## <a name="requirements"></a><span data-ttu-id="f9912-428">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9912-428">Requirements</span></span>



| <span data-ttu-id="f9912-429">需求</span><span class="sxs-lookup"><span data-stu-id="f9912-429">Requirement</span></span> | <span data-ttu-id="f9912-430">值</span><span class="sxs-lookup"><span data-stu-id="f9912-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9912-431">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9912-431">Minimum supported client</span></span><br/> | <span data-ttu-id="f9912-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9912-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9912-433">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9912-433">Minimum supported server</span></span><br/> | <span data-ttu-id="f9912-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9912-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9912-435">命名空間</span><span class="sxs-lookup"><span data-stu-id="f9912-435">Namespace</span></span><br/>                | <span data-ttu-id="f9912-436">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f9912-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f9912-437">MOF</span><span class="sxs-lookup"><span data-stu-id="f9912-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9912-438"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9912-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9912-439">DLL</span><span class="sxs-lookup"><span data-stu-id="f9912-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9912-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9912-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9912-441">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9912-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9912-442">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="f9912-442">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="f9912-443">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="f9912-443">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="f9912-444">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="f9912-444">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

