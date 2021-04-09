---
description: Win32 \_ CodecFile&\# 32;WMI 類別代表安裝在電腦系統上的音訊或影片編解碼器。
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Win32_CodecFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc7a6073ab2841fde4492cd59ae1696aeca9f6a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111233"
---
# <a name="win32_codecfile-class"></a><span data-ttu-id="0b0b3-103">Win32 \_ CodecFile 類別</span><span class="sxs-lookup"><span data-stu-id="0b0b3-103">Win32\_CodecFile class</span></span>

<span data-ttu-id="0b0b3-104">**Win32 \_ CodecFile** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表安裝在電腦系統上的音訊或影片編解碼器。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-104">The **Win32\_CodecFile** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the audio or video codec installed on the computer system.</span></span> <span data-ttu-id="0b0b3-105">編解碼器會將媒體格式類型轉換成另一種類型，通常會將壓縮格式轉換成未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-105">Codecs convert one media format type to another, typically a compressed format to an uncompressed format.</span></span> <span data-ttu-id="0b0b3-106">名稱 "編解碼器" 衍生自壓縮和解壓縮的組合。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-106">The name "codec" is derived from a combination of compress and decompress.</span></span> <span data-ttu-id="0b0b3-107">例如，編解碼器可以將壓縮格式（例如，ADPCM）轉換成未壓縮的格式，例如 PCM，大部分的音訊硬體都可以直接播放。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-107">For example, a codec can convert a compressed format, such as MS-ADPCM, to an uncompressed format such as PCM, which most audio hardware can play directly.</span></span>

<span data-ttu-id="0b0b3-108">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0b0b3-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0b3-110">語法</span><span class="sxs-lookup"><span data-stu-id="0b0b3-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
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
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="0b0b3-111">成員</span><span class="sxs-lookup"><span data-stu-id="0b0b3-111">Members</span></span>

<span data-ttu-id="0b0b3-112">**Win32 \_ CodecFile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0b0b3-112">The **Win32\_CodecFile** class has these types of members:</span></span>

-   [<span data-ttu-id="0b0b3-113">方法</span><span class="sxs-lookup"><span data-stu-id="0b0b3-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="0b0b3-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0b0b3-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0b0b3-115">方法</span><span class="sxs-lookup"><span data-stu-id="0b0b3-115">Methods</span></span>

<span data-ttu-id="0b0b3-116">**Win32 \_ CodecFile** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-116">The **Win32\_CodecFile** class has these methods.</span></span>



| <span data-ttu-id="0b0b3-117">方法</span><span class="sxs-lookup"><span data-stu-id="0b0b3-117">Method</span></span>                                                                                             | <span data-ttu-id="0b0b3-118">描述</span><span class="sxs-lookup"><span data-stu-id="0b0b3-118">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b0b3-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-codecfile.md)     | <span data-ttu-id="0b0b3-120">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-120">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="0b0b3-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | <span data-ttu-id="0b0b3-122">變更物件路徑中指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-122">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="0b0b3-123">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-123">**Compress**</span></span>](compress-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="0b0b3-124">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-124">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="0b0b3-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-125">**CompressEx**</span></span>](compressex-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="0b0b3-126">壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-126">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="0b0b3-127">**複製**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-127">**Copy**</span></span>](copy-method-in-class-win32-codecfile.md)                                               | <span data-ttu-id="0b0b3-128">將物件路徑中指定的邏輯檔案或目錄複寫到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-128">Copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                         |
| [<span data-ttu-id="0b0b3-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-129">**CopyEx**</span></span>](copyex-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="0b0b3-130">類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到 FileName 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-130">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                    |
| [<span data-ttu-id="0b0b3-131">**刪除**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-131">**Delete**</span></span>](delete-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="0b0b3-132">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-132">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="0b0b3-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="0b0b3-134">刪除在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-134">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="0b0b3-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-codecfile.md)           | <span data-ttu-id="0b0b3-136">判斷呼叫端是否有 **許可權** 引數所指定的匯總許可權，不只是在檔案物件上，而是在共用上的檔案或目錄位於共用) 的 (。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-136">Determines whether the caller has the aggregated permissions specified by the **permission** argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="0b0b3-137">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-137">**Rename**</span></span>](rename-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="0b0b3-138">類別方法，會將物件路徑中指定的邏輯檔案 (或目錄) 重新命名。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="0b0b3-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-codecfile.md)                             | <span data-ttu-id="0b0b3-140">取得物件路徑中指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-140">Obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="0b0b3-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-codecfile.md)                         | <span data-ttu-id="0b0b3-142">取得物件路徑中所指定之邏輯檔案擁有權的類別方法。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="0b0b3-143">**解壓**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="0b0b3-144">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-144">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="0b0b3-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-codecfile.md)                               | <span data-ttu-id="0b0b3-146">Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-146">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="0b0b3-147">屬性</span><span class="sxs-lookup"><span data-stu-id="0b0b3-147">Properties</span></span>

