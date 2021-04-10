---
description: CIM \_ DeviceFile 類別代表代表裝置的邏輯檔案類型。
ms.assetid: b07f039c-8ab0-4e13-96d5-3621da19e66d
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile
- CIM_DeviceFile.AccessMask
- CIM_DeviceFile.Archive
- CIM_DeviceFile.Caption
- CIM_DeviceFile.Compressed
- CIM_DeviceFile.CompressionMethod
- CIM_DeviceFile.CreationClassName
- CIM_DeviceFile.CreationDate
- CIM_DeviceFile.CSCreationClassName
- CIM_DeviceFile.CSName
- CIM_DeviceFile.Description
- CIM_DeviceFile.Drive
- CIM_DeviceFile.EightDotThreeFileName
- CIM_DeviceFile.Encrypted
- CIM_DeviceFile.EncryptionMethod
- CIM_DeviceFile.Extension
- CIM_DeviceFile.FileName
- CIM_DeviceFile.FileSize
- CIM_DeviceFile.FileType
- CIM_DeviceFile.FSCreationClassName
- CIM_DeviceFile.FSName
- CIM_DeviceFile.Hidden
- CIM_DeviceFile.InstallDate
- CIM_DeviceFile.InUseCount
- CIM_DeviceFile.LastAccessed
- CIM_DeviceFile.LastModified
- CIM_DeviceFile.Name
- CIM_DeviceFile.Path
- CIM_DeviceFile.Readable
- CIM_DeviceFile.Status
- CIM_DeviceFile.System
- CIM_DeviceFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 476f0ecd212247e1fc96db3efedcc0c18a6a2e06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936386"
---
# <a name="cim_devicefile-class"></a><span data-ttu-id="ea05f-103">CIM \_ DeviceFile 類別</span><span class="sxs-lookup"><span data-stu-id="ea05f-103">CIM\_DeviceFile class</span></span>

