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
# <a name="win32_pagefile-class"></a>Win32 \_ 分頁檔類別

**Win32 \_ 頁面** 檔 [WMI 類別](../wmisdk/retrieving-a-class.md)代表用來處理在 Win32 系統上交換虛擬記憶體檔案的檔案。 這個類別已被取代。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

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

## <a name="members"></a>成員

**Win32 \_ 分頁檔** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ 分頁檔** 類別有這些方法。



| 方法                                                                                            | 描述                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-pagefile.md)     | 類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。<br/>                                                                                                                       |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | 類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。<br/>                                                                                                                       |
| [**壓縮**](compress-method-in-class-win32-pagefile.md)                                       | 類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。<br/>                                                                                                                                  |
| [**CompressEx**](compressex-method-in-class-win32-pagefile.md)                                   | 類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。<br/>                                                                                                                                  |
| [**複製**](copy-method-in-class-win32-pagefile.md)                                               | 類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到輸入參數所指定的位置。<br/>                                                                                       |
| [**CopyEx**](copyex-method-in-class-win32-pagefile.md)                                           | 類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到 FileName 參數所指定的位置。<br/>                                                                                    |
| [**刪除**](delete-method-in-class-win32-pagefile.md)                                           | 類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。<br/>                                                                                                                                     |
| [**DeleteEx**](deleteex-method-in-class-win32-pagefile.md)                                       | 類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。<br/>                                                                                                                                     |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-pagefile.md)           | 類別方法，這個方法會判斷呼叫端是否有 *許可權* 引數所指定的匯總許可權，不只是在檔案物件上，而是在共用上的檔案或目錄位於共用) 的 (。<br/> |
| [**重新命名**](rename-method-in-class-win32-pagefile.md)                                           | 類別方法，會將物件路徑中指定的邏輯檔案 (或目錄) 重新命名。<br/>                                                                                                                                     |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-pagefile.md)                             | 取得物件路徑中所指定之邏輯檔案擁有權的類別方法。<br/>                                                                                                                                       |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-pagefile.md)                         | 取得物件路徑中所指定之邏輯檔案擁有權的類別方法。<br/>                                                                                                                                       |
| [**解壓**](uncompress-method-in-class-win32-pagefile.md)                                   | Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。<br/>                                                                                                                                |
| [**UncompressEx**](uncompressex-method-in-class-win32-pagefile.md)                               | Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。<br/>                                                                                                                                |



 

### <a name="properties"></a>屬性

**Win32 \_ 分頁檔** 類別具有這些屬性。

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "存取權限" ) 
</dt> </dl>

位元遮罩，表示存取或執行檔案上特定作業所需的存取權限。 如需值，請參閱檔案 [**和目錄存取權限常數**](../wmisdk/file-and-directory-access-rights-constants.md)。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) 


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) 


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**檔案 \_\_將資料附加)  (檔案或檔案 \_ 新增 \_ 子目錄 (目錄)** (4) 


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**檔案 \_讀取 \_ EA** (8) 


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**檔案 \_將 \_ EA 寫入** (16) 


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) 


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**檔案 \_刪除 \_ 子 (目錄)** (64) 


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**檔案 \_讀取 \_ 屬性** (128) 


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**檔案 \_將 \_ 屬性寫入** (256) 


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**刪除** (65536) 


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**讀取 \_控制** (131072) 


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**寫入 \_DAC** (262144) 


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**寫入 \_擁有** 者 (524288) 


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**同步處理** (1048576) 


</dt> <dd></dd> </dl>

</dd> <dt>

**封存**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "應該封存" ) 
</dt> </dl>

若 **為 True**，則表示應該封存檔案。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( 「Win32」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「壓縮」 ) 
</dt> </dl>

若 **為 True**，則會壓縮檔案。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Compression Method" ) 
</dt> </dl>

自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。 如果壓縮配置未知或未描述，請使用「未知」。 如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。 如果邏輯檔案未壓縮，請使用「未壓縮」。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) 
</dt> </dl>