<span data-ttu-id="0b0b3-148">**Win32 \_ CodecFile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-148">The **Win32\_CodecFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b0b3-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-152">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-153">代表在編解碼器檔案上存取或執行特定作業所需存取權限的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-153">Bitmask that represents the access rights required to access or perform specific operations on the codec file.</span></span> <span data-ttu-id="0b0b3-154">如需位值，請參閱檔案 [**和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="0b0b3-155">在 FAT 磁片區上，會改為傳回 **完整 \_ 存取** 值，表示物件上未設定任何安全性。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="0b0b3-156">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="0b0b3-157">**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-157">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="0b0b3-158">**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-158">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="0b0b3-159">**檔案 \_\_將資料附加)  (檔案或檔案 \_ 新增 \_ 子目錄 (目錄)** (4) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-159">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="0b0b3-160">**檔案 \_讀取 \_ EA** (8) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-160">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="0b0b3-161">**檔案 \_將 \_ EA 寫入** (16) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-161">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="0b0b3-162">**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-162">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="0b0b3-163">**檔案 \_刪除 \_ 子 (目錄)** (64) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-163">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="0b0b3-164">**檔案 \_讀取 \_ 屬性** (128) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-164">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="0b0b3-165">**檔案 \_將 \_ 屬性寫入** (256) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-165">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="0b0b3-166">**刪除** (65536) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-166">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="0b0b3-167">**讀取 \_控制** (131072) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-167">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="0b0b3-168">**寫入 \_DAC** (262144) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-168">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="0b0b3-169">**寫入 \_擁有** 者 (524288) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-169">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="0b0b3-170">**同步處理** (1048576) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-170">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b0b3-171">**封存**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-171">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-172">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-174">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "應該封存" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-175">若 **為 True**，則表示應該封存檔案。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-175">If **True**, the file should be archived.</span></span>

<span data-ttu-id="0b0b3-176">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-176">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-177">**標題**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-177">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-180">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-181">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-181">Short description of the object.</span></span>

<span data-ttu-id="0b0b3-182">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-183">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-183">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-186">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-187">若 **為 True**，則會壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-187">If **True**, the file is compressed.</span></span>

<span data-ttu-id="0b0b3-188">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-188">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-189">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-189">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-192">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Compression Method" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-192">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-193">用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-193">Algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="0b0b3-194">若無法 (或不需要的) 描述壓縮配置 (可能因為不知道) ，請使用下列文字：「未知」表示不知道邏輯檔案是否已壓縮;「已壓縮」表示壓縮檔案，但其壓縮配置未知或未洩漏;和「未壓縮」表示邏輯檔案未壓縮。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-194">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed or not; "Compressed" to represent that the file is compressed but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="0b0b3-195">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-199">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-199">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-200">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-200">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0b0b3-201">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-201">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0b0b3-202">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-202">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-203">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-203">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-204">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-204">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-206">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建立日期" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-206">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-207">檔案建立日期。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-207">File creation date.</span></span>

<span data-ttu-id="0b0b3-208">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-209">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-209">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-212">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統類別名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-213">電腦系統的類別。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-213">Class of the computer system.</span></span>

<span data-ttu-id="0b0b3-214">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-214">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-215">**CSName**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-215">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-218">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統名稱」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-218">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-219">代表電腦系統名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-219">String representing the name of the computer system.</span></span>

<span data-ttu-id="0b0b3-220">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-221">**說明**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-221">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-224">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (描述) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ MediaResources \\ \\ icm \| Description" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-224">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\icm\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-225">編解碼器驅動程式的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-225">Full name of the codec driver.</span></span> <span data-ttu-id="0b0b3-226">這個字串的目的是要以大量 (描述性) 空間來顯示。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-226">This string is intended to be displayed in large (descriptive) spaces.</span></span>

<span data-ttu-id="0b0b3-227">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0b0b3-228">範例：「Microsoft PCM 轉換器」</span><span class="sxs-lookup"><span data-stu-id="0b0b3-228">Example: "Microsoft PCM Converter"</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-229">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-229">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-232">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Drive" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-232">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-233">磁碟機號 (包括檔案的冒號) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-233">Drive letter (including colon) of the file.</span></span>

<span data-ttu-id="0b0b3-234">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="0b0b3-235">範例： "c："</span><span class="sxs-lookup"><span data-stu-id="0b0b3-235">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-236">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-236">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-239">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "八點三個檔案名" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-240">這個檔案的 DOS 相容檔案名。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-240">DOS-compatible file name for this file.</span></span>

<span data-ttu-id="0b0b3-241">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="0b0b3-242">範例： "c： \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="0b0b3-242">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-243">**已加密**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-243">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-244">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-246">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encrypted" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-247">若 **為 True**，則表示檔案已加密。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-247">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="0b0b3-248">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-248">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-249">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-249">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-252">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encryption Method" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-252">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-253">用來加密邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-253">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="0b0b3-254">如果 (或不需要的) 描述加密配置 (可能基於安全性理由) ，請使用下列文字：「未知」表示不知道邏輯檔案是否已加密;「已加密」表示檔案已加密，但其加密配置不知道或未洩漏;和「未加密」表示邏輯檔案未加密。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-254">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted or not; "Encrypted" to represent that the file is encrypted but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="0b0b3-255">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-256">**分機**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-259">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Extension" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-259">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-260">副檔名 (沒有點) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-260">File name extension (without the dot).</span></span>

<span data-ttu-id="0b0b3-261">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-261">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="0b0b3-262">範例： "txt"、"mof"、"mdb"</span><span class="sxs-lookup"><span data-stu-id="0b0b3-262">Examples: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-266">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-266">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-267">不含副檔名) 的 (名稱。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-267">Name (without the extension) of the file.</span></span>

<span data-ttu-id="0b0b3-268">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-268">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="0b0b3-269">範例： "autoexec"</span><span class="sxs-lookup"><span data-stu-id="0b0b3-269">Example: "autoexec"</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-271">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-273">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-274">檔案大小 (以位元組為單位) 。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-274">Size of the file (in bytes).</span></span>

<span data-ttu-id="0b0b3-275">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="0b0b3-276">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-276">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-280">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "檔案類型" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-281">**延伸** 模組屬性) 指定的檔案類型 (。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-281">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="0b0b3-282">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-283">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-283">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-286">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 檔案系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="0b0b3-286">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-287">檔案系統的類別。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-287">Class of the file system.</span></span>

<span data-ttu-id="0b0b3-288">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-289">**FSName**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-289">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-290">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-292">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" File System Name ") </span><span class="sxs-lookup"><span data-stu-id="0b0b3-292">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-293">檔案系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-293">Name of the file system.</span></span>