<span data-ttu-id="ea05f-104">**CIM \_ DeviceFile** 類別代表代表裝置的邏輯檔案類型。</span><span class="sxs-lookup"><span data-stu-id="ea05f-104">The **CIM\_DeviceFile** class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="ea05f-105">此慣例適用于使用位元組串流 i/o 模型管理裝置的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ea05f-105">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="ea05f-106">與此檔案相關聯的邏輯裝置是使用 [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) 關聯性所指定。</span><span class="sxs-lookup"><span data-stu-id="ea05f-106">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea05f-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="ea05f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ea05f-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ea05f-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ea05f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ea05f-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ea05f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea05f-111">語法</span><span class="sxs-lookup"><span data-stu-id="ea05f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{4333BD60-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceFile : CIM_LogicalFile
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

## <a name="members"></a><span data-ttu-id="ea05f-112">成員</span><span class="sxs-lookup"><span data-stu-id="ea05f-112">Members</span></span>

<span data-ttu-id="ea05f-113">**CIM \_ DeviceFile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ea05f-113">The **CIM\_DeviceFile** class has these types of members:</span></span>

-   [<span data-ttu-id="ea05f-114">方法</span><span class="sxs-lookup"><span data-stu-id="ea05f-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea05f-115">屬性</span><span class="sxs-lookup"><span data-stu-id="ea05f-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea05f-116">方法</span><span class="sxs-lookup"><span data-stu-id="ea05f-116">Methods</span></span>

<span data-ttu-id="ea05f-117">**CIM \_ DeviceFile** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ea05f-117">The **CIM\_DeviceFile** class has these methods.</span></span>



| <span data-ttu-id="ea05f-118">方法</span><span class="sxs-lookup"><span data-stu-id="ea05f-118">Method</span></span>                                                                                            | <span data-ttu-id="ea05f-119">描述</span><span class="sxs-lookup"><span data-stu-id="ea05f-119">Description</span></span>                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea05f-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="ea05f-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)     | <span data-ttu-id="ea05f-121">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="ea05f-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-122">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="ea05f-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="ea05f-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | <span data-ttu-id="ea05f-124">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="ea05f-125">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-125">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="ea05f-126">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="ea05f-126">**Compress**</span></span>](compress-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="ea05f-127">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-127">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ea05f-128">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-128">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="ea05f-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="ea05f-129">**CompressEx**</span></span>](compressex-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="ea05f-130">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ea05f-131">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-131">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="ea05f-132">**複製**</span><span class="sxs-lookup"><span data-stu-id="ea05f-132">**Copy**</span></span>](copy-method-in-class-cim-devicefile.md)                                               | <span data-ttu-id="ea05f-133">將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="ea05f-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="ea05f-134">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-134">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="ea05f-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="ea05f-135">**CopyEx**</span></span>](copyex-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="ea05f-136">將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="ea05f-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="ea05f-137">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-137">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="ea05f-138">**刪除**</span><span class="sxs-lookup"><span data-stu-id="ea05f-138">**Delete**</span></span>](delete-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="ea05f-139">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ea05f-140">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-140">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ea05f-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="ea05f-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="ea05f-142">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ea05f-143">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-143">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ea05f-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="ea05f-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)           | <span data-ttu-id="ea05f-145">判斷呼叫端是否具有 **許可權** 引數所指定的匯總許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="ea05f-146">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-146">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="ea05f-147">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="ea05f-147">**Rename**</span></span>](rename-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="ea05f-148">重新命名在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ea05f-149">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-149">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ea05f-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="ea05f-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-devicefile.md)                             | <span data-ttu-id="ea05f-151">取得物件路徑中指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="ea05f-152">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-152">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="ea05f-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="ea05f-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-devicefile.md)                         | <span data-ttu-id="ea05f-154">取得物件路徑中指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="ea05f-155">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-155">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="ea05f-156">**解壓**</span><span class="sxs-lookup"><span data-stu-id="ea05f-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="ea05f-157">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ea05f-158">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-158">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="ea05f-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="ea05f-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-devicefile.md)                               | <span data-ttu-id="ea05f-160">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ea05f-161">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ea05f-161">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="ea05f-162">屬性</span><span class="sxs-lookup"><span data-stu-id="ea05f-162">Properties</span></span>

<span data-ttu-id="ea05f-163">**CIM \_ DeviceFile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ea05f-163">The **CIM\_DeviceFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea05f-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="ea05f-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ea05f-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-167">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-168">代表傳回實例之使用者或群組所持有之指定檔案或目錄之存取權限的位陣列。</span><span class="sxs-lookup"><span data-stu-id="ea05f-168">Bit array that represents the access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="ea05f-169">在 FAT 磁片區上，會傳回 **完整 \_ 存取權** ，這表示物件上未設定任何安全性。</span><span class="sxs-lookup"><span data-stu-id="ea05f-169">On FAT volumes, **FULL\_ACCESS** is returned, which indicates that no security has been set on the object.</span></span>

