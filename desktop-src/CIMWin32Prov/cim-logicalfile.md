---
description: CIM \_ LogicalFile 類別代表資料的命名集合，可以是可執行程式碼，位於儲存區的檔案系統中。
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile
- CIM_LogicalFile.Caption
- CIM_LogicalFile.Description
- CIM_LogicalFile.InstallDate
- CIM_LogicalFile.Status
- CIM_LogicalFile.AccessMask
- CIM_LogicalFile.Archive
- CIM_LogicalFile.Compressed
- CIM_LogicalFile.CompressionMethod
- CIM_LogicalFile.CreationClassName
- CIM_LogicalFile.CreationDate
- CIM_LogicalFile.CSCreationClassName
- CIM_LogicalFile.CSName
- CIM_LogicalFile.Drive
- CIM_LogicalFile.EightDotThreeFileName
- CIM_LogicalFile.Encrypted
- CIM_LogicalFile.EncryptionMethod
- CIM_LogicalFile.Name
- CIM_LogicalFile.Extension
- CIM_LogicalFile.FileName
- CIM_LogicalFile.FileSize
- CIM_LogicalFile.FileType
- CIM_LogicalFile.FSCreationClassName
- CIM_LogicalFile.FSName
- CIM_LogicalFile.Hidden
- CIM_LogicalFile.InUseCount
- CIM_LogicalFile.LastAccessed
- CIM_LogicalFile.LastModified
- CIM_LogicalFile.Path
- CIM_LogicalFile.Readable
- CIM_LogicalFile.System
- CIM_LogicalFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a06d2abd1c4ad92d751afa6c8aa47c0cfaa8b1f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984544"
---
# <a name="cim_logicalfile-class"></a><span data-ttu-id="517ef-103">CIM \_ LogicalFile 類別</span><span class="sxs-lookup"><span data-stu-id="517ef-103">CIM\_LogicalFile class</span></span>

<span data-ttu-id="517ef-104">**CIM \_ LogicalFile** 類別代表資料的命名集合，可以是可執行程式碼，位於儲存區的檔案系統中。</span><span class="sxs-lookup"><span data-stu-id="517ef-104">The **CIM\_LogicalFile** class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="517ef-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="517ef-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="517ef-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="517ef-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="517ef-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="517ef-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="517ef-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="517ef-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="517ef-109">語法</span><span class="sxs-lookup"><span data-stu-id="517ef-109">Syntax</span></span>

