---
description: CIM \_ 目錄類別代表以邏輯方式分組其包含之資料檔案的檔案類型，並提供群組檔案的路徑資訊。
ms.assetid: a9594f53-08f0-4a47-9edc-51686c80c5ea
ms.tgt_platform: multiple
title: CIM_Directory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory
- CIM_Directory.AccessMask
- CIM_Directory.Archive
- CIM_Directory.Caption
- CIM_Directory.Compressed
- CIM_Directory.CompressionMethod
- CIM_Directory.CreationClassName
- CIM_Directory.CreationDate
- CIM_Directory.CSCreationClassName
- CIM_Directory.CSName
- CIM_Directory.Description
- CIM_Directory.Drive
- CIM_Directory.EightDotThreeFileName
- CIM_Directory.Encrypted
- CIM_Directory.EncryptionMethod
- CIM_Directory.Extension
- CIM_Directory.FileName
- CIM_Directory.FileSize
- CIM_Directory.FileType
- CIM_Directory.FSCreationClassName
- CIM_Directory.FSName
- CIM_Directory.Hidden
- CIM_Directory.InstallDate
- CIM_Directory.InUseCount
- CIM_Directory.LastAccessed
- CIM_Directory.LastModified
- CIM_Directory.Name
- CIM_Directory.Path
- CIM_Directory.Readable
- CIM_Directory.Status
- CIM_Directory.System
- CIM_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cebab65cc067018b3a57aa5f6890fffad1cb4c7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970335"
---
# <a name="cim_directory-class"></a><span data-ttu-id="02706-103">CIM \_ 目錄類別</span><span class="sxs-lookup"><span data-stu-id="02706-103">CIM\_Directory class</span></span>

<span data-ttu-id="02706-104">**CIM \_ 目錄** 類別代表以邏輯方式分組其包含之資料檔案的檔案類型，並提供群組檔案的路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="02706-104">The **CIM\_Directory** class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02706-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="02706-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02706-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="02706-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="02706-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="02706-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="02706-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="02706-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02706-109">語法</span><span class="sxs-lookup"><span data-stu-id="02706-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C55F-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Directories (CIM)"), AMENDMENT]
class CIM_Directory : CIM_LogicalFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
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
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="02706-110">成員</span><span class="sxs-lookup"><span data-stu-id="02706-110">Members</span></span>

<span data-ttu-id="02706-111">**CIM \_ 目錄** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="02706-111">The **CIM\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="02706-112">方法</span><span class="sxs-lookup"><span data-stu-id="02706-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="02706-113">屬性</span><span class="sxs-lookup"><span data-stu-id="02706-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="02706-114">方法</span><span class="sxs-lookup"><span data-stu-id="02706-114">Methods</span></span>

<span data-ttu-id="02706-115">**CIM \_ 目錄** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="02706-115">The **CIM\_Directory** class has these methods.</span></span>



| <span data-ttu-id="02706-116">方法</span><span class="sxs-lookup"><span data-stu-id="02706-116">Method</span></span>                                                                                           | <span data-ttu-id="02706-117">描述</span><span class="sxs-lookup"><span data-stu-id="02706-117">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02706-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="02706-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)     | <span data-ttu-id="02706-119">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="02706-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="02706-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="02706-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="02706-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md) | <span data-ttu-id="02706-122">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="02706-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="02706-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="02706-124">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="02706-124">**Compress**</span></span>](compress-method-in-class-cim-directory.md)                                       | <span data-ttu-id="02706-125">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="02706-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="02706-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="02706-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="02706-127">**CompressEx**</span></span>](compressex-method-in-class-cim-directory.md)                                   | <span data-ttu-id="02706-128">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="02706-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="02706-129">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="02706-130">**複製**</span><span class="sxs-lookup"><span data-stu-id="02706-130">**Copy**</span></span>](copy-method-in-class-cim-directory.md)                                               | <span data-ttu-id="02706-131">將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="02706-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="02706-132">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="02706-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="02706-133">**CopyEx**</span></span>](copyex-method-in-class-cim-directory.md)                                           | <span data-ttu-id="02706-134">將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="02706-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="02706-135">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="02706-136">**刪除**</span><span class="sxs-lookup"><span data-stu-id="02706-136">**Delete**</span></span>](delete-method-in-class-cim-directory.md)                                           | <span data-ttu-id="02706-137">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="02706-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="02706-138">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="02706-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="02706-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-directory.md)                                       | <span data-ttu-id="02706-140">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="02706-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="02706-141">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="02706-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="02706-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)           | <span data-ttu-id="02706-143">判斷呼叫端是否具有 **許可權** 引數所指定的匯總許可權。</span><span class="sxs-lookup"><span data-stu-id="02706-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="02706-144">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="02706-145">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="02706-145">**Rename**</span></span>](rename-method-in-class-cim-directory.md)                                           | <span data-ttu-id="02706-146">重新命名在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="02706-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="02706-147">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="02706-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="02706-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-directory.md)                             | <span data-ttu-id="02706-149">取得物件路徑中指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="02706-149">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="02706-150">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-150">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="02706-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="02706-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-directory.md)                         | <span data-ttu-id="02706-152">取得物件路徑中指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="02706-152">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="02706-153">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-153">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="02706-154">**解壓**</span><span class="sxs-lookup"><span data-stu-id="02706-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-directory.md)                                   | <span data-ttu-id="02706-155">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="02706-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="02706-156">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="02706-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="02706-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-directory.md)                               | <span data-ttu-id="02706-158">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="02706-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="02706-159">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="02706-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="02706-160">屬性</span><span class="sxs-lookup"><span data-stu-id="02706-160">Properties</span></span>