<span data-ttu-id="ea05f-170">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-170">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ea05f-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="ea05f-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-172">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-172">Grants the right to read data from the file.</span></span> <span data-ttu-id="ea05f-173">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="ea05f-173">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="ea05f-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="ea05f-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-175">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-175">Grants the right to write data to the file.</span></span> <span data-ttu-id="ea05f-176">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-176">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ea05f-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**檔案 \_\_將資料附加)  (檔案或檔案 \_ 新增 \_ 子目錄 (目錄)** (4) </span><span class="sxs-lookup"><span data-stu-id="ea05f-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-178">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-178">Grants the right to append data to the file.</span></span> <span data-ttu-id="ea05f-179">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-179">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="ea05f-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="ea05f-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-181">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-181">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="ea05f-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="ea05f-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-183">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-183">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="ea05f-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="ea05f-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-185">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="ea05f-185">Grants the right to execute a file.</span></span> <span data-ttu-id="ea05f-186">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="ea05f-186">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="ea05f-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="ea05f-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-188">授與刪除目錄的許可權，以及它所包含的所有檔案 (其子) ，即使檔案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ea05f-188">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="ea05f-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="ea05f-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-190">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-190">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="ea05f-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="ea05f-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-192">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-192">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="ea05f-193"><span id="DELETE"></span><span id="delete"></span>**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="ea05f-193"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-194">授與刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="ea05f-194">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="ea05f-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="ea05f-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-196">授與安全描述項和擁有者的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="ea05f-196">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="ea05f-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="ea05f-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-198">授與任意 ACL 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="ea05f-198">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="ea05f-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="ea05f-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-200">指派寫入擁有者。</span><span class="sxs-lookup"><span data-stu-id="ea05f-200">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="ea05f-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="ea05f-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="ea05f-202">同步存取，並允許進程等候物件進入已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="ea05f-202">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea05f-203">**封存**</span><span class="sxs-lookup"><span data-stu-id="ea05f-203">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-204">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ea05f-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-206">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "應該封存" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-206">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-207">若 **為 True**，則表示應該封存檔案。</span><span class="sxs-lookup"><span data-stu-id="ea05f-207">If **True**, the file should be archived.</span></span>

<span data-ttu-id="ea05f-208">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-209">**標題**</span><span class="sxs-lookup"><span data-stu-id="ea05f-209">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-212">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-213">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="ea05f-213">Short textual description of the object.</span></span>

<span data-ttu-id="ea05f-214">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-215">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="ea05f-215">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-216">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ea05f-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-218">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-218">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-219">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="ea05f-219">If **True**, the file is compressed.</span></span>

<span data-ttu-id="ea05f-220">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-221">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="ea05f-221">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-224">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Compression Method" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-224">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-225">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="ea05f-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="ea05f-226">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="ea05f-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="ea05f-227">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="ea05f-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="ea05f-228">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="ea05f-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="ea05f-229">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-229">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-230">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea05f-230">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-233">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-233">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-234">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea05f-234">Name of the class.</span></span>

<span data-ttu-id="ea05f-235">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-235">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-236">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="ea05f-236">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-237">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ea05f-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-239">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建立日期" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-240">檔案的建立日期。</span><span class="sxs-lookup"><span data-stu-id="ea05f-240">File's creation date.</span></span>

<span data-ttu-id="ea05f-241">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-242">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea05f-242">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-245">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統類別名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-245">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-246">電腦系統的類別。</span><span class="sxs-lookup"><span data-stu-id="ea05f-246">Class of the computer system.</span></span>

<span data-ttu-id="ea05f-247">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-247">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-248">**CSName**</span><span class="sxs-lookup"><span data-stu-id="ea05f-248">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-251">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-251">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-252">電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea05f-252">Name of the computer system.</span></span>

<span data-ttu-id="ea05f-253">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-254">**說明**</span><span class="sxs-lookup"><span data-stu-id="ea05f-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-257">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-258">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="ea05f-258">Textual description of the object.</span></span>