類別的名稱。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "建立日期" ) 
</dt> </dl>

建立檔案的日期和時間。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「電腦系統類別名稱」 ) 
</dt> </dl>

電腦系統的類別。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「電腦系統名稱」 ) 
</dt> </dl>

電腦系統的名稱。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**磁碟機**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Drive" ) 
</dt> </dl>

磁碟機號 (包括在檔案的磁碟機號) 後面的冒號。 這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

範例： "c："

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "八點三個檔案名" ) 
</dt> </dl>

DOS 相容的檔案名。

範例： "c： \\ progra ~ 1"

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**已加密**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Encrypted" ) 
</dt> </dl>

若 **為 True**，則表示檔案已加密。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Encryption Method" ) 
</dt> </dl>

識別用來加密邏輯檔案之演算法或工具的自由格式字串。 如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。 如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。 如果邏輯檔案未加密，請使用「未加密」。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**分機**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Extension" ) 
</dt> </dl>

沒有前一個期間的副檔名 (點) 。

範例： "txt"、"mof"、"mdb"

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Name" ) 
</dt> </dl>

不含副檔名的檔案名。 範例： "MyDataFile"

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Size" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) 
</dt> </dl>

檔案的大小（以位元組為單位）。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "檔案類型" ) 
</dt> </dl>

表示 **擴充** 屬性所表示之檔案類型的描述元。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**FreeSpace**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Memory Management 結構 \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) 
</dt> </dl>

分頁檔案中的可用空間。 作業系統可以視需要擴大分頁檔，最多可達使用者所加諸的限制。 這個屬性會顯示目前認可的記憶體大小與目前頁面檔案大小之間的差異;它不會顯示分頁檔案的最大可能大小。

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 檔案系統類別名稱 ") 
</dt> </dl>

檔案系統的類別。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) (" File System Name ") 
</dt> </dl>

檔案系統的名稱。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( 「Win32」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「隱藏」 ) 
</dt> </dl>

若 **為 True**，則表示檔案已隱藏。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**InitialSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) 
</dt> </dl>

分頁檔案的初始大小。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「目前的檔案開啟計數」 ) 
</dt> </dl>

檔案目前作用中的「檔案開啟」數目。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「上次存取」 ) 
</dt> </dl>

上次存取檔案的日期和時間。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「上次修改」 ) 
</dt> </dl>

上次修改檔案的日期和時間。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "製造商" ) 
</dt> </dl>

版本資源 (的製造商字串（如果有的話) ）。

這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。

</dd> <dt>

**MaximumSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Memory Management 結構 \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) 
</dt> </dl>

使用者所設定之分頁檔的大小上限。 作業系統將不會允許分頁檔超過此限制。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)，覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Name" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemPageFileInformation \| PageFileName" ) 
</dt> </dl>

分頁檔案的名稱。

範例： "C： \\PAGEFILE.SYS"

</dd> <dt>

**路徑**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**Schema**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Path" ) 
</dt> </dl>

檔案的路徑，包括開頭和尾端的反斜線。

範例： " \\ windows \\ system \\ "

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**讀**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "可讀取" ) 
</dt> </dl>

若 **為 True**，則表示可以讀取檔案。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

表示物件目前狀態的字串。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**系統**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "System File" ) 
</dt> </dl>

若 **為 True**，表示檔案為系統檔案。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Version" ) 
</dt> </dl>

版本資源 (的版本字串（如果有的話）) 。

這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。

</dd> <dt>

**可寫入**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "可寫入" ) 
</dt> </dl>

若 **為 True**，則表示可以寫入檔案。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ 分頁檔** 類別衍生自 [**CIM \_ 目錄**](cim-directory.md)。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例示範如何從 **Win32 \_ 頁面** 檔的實例中取出分頁檔統計資料。


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



下列 Perl 程式碼範例示範如何從 **Win32 \_ 頁面** 檔的實例中取出分頁檔統計資料。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 資料檔案**](cim-datafile.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