<span data-ttu-id="02706-161">**CIM \_ 目錄** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="02706-161">The **CIM\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02706-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="02706-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="02706-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02706-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-165">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) </span><span class="sxs-lookup"><span data-stu-id="02706-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="02706-166">位元遮罩，表示存取或執行目錄上特定作業所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="02706-166">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="02706-167">如需值，請參閱檔案 [**和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)。</span><span class="sxs-lookup"><span data-stu-id="02706-167">For values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="02706-168">在 FAT 磁片區上，會改為傳回 **完整 \_ 存取** 值，表示物件上未設定任何安全性。</span><span class="sxs-lookup"><span data-stu-id="02706-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="02706-169">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-169">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="02706-170">**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="02706-170">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="02706-171">**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="02706-171">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="02706-172">**檔案 \_\_將資料附加)  (檔案或檔案 \_ 新增 \_ 子目錄 (目錄)** (4) </span><span class="sxs-lookup"><span data-stu-id="02706-172">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="02706-173">**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="02706-173">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="02706-174">**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="02706-174">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="02706-175">**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="02706-175">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="02706-176">**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="02706-176">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="02706-177">**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="02706-177">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="02706-178">**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="02706-178">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="02706-179">**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="02706-179">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="02706-180">**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="02706-180">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="02706-181">**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="02706-181">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="02706-182">**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="02706-182">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="02706-183">**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="02706-183">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02706-184">**封存**</span><span class="sxs-lookup"><span data-stu-id="02706-184">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-185">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="02706-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02706-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-187">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "應該封存" ) </span><span class="sxs-lookup"><span data-stu-id="02706-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="02706-188">若 **為 True**，則表示應該封存檔案。</span><span class="sxs-lookup"><span data-stu-id="02706-188">If **True**, the file should be archived.</span></span>

<span data-ttu-id="02706-189">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-189">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-190">**標題**</span><span class="sxs-lookup"><span data-stu-id="02706-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-193">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="02706-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="02706-194">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="02706-194">Short textual description of the object.</span></span>

<span data-ttu-id="02706-195">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-196">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="02706-196">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-197">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="02706-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02706-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-199">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-199">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="02706-200">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="02706-200">If **True**, the file is compressed.</span></span>

<span data-ttu-id="02706-201">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-202">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="02706-202">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-205">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Compression Method" ) </span><span class="sxs-lookup"><span data-stu-id="02706-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="02706-206">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="02706-206">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="02706-207">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="02706-207">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="02706-208">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="02706-208">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="02706-209">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="02706-209">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="02706-210">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-210">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-211">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="02706-211">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-212">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-214">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="02706-214">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="02706-215">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="02706-215">Name of the class.</span></span>

<span data-ttu-id="02706-216">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-216">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-217">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="02706-217">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-218">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="02706-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="02706-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-220">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建立日期" ) </span><span class="sxs-lookup"><span data-stu-id="02706-220">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="02706-221">建立檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="02706-221">Date and time that the file was created.</span></span>

<span data-ttu-id="02706-222">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-222">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-223">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="02706-223">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-226">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統類別名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-226">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="02706-227">電腦系統的類別。</span><span class="sxs-lookup"><span data-stu-id="02706-227">Class of the computer system.</span></span>

<span data-ttu-id="02706-228">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-228">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-229">**CSName**</span><span class="sxs-lookup"><span data-stu-id="02706-229">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-232">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-232">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="02706-233">電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="02706-233">Name of the computer system.</span></span>

<span data-ttu-id="02706-234">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-235">**說明**</span><span class="sxs-lookup"><span data-stu-id="02706-235">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-238">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="02706-238">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="02706-239">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="02706-239">Textual description of the object.</span></span>