<span data-ttu-id="0b0b3-294">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-295">**群組**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-295">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-296">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-298">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion driver \\ \\ . desc" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-298">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\drivers.desc")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-299">此類別所代表的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-299">Codec represented by this class.</span></span>

<span data-ttu-id="0b0b3-300">值如下：</span><span class="sxs-lookup"><span data-stu-id="0b0b3-300">The values are:</span></span>

<dl> <dd><span data-ttu-id="0b0b3-301">視聽</span><span class="sxs-lookup"><span data-stu-id="0b0b3-301">"Audio"</span></span></dd> <dd><span data-ttu-id="0b0b3-302">攝像機</span><span class="sxs-lookup"><span data-stu-id="0b0b3-302">"Video"</span></span></dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

<span data-ttu-id="0b0b3-303">**音訊** ( "音訊" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-303">**Audio** ("Audio")</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="0b0b3-304">**影片** ( 「影片」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-304">**Video** ("Video")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b0b3-305">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-305">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-306">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-306">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-308">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「隱藏」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-308">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-309">若 **為 True**，則表示檔案已隱藏。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-309">If **True**, the file is hidden.</span></span>

<span data-ttu-id="0b0b3-310">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-312">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-314">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0b0b3-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-315">已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-315">Object was installed.</span></span> <span data-ttu-id="0b0b3-316">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-316">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0b0b3-317">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-318">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-318">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-319">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-321">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「目前的檔案開啟計數」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-321">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-322">檔案目前作用中的「檔案開啟」數目。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-322">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="0b0b3-323">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="0b0b3-324">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-324">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-325">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-325">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-326">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-328">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次存取」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-329">上次存取檔案的時間。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-329">File was last accessed.</span></span>

<span data-ttu-id="0b0b3-330">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-331">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-331">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-332">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-334">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次修改」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-335">上次修改檔案的時間。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-335">File was last modified.</span></span>

<span data-ttu-id="0b0b3-336">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-337">**製造商**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-337">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-340">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "製造商" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-340">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-341">版本資源中的製造商字串（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-341">Manufacturer string from version resource, if one is present.</span></span>

<span data-ttu-id="0b0b3-342">這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-342">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-343">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-344">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-346">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b0b3-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-347">作為檔案系統內邏輯檔案實例之索引鍵的繼承名稱。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-347">Inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="0b0b3-348">應提供完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-348">Full path names should be provided.</span></span>

<span data-ttu-id="0b0b3-349">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0b0b3-350">範例： "C： \\ Windows \\ system \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="0b0b3-350">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-351">**路徑**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-351">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-354">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Path" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-354">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-355">檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-355">Path of the file.</span></span> <span data-ttu-id="0b0b3-356">這包括開頭和尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-356">This includes leading and trailing backslashes.</span></span>

<span data-ttu-id="0b0b3-357">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-357">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="0b0b3-358">範例： " \\ windows \\ system \\ "</span><span class="sxs-lookup"><span data-stu-id="0b0b3-358">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-359">**讀**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-359">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-360">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-362">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可讀取" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-363">可以讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-363">File can be read.</span></span>

<span data-ttu-id="0b0b3-364">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-364">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-365">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-366">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-368">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-369">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-369">Current status of the object.</span></span> <span data-ttu-id="0b0b3-370">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0b0b3-371">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0b0b3-372">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0b0b3-373">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0b0b3-374">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0b0b3-375">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0b0b3-376">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0b0b3-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0b0b3-377">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0b0b3-378">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0b0b3-379">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b0b3-380">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0b0b3-381">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0b0b3-382">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0b0b3-383">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0b0b3-384">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0b0b3-385">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0b0b3-386">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0b0b3-387">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0b0b3-388">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b0b3-389">**系統**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-390">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-392">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "System File" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-392">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-393">若 **為 True**，表示檔案為系統檔案。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="0b0b3-394">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-395">**版本**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-396">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-398">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Version" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-398">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-399">版本資源中的版本字串（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-399">Version string from version resource, if one is present.</span></span>

<span data-ttu-id="0b0b3-400">這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0b3-401">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0b3-402">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b0b3-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0b3-404">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可寫入" ) </span><span class="sxs-lookup"><span data-stu-id="0b0b3-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="0b0b3-405">若 **為 True**，則表示可以寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="0b0b3-406">這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b0b3-407">備註</span><span class="sxs-lookup"><span data-stu-id="0b0b3-407">Remarks</span></span>