``` syntax
[SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C559-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Files (CIM)"), AMENDMENT]
class CIM_LogicalFile : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="517ef-110">成員</span><span class="sxs-lookup"><span data-stu-id="517ef-110">Members</span></span>

<span data-ttu-id="517ef-111">**CIM \_ LogicalFile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="517ef-111">The **CIM\_LogicalFile** class has these types of members:</span></span>

-   [<span data-ttu-id="517ef-112">方法</span><span class="sxs-lookup"><span data-stu-id="517ef-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="517ef-113">屬性</span><span class="sxs-lookup"><span data-stu-id="517ef-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="517ef-114">方法</span><span class="sxs-lookup"><span data-stu-id="517ef-114">Methods</span></span>

<span data-ttu-id="517ef-115">**CIM \_ LogicalFile** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="517ef-115">The **CIM\_LogicalFile** class has these methods.</span></span>



| <span data-ttu-id="517ef-116">方法</span><span class="sxs-lookup"><span data-stu-id="517ef-116">Method</span></span>                                                                                             | <span data-ttu-id="517ef-117">描述</span><span class="sxs-lookup"><span data-stu-id="517ef-117">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="517ef-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="517ef-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | <span data-ttu-id="517ef-119">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="517ef-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="517ef-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="517ef-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="517ef-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | <span data-ttu-id="517ef-122">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="517ef-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="517ef-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="517ef-124">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="517ef-124">**Compress**</span></span>](compress-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="517ef-125">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="517ef-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="517ef-127">**CompressEx**</span></span>](compressex-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="517ef-128">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-129">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="517ef-130">**複製**</span><span class="sxs-lookup"><span data-stu-id="517ef-130">**Copy**</span></span>](copy-method-in-class-cim-logicalfile.md)                                               | <span data-ttu-id="517ef-131">將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="517ef-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="517ef-132">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="517ef-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="517ef-133">**CopyEx**</span></span>](copyex-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="517ef-134">將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="517ef-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="517ef-135">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="517ef-136">**刪除**</span><span class="sxs-lookup"><span data-stu-id="517ef-136">**Delete**</span></span>](delete-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="517ef-137">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-138">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="517ef-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="517ef-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="517ef-140">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-141">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="517ef-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="517ef-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)           | <span data-ttu-id="517ef-143">判斷呼叫端是否具有 **許可權** 引數所指定的匯總許可權。</span><span class="sxs-lookup"><span data-stu-id="517ef-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="517ef-144">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="517ef-145">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="517ef-145">**Rename**</span></span>](rename-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="517ef-146">重新命名在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-147">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="517ef-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="517ef-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-logicalfile.md)                             | <span data-ttu-id="517ef-149">取得在物件路徑中指定的邏輯檔案 (或目錄) 的擁有權。</span><span class="sxs-lookup"><span data-stu-id="517ef-149">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-150">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-150">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="517ef-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="517ef-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)                         | <span data-ttu-id="517ef-152">取得在物件路徑中指定的邏輯檔案 (或目錄) 的擁有權。</span><span class="sxs-lookup"><span data-stu-id="517ef-152">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-153">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-153">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="517ef-154">**解壓**</span><span class="sxs-lookup"><span data-stu-id="517ef-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="517ef-155">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-156">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="517ef-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="517ef-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-logicalfile.md)                               | <span data-ttu-id="517ef-158">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="517ef-159">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="517ef-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="517ef-160">屬性</span><span class="sxs-lookup"><span data-stu-id="517ef-160">Properties</span></span>

<span data-ttu-id="517ef-161">**CIM \_ LogicalFile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="517ef-161">The **CIM\_LogicalFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="517ef-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="517ef-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="517ef-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-165">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-166">位元遮罩，表示存取或執行檔案上特定作業所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="517ef-166">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="517ef-167">如需位值，請參閱檔案 [**和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)。</span><span class="sxs-lookup"><span data-stu-id="517ef-167">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="517ef-168">在 FAT 磁片區上，會改為傳回 **完整 \_ 存取** 值，表示物件上未設定任何安全性。</span><span class="sxs-lookup"><span data-stu-id="517ef-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="517ef-169">**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="517ef-169">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="517ef-170">**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="517ef-170">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="517ef-171">**檔案 \_\_將資料附加)  (檔案或檔案 \_ 新增 \_ 子目錄 (目錄)** (4) </span><span class="sxs-lookup"><span data-stu-id="517ef-171">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="517ef-172">**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="517ef-172">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="517ef-173">**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="517ef-173">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="517ef-174">**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="517ef-174">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="517ef-175">**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="517ef-175">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="517ef-176">**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="517ef-176">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="517ef-177">**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="517ef-177">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="517ef-178">**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="517ef-178">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="517ef-179">**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="517ef-179">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="517ef-180">**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="517ef-180">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="517ef-181">**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="517ef-181">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="517ef-182">**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="517ef-182">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="517ef-183">**封存**</span><span class="sxs-lookup"><span data-stu-id="517ef-183">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="517ef-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-186">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "應該封存" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-187">若 **為 True**，則表示應該封存檔案。</span><span class="sxs-lookup"><span data-stu-id="517ef-187">If **True**, the file should be archived.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-188">**標題**</span><span class="sxs-lookup"><span data-stu-id="517ef-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-191">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-192">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="517ef-192">A short textual description of the object.</span></span>

<span data-ttu-id="517ef-193">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="517ef-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="517ef-194">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="517ef-194">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-195">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="517ef-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-197">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-197">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-198">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="517ef-198">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="517ef-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-202">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Compression Method" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-202">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-203">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="517ef-203">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="517ef-204">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="517ef-204">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="517ef-205">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="517ef-205">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="517ef-206">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="517ef-206">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="517ef-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="517ef-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-210">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-210">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-211">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="517ef-211">Name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-212">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="517ef-212">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-213">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="517ef-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-215">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建立日期" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-216">建立檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="517ef-216">Date and time of the file's creation.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-217">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="517ef-217">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-220">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統類別名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-220">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-221">電腦系統的類別。</span><span class="sxs-lookup"><span data-stu-id="517ef-221">Class of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-222">**CSName**</span><span class="sxs-lookup"><span data-stu-id="517ef-222">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-225">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-225">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-226">電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="517ef-226">Name of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-227">**說明**</span><span class="sxs-lookup"><span data-stu-id="517ef-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-230">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-231">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="517ef-231">A textual description of the object.</span></span>

<span data-ttu-id="517ef-232">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="517ef-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="517ef-233">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="517ef-233">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-236">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Drive" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-236">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-237">磁碟機號 (包括在檔案的磁碟機號) 後面的冒號。</span><span class="sxs-lookup"><span data-stu-id="517ef-237">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="517ef-238">這個屬性繼承自 **CIM \_ LogicalFile**。範例： "c："</span><span class="sxs-lookup"><span data-stu-id="517ef-238">This property is inherited from **CIM\_LogicalFile**.Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="517ef-239">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="517ef-239">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-242">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "八點三個檔案名" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-243">DOS 相容的檔案名。</span><span class="sxs-lookup"><span data-stu-id="517ef-243">DOS-compatible file name.</span></span> <span data-ttu-id="517ef-244">範例： "c： \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="517ef-244">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="517ef-245">**已加密**</span><span class="sxs-lookup"><span data-stu-id="517ef-245">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-246">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="517ef-246">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-248">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encrypted" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-248">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-249">若 **為 True**，則表示檔案已加密。</span><span class="sxs-lookup"><span data-stu-id="517ef-249">If **True**, the file is encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-250">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="517ef-250">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-253">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encryption Method" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-254">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="517ef-254">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="517ef-255">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="517ef-255">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="517ef-256">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="517ef-256">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="517ef-257">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="517ef-257">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="517ef-258">**分機**</span><span class="sxs-lookup"><span data-stu-id="517ef-258">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-259">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-261">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Extension" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-261">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-262">沒有前一個期間的副檔名 (點) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-262">File name extension without the preceding period (dot).</span></span> <span data-ttu-id="517ef-263">範例： "txt"、"mof"、"mdb"</span><span class="sxs-lookup"><span data-stu-id="517ef-263">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="517ef-264">**FileName**</span><span class="sxs-lookup"><span data-stu-id="517ef-264">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-265">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-267">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-267">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-268">不含副檔名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="517ef-268">File name without the file name extension.</span></span> <span data-ttu-id="517ef-269">範例： "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="517ef-269">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="517ef-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="517ef-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-271">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="517ef-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-273">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-274">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="517ef-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="517ef-275">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="517ef-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="517ef-276">**FileType**</span><span class="sxs-lookup"><span data-stu-id="517ef-276">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-277">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-279">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "檔案類型" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-280">表示 **擴充** 屬性所表示之檔案類型的描述元。</span><span class="sxs-lookup"><span data-stu-id="517ef-280">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="517ef-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-284">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 檔案系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="517ef-284">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-285">檔案系統的類別。</span><span class="sxs-lookup"><span data-stu-id="517ef-285">Class of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-286">**FSName**</span><span class="sxs-lookup"><span data-stu-id="517ef-286">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-287">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-289">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" File System Name ") </span><span class="sxs-lookup"><span data-stu-id="517ef-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-290">檔案系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="517ef-290">Name of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-291">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="517ef-291">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-292">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="517ef-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-294">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「隱藏」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-295">若 **為 True**，則表示檔案已隱藏。</span><span class="sxs-lookup"><span data-stu-id="517ef-295">If **True**, the file is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-296">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="517ef-296">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-297">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="517ef-297">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-299">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="517ef-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-300">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="517ef-300">Indicates when the object was installed.</span></span> <span data-ttu-id="517ef-301">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="517ef-301">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="517ef-302">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="517ef-302">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="517ef-303">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="517ef-303">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-304">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="517ef-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-306">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「目前的檔案開啟計數」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-307">檔案目前作用中的「檔案開啟」數目。</span><span class="sxs-lookup"><span data-stu-id="517ef-307">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="517ef-308">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="517ef-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="517ef-309">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="517ef-309">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-310">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="517ef-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-312">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次存取」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-313">上次存取檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="517ef-313">Date and time the file was last accessed.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-314">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="517ef-314">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-315">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="517ef-315">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-317">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次修改」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-318">上次修改檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="517ef-318">Date and time the file was last modified.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-319">**名稱**</span><span class="sxs-lookup"><span data-stu-id="517ef-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-322">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="517ef-322">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="517ef-323">Name 屬性是一個字串，代表繼承的名稱，做為檔案系統內的邏輯檔案實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="517ef-323">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="517ef-324">應提供完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="517ef-324">Full path names should be provided.</span></span> <span data-ttu-id="517ef-325">範例： C： \\ Windows \\ system \\win.ini</span><span class="sxs-lookup"><span data-stu-id="517ef-325">Example: C:\\Windows\\system\\win.ini</span></span>

</dd> <dt>

<span data-ttu-id="517ef-326">**路徑**</span><span class="sxs-lookup"><span data-stu-id="517ef-326">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-327">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-329">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Path" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-329">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-330">檔案的路徑，包括開頭和尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="517ef-330">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="517ef-331">範例： " \\ windows \\ system \\ "</span><span class="sxs-lookup"><span data-stu-id="517ef-331">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="517ef-332">**讀**</span><span class="sxs-lookup"><span data-stu-id="517ef-332">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-333">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="517ef-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-335">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可讀取" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-336">若 **為 True**，則表示可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="517ef-336">If **True**, the file can be read.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-337">**狀態**</span><span class="sxs-lookup"><span data-stu-id="517ef-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="517ef-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-340">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-340">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-341">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="517ef-341">String that indicates the current status of the object.</span></span> <span data-ttu-id="517ef-342">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="517ef-342">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="517ef-343">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="517ef-343">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="517ef-344">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="517ef-344">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="517ef-345">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="517ef-345">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="517ef-346">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="517ef-346">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="517ef-347">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="517ef-347">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="517ef-348">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="517ef-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="517ef-349">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="517ef-349">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="517ef-350">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="517ef-350">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="517ef-351">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-351">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="517ef-352">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-352">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="517ef-353">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-353">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="517ef-354">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-354">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="517ef-355">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-355">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="517ef-356">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-356">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="517ef-357">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-357">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="517ef-358">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-358">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="517ef-359">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-359">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="517ef-360">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-360">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="517ef-361">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="517ef-361">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="517ef-362">**系統**</span><span class="sxs-lookup"><span data-stu-id="517ef-362">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-363">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="517ef-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-365">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "System File" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-366">若 **為 True**，表示檔案為系統檔案。</span><span class="sxs-lookup"><span data-stu-id="517ef-366">If **True**, the file is a system file.</span></span>

</dd> <dt>

<span data-ttu-id="517ef-367">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="517ef-367">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517ef-368">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="517ef-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="517ef-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="517ef-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="517ef-370">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可寫入" ) </span><span class="sxs-lookup"><span data-stu-id="517ef-370">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="517ef-371">若 **為 True**，則表示可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="517ef-371">If **True**, the file can be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="517ef-372">備註</span><span class="sxs-lookup"><span data-stu-id="517ef-372">Remarks</span></span>

<span data-ttu-id="517ef-373">**Cim \_ LogicalFile** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="517ef-373">The **CIM\_LogicalFile** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="517ef-374">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="517ef-374">WMI does not implement this class.</span></span> <span data-ttu-id="517ef-375">針對衍生自 **CIM \_ LogicalFile** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="517ef-375">For classes derived from **CIM\_LogicalFile**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="517ef-376">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="517ef-376">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="517ef-377">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="517ef-377">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="517ef-378">規格需求</span><span class="sxs-lookup"><span data-stu-id="517ef-378">Requirements</span></span>



| <span data-ttu-id="517ef-379">需求</span><span class="sxs-lookup"><span data-stu-id="517ef-379">Requirement</span></span> | <span data-ttu-id="517ef-380">值</span><span class="sxs-lookup"><span data-stu-id="517ef-380">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="517ef-381">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="517ef-381">Minimum supported client</span></span><br/> | <span data-ttu-id="517ef-382">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="517ef-382">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="517ef-383">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="517ef-383">Minimum supported server</span></span><br/> | <span data-ttu-id="517ef-384">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="517ef-384">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="517ef-385">命名空間</span><span class="sxs-lookup"><span data-stu-id="517ef-385">Namespace</span></span><br/>                | <span data-ttu-id="517ef-386">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="517ef-386">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="517ef-387">MOF</span><span class="sxs-lookup"><span data-stu-id="517ef-387">MOF</span></span><br/>                      | <dl> <span data-ttu-id="517ef-388"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="517ef-388"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="517ef-389">DLL</span><span class="sxs-lookup"><span data-stu-id="517ef-389">DLL</span></span><br/>                      | <dl> <span data-ttu-id="517ef-390"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="517ef-390"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="517ef-391">另請參閱</span><span class="sxs-lookup"><span data-stu-id="517ef-391">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517ef-392">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="517ef-392">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