<span data-ttu-id="02706-240">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-241">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="02706-241">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-244">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Drive" ) </span><span class="sxs-lookup"><span data-stu-id="02706-244">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="02706-245">磁碟機號 (包括在檔案的磁碟機號) 後面的冒號。</span><span class="sxs-lookup"><span data-stu-id="02706-245">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="02706-246">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="02706-247">範例： "c："</span><span class="sxs-lookup"><span data-stu-id="02706-247">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="02706-248">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="02706-248">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-251">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "八點三個檔案名" ) </span><span class="sxs-lookup"><span data-stu-id="02706-251">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="02706-252">DOS 相容的檔案名。</span><span class="sxs-lookup"><span data-stu-id="02706-252">DOS-compatible file name.</span></span> <span data-ttu-id="02706-253">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="02706-254">範例： "c： \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="02706-254">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="02706-255">**已加密**</span><span class="sxs-lookup"><span data-stu-id="02706-255">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-256">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="02706-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02706-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-258">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encrypted" ) </span><span class="sxs-lookup"><span data-stu-id="02706-258">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="02706-259">若 **為 True**，則表示檔案已加密。</span><span class="sxs-lookup"><span data-stu-id="02706-259">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="02706-260">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-261">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="02706-261">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-262">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-264">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encryption Method" ) </span><span class="sxs-lookup"><span data-stu-id="02706-264">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="02706-265">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="02706-265">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="02706-266">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="02706-266">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="02706-267">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="02706-267">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="02706-268">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="02706-268">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="02706-269">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-270">**分機**</span><span class="sxs-lookup"><span data-stu-id="02706-270">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-271">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-273">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Extension" ) </span><span class="sxs-lookup"><span data-stu-id="02706-273">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="02706-274">沒有前一個期間的副檔名 (點) 。</span><span class="sxs-lookup"><span data-stu-id="02706-274">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="02706-275">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="02706-276">範例： "txt"、"mof"、"mdb"</span><span class="sxs-lookup"><span data-stu-id="02706-276">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="02706-277">**FileName**</span><span class="sxs-lookup"><span data-stu-id="02706-277">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-280">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) </span><span class="sxs-lookup"><span data-stu-id="02706-280">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="02706-281">不含副檔名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="02706-281">File name without the file name extension.</span></span>

<span data-ttu-id="02706-282">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="02706-283">範例： "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="02706-283">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="02706-284">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="02706-284">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-285">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="02706-285">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="02706-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-287">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="02706-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="02706-288">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="02706-288">Size of the file, in bytes.</span></span>

<span data-ttu-id="02706-289">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-289">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="02706-290">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="02706-290">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="02706-291">**FileType**</span><span class="sxs-lookup"><span data-stu-id="02706-291">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-294">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "檔案類型" ) </span><span class="sxs-lookup"><span data-stu-id="02706-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="02706-295">描述) **擴充** 屬性所表示之檔案類型 (的描述項。</span><span class="sxs-lookup"><span data-stu-id="02706-295">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="02706-296">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-296">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-297">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="02706-297">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-300">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 檔案系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="02706-300">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="02706-301">檔案系統的類別。</span><span class="sxs-lookup"><span data-stu-id="02706-301">Class of the file system.</span></span>

<span data-ttu-id="02706-302">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-303">**FSName**</span><span class="sxs-lookup"><span data-stu-id="02706-303">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-306">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" File System Name ") </span><span class="sxs-lookup"><span data-stu-id="02706-306">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="02706-307">檔案系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="02706-307">Name of the file system.</span></span>

<span data-ttu-id="02706-308">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-309">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="02706-309">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-310">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="02706-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02706-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-312">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「隱藏」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-312">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="02706-313">若 **為 True**，則表示檔案已隱藏。</span><span class="sxs-lookup"><span data-stu-id="02706-313">If **True**, the file is hidden.</span></span>

<span data-ttu-id="02706-314">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-314">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-315">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="02706-315">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-316">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="02706-316">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="02706-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-318">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="02706-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="02706-319">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="02706-319">Date and time when the object was installed.</span></span> <span data-ttu-id="02706-320">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="02706-320">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="02706-321">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-322">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="02706-322">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-323">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="02706-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="02706-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-325">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「目前的檔案開啟計數」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="02706-326">檔案目前作用中的「檔案開啟」數目。</span><span class="sxs-lookup"><span data-stu-id="02706-326">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="02706-327">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="02706-328">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="02706-328">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="02706-329">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="02706-329">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-330">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="02706-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="02706-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-332">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次存取」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="02706-333">上次存取檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="02706-333">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="02706-334">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-334">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-335">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="02706-335">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-336">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="02706-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="02706-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-338">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次修改」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-338">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="02706-339">上次修改檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="02706-339">Date and time that the file was last modified.</span></span>