<span data-ttu-id="0b0b3-408">**Win32 \_ CodecFile** 類別衍生自 [**CIM \_ 資料檔案**](cim-datafile.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0b3-408">The **Win32\_CodecFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b0b3-409">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b0b3-409">Requirements</span></span>



| <span data-ttu-id="0b0b3-410">需求</span><span class="sxs-lookup"><span data-stu-id="0b0b3-410">Requirement</span></span> | <span data-ttu-id="0b0b3-411">值</span><span class="sxs-lookup"><span data-stu-id="0b0b3-411">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0b3-412">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b0b3-412">Minimum supported client</span></span><br/> | <span data-ttu-id="0b0b3-413">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b0b3-413">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b0b3-414">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b0b3-414">Minimum supported server</span></span><br/> | <span data-ttu-id="0b0b3-415">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b0b3-415">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b0b3-416">命名空間</span><span class="sxs-lookup"><span data-stu-id="0b0b3-416">Namespace</span></span><br/>                | <span data-ttu-id="0b0b3-417">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0b0b3-417">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b0b3-418">MOF</span><span class="sxs-lookup"><span data-stu-id="0b0b3-418">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b0b3-419"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b0b3-419"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b0b3-420">DLL</span><span class="sxs-lookup"><span data-stu-id="0b0b3-420">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b0b3-421"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b0b3-421"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b0b3-422">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b0b3-422">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0b3-423">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="0b0b3-423">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

<span data-ttu-id="0b0b3-424">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b0b3-424">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