<span data-ttu-id="ea05f-259">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-260">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="ea05f-260">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-263">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Drive" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-263">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-264">磁碟機號 (包括在檔案的磁碟機號) 後面的冒號。</span><span class="sxs-lookup"><span data-stu-id="ea05f-264">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="ea05f-265">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ea05f-266">範例： "c："</span><span class="sxs-lookup"><span data-stu-id="ea05f-266">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-267">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="ea05f-267">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-268">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-270">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "八點三個檔案名" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-270">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-271">檔案的 DOS 相容檔案名。</span><span class="sxs-lookup"><span data-stu-id="ea05f-271">DOS-compatible file name for the file.</span></span> <span data-ttu-id="ea05f-272">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ea05f-273">範例： "c： \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="ea05f-273">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-274">**已加密**</span><span class="sxs-lookup"><span data-stu-id="ea05f-274">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-275">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ea05f-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-277">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encrypted" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-278">若 **為 True**，則表示檔案已加密。</span><span class="sxs-lookup"><span data-stu-id="ea05f-278">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="ea05f-279">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-280">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="ea05f-280">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-283">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encryption Method" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-283">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-284">識別用來加密邏輯檔案之演算法或工具的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="ea05f-284">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="ea05f-285">如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="ea05f-285">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="ea05f-286">如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。</span><span class="sxs-lookup"><span data-stu-id="ea05f-286">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="ea05f-287">如果邏輯檔案未加密，請使用「未加密」。</span><span class="sxs-lookup"><span data-stu-id="ea05f-287">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="ea05f-288">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-289">**分機**</span><span class="sxs-lookup"><span data-stu-id="ea05f-289">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-290">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-292">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Extension" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-292">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-293">沒有前一個期間的副檔名 (點) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-293">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="ea05f-294">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ea05f-295">範例： "txt"、"mof"、"mdb"</span><span class="sxs-lookup"><span data-stu-id="ea05f-295">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-296">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ea05f-296">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-299">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-299">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-300">不含副檔名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ea05f-300">File name without the file name extension.</span></span>

<span data-ttu-id="ea05f-301">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ea05f-302">範例： "MyDataFile"</span><span class="sxs-lookup"><span data-stu-id="ea05f-302">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-303">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="ea05f-303">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-304">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ea05f-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-306">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-307">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ea05f-307">Size of the file, in bytes.</span></span>

<span data-ttu-id="ea05f-308">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ea05f-309">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-310">**FileType**</span><span class="sxs-lookup"><span data-stu-id="ea05f-310">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-313">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "檔案類型" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-313">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-314">描述) **擴充** 屬性所表示之檔案類型 (的描述項。</span><span class="sxs-lookup"><span data-stu-id="ea05f-314">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="ea05f-315">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-315">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-316">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea05f-316">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-319">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 檔案系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="ea05f-319">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-320">檔案系統的類別。</span><span class="sxs-lookup"><span data-stu-id="ea05f-320">Class of the file system.</span></span>

<span data-ttu-id="ea05f-321">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-321">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-322">**FSName**</span><span class="sxs-lookup"><span data-stu-id="ea05f-322">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-323">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-325">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" File System Name ") </span><span class="sxs-lookup"><span data-stu-id="ea05f-325">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-326">檔案系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea05f-326">Name of the file system.</span></span>

<span data-ttu-id="ea05f-327">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-328">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="ea05f-328">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-329">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ea05f-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-331">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「隱藏」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-332">若 **為 True**，則表示檔案已隱藏。</span><span class="sxs-lookup"><span data-stu-id="ea05f-332">If **True**, the file is hidden.</span></span>

<span data-ttu-id="ea05f-333">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-333">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ea05f-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-335">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ea05f-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-337">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="ea05f-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-338">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ea05f-338">Date and time when the object was installed.</span></span> <span data-ttu-id="ea05f-339">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="ea05f-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ea05f-340">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-341">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="ea05f-341">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-342">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ea05f-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-344">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「目前的檔案開啟計數」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-344">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-345">檔案目前作用中的「檔案開啟」數目。</span><span class="sxs-lookup"><span data-stu-id="ea05f-345">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="ea05f-346">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-346">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ea05f-347">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-348">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="ea05f-348">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-349">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ea05f-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-351">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次存取」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-352">上次存取檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ea05f-352">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="ea05f-353">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-354">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="ea05f-354">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-355">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ea05f-355">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-357">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次修改」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-357">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-358">上次修改檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ea05f-358">Date and time that the file was last modified.</span></span>