<span data-ttu-id="02706-340">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-340">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-341">**名稱**</span><span class="sxs-lookup"><span data-stu-id="02706-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-344">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02706-344">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="02706-345">作為檔案系統內邏輯檔案實例之索引鍵的繼承名稱 (提供完整路徑名稱) 。</span><span class="sxs-lookup"><span data-stu-id="02706-345">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="02706-346">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="02706-347">範例： "C： \\ Windows \\ system \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="02706-347">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="02706-348">**路徑**</span><span class="sxs-lookup"><span data-stu-id="02706-348">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-351">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Path" ) </span><span class="sxs-lookup"><span data-stu-id="02706-351">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="02706-352">檔案的路徑，包括開頭和尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="02706-352">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="02706-353">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="02706-354">範例： " \\ windows \\ system \\ "</span><span class="sxs-lookup"><span data-stu-id="02706-354">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="02706-355">**讀**</span><span class="sxs-lookup"><span data-stu-id="02706-355">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-356">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="02706-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02706-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-358">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可讀取" ) </span><span class="sxs-lookup"><span data-stu-id="02706-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="02706-359">若 **為 True**，則表示可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="02706-359">If **True**, the file can be read.</span></span>

<span data-ttu-id="02706-360">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-360">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-361">**狀態**</span><span class="sxs-lookup"><span data-stu-id="02706-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-362">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02706-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02706-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-364">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="02706-364">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="02706-365">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="02706-365">String that indicates the current status of the object.</span></span>

<span data-ttu-id="02706-366">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="02706-367">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="02706-367">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="02706-368">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="02706-368">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="02706-369">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-369">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="02706-370">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-370">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02706-371">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-371">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="02706-372">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-372">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="02706-373">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-373">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="02706-374">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-374">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="02706-375">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-375">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="02706-376">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-376">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="02706-377">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="02706-377">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="02706-378">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-378">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="02706-379">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="02706-379">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02706-380">**系統**</span><span class="sxs-lookup"><span data-stu-id="02706-380">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-381">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="02706-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02706-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-383">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "System File" ) </span><span class="sxs-lookup"><span data-stu-id="02706-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="02706-384">若 **為 True**，表示檔案為系統檔案。</span><span class="sxs-lookup"><span data-stu-id="02706-384">If **True**, the file is a system file.</span></span>

<span data-ttu-id="02706-385">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-385">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02706-386">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="02706-386">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02706-387">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="02706-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02706-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02706-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02706-389">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可寫入" ) </span><span class="sxs-lookup"><span data-stu-id="02706-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="02706-390">若 **為 True**，則表示可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="02706-390">If **True**, the file can be written.</span></span>

<span data-ttu-id="02706-391">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-391">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02706-392">備註</span><span class="sxs-lookup"><span data-stu-id="02706-392">Remarks</span></span>

<span data-ttu-id="02706-393">**Cim \_ 目錄** 類別衍生自 [**cim \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-393">The **CIM\_Directory** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="02706-394">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="02706-394">WMI does not implement this class.</span></span> <span data-ttu-id="02706-395">如需衍生自 **CIM \_ 目錄** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="02706-395">For more information about classes derived from **CIM\_Directory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="02706-396">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="02706-396">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02706-397">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="02706-397">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02706-398">規格需求</span><span class="sxs-lookup"><span data-stu-id="02706-398">Requirements</span></span>



| <span data-ttu-id="02706-399">需求</span><span class="sxs-lookup"><span data-stu-id="02706-399">Requirement</span></span> | <span data-ttu-id="02706-400">值</span><span class="sxs-lookup"><span data-stu-id="02706-400">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02706-401">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02706-401">Minimum supported client</span></span><br/> | <span data-ttu-id="02706-402">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02706-402">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02706-403">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02706-403">Minimum supported server</span></span><br/> | <span data-ttu-id="02706-404">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02706-404">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02706-405">命名空間</span><span class="sxs-lookup"><span data-stu-id="02706-405">Namespace</span></span><br/>                | <span data-ttu-id="02706-406">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="02706-406">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02706-407">MOF</span><span class="sxs-lookup"><span data-stu-id="02706-407">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02706-408"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="02706-408"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02706-409">DLL</span><span class="sxs-lookup"><span data-stu-id="02706-409">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02706-410"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02706-410"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02706-411">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02706-411">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02706-412">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="02706-412">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