<span data-ttu-id="ea05f-359">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-359">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-360">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ea05f-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-363">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ea05f-363">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-364">作為檔案系統內邏輯檔案實例之索引鍵的繼承名稱 (提供完整路徑名稱) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-364">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="ea05f-365">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ea05f-366">範例： "C： \\ Windows \\ system \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="ea05f-366">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-367">**路徑**</span><span class="sxs-lookup"><span data-stu-id="ea05f-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-368">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-370">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Path" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-371">檔案的路徑，包括開頭和尾端反斜線。</span><span class="sxs-lookup"><span data-stu-id="ea05f-371">Path of the file including leading and trailing backslashes.</span></span> <span data-ttu-id="ea05f-372">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-372">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ea05f-373">範例： " \\ windows \\ system \\ "</span><span class="sxs-lookup"><span data-stu-id="ea05f-373">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-374">**讀**</span><span class="sxs-lookup"><span data-stu-id="ea05f-374">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-375">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ea05f-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-377">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可讀取" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-377">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-378">若 **為 True**，則表示可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="ea05f-378">If **True**, the file can be read.</span></span>

<span data-ttu-id="ea05f-379">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-379">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-380">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ea05f-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea05f-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-383">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-384">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="ea05f-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="ea05f-385">您可以定義操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="ea05f-385">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="ea05f-386">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="ea05f-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ea05f-387">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="ea05f-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ea05f-388">Nonoperational 狀態可能包含「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="ea05f-388">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ea05f-389">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="ea05f-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ea05f-390">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="ea05f-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ea05f-391">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ea05f-392">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="ea05f-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ea05f-393">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ea05f-394">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ea05f-395">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ea05f-396">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ea05f-397">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ea05f-398">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ea05f-399">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ea05f-400">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ea05f-401">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ea05f-402">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ea05f-403">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ea05f-404">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ea05f-405">**系統**</span><span class="sxs-lookup"><span data-stu-id="ea05f-405">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-406">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ea05f-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-408">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "System File" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-408">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-409">若 **為 True**，表示檔案為系統檔案。</span><span class="sxs-lookup"><span data-stu-id="ea05f-409">If **True**, the file is a system file.</span></span>

<span data-ttu-id="ea05f-410">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea05f-411">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="ea05f-411">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea05f-412">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ea05f-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea05f-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea05f-414">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可寫入" ) </span><span class="sxs-lookup"><span data-stu-id="ea05f-414">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="ea05f-415">若 **為 True**，則表示可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="ea05f-415">If **True**, the file can be written.</span></span>

<span data-ttu-id="ea05f-416">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-416">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea05f-417">備註</span><span class="sxs-lookup"><span data-stu-id="ea05f-417">Remarks</span></span>

<span data-ttu-id="ea05f-418">**Cim \_ DeviceFile** 類別衍生自 [**cim \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="ea05f-418">The **CIM\_DeviceFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ea05f-419">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="ea05f-419">WMI does not implement this class.</span></span>

<span data-ttu-id="ea05f-420">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="ea05f-420">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ea05f-421">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ea05f-421">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea05f-422">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea05f-422">Requirements</span></span>



| <span data-ttu-id="ea05f-423">需求</span><span class="sxs-lookup"><span data-stu-id="ea05f-423">Requirement</span></span> | <span data-ttu-id="ea05f-424">值</span><span class="sxs-lookup"><span data-stu-id="ea05f-424">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea05f-425">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea05f-425">Minimum supported client</span></span><br/> | <span data-ttu-id="ea05f-426">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea05f-426">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea05f-427">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea05f-427">Minimum supported server</span></span><br/> | <span data-ttu-id="ea05f-428">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea05f-428">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea05f-429">命名空間</span><span class="sxs-lookup"><span data-stu-id="ea05f-429">Namespace</span></span><br/>                | <span data-ttu-id="ea05f-430">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ea05f-430">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ea05f-431">MOF</span><span class="sxs-lookup"><span data-stu-id="ea05f-431">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea05f-432"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea05f-432"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea05f-433">DLL</span><span class="sxs-lookup"><span data-stu-id="ea05f-433">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea05f-434"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea05f-434"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea05f-435">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea05f-435">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea05f-436">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="ea05f-436">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

