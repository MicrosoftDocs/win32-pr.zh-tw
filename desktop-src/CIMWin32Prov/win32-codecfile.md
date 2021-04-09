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
# <a name="win32_codecfile-class"></a>Win32 \_ CodecFile 類別

**Win32 \_ CodecFile** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表安裝在電腦系統上的音訊或影片編解碼器。 編解碼器會將媒體格式類型轉換成另一種類型，通常會將壓縮格式轉換成未壓縮的格式。 名稱 "編解碼器" 衍生自壓縮和解壓縮的組合。 例如，編解碼器可以將壓縮格式（例如，ADPCM）轉換成未壓縮的格式，例如 PCM，大部分的音訊硬體都可以直接播放。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

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

## <a name="members"></a>成員

**Win32 \_ CodecFile** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ CodecFile** 類別具有這些方法。



| 方法                                                                                             | 描述                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-codecfile.md)     | 變更物件路徑中指定之邏輯檔案的安全性許可權。<br/>                                                                                                                         |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | 變更物件路徑中指定之邏輯檔案的安全性許可權。<br/>                                                                                                                         |
| [**壓縮**](compress-method-in-class-win32-codecfile.md)                                       | 壓縮物件路徑中指定的邏輯檔案 (或目錄) 。<br/>                                                                                                                                    |
| [**CompressEx**](compressex-method-in-class-win32-codecfile.md)                                   | 壓縮物件路徑中指定的邏輯檔案 (或目錄) 。<br/>                                                                                                                                    |
| [**複製**](copy-method-in-class-win32-codecfile.md)                                               | 將物件路徑中指定的邏輯檔案或目錄複寫到輸入參數所指定的位置。<br/>                                                                                         |
| [**CopyEx**](copyex-method-in-class-win32-codecfile.md)                                           | 類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到 FileName 參數所指定的位置。<br/>                                                                    |
| [**刪除**](delete-method-in-class-win32-codecfile.md)                                           | 刪除在物件路徑中指定的邏輯檔案 (或目錄) 。<br/>                                                                                                                                       |
| [**DeleteEx**](deleteex-method-in-class-win32-codecfile.md)                                       | 刪除在物件路徑中指定的邏輯檔案 (或目錄) 。<br/>                                                                                                                                       |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-codecfile.md)           | 判斷呼叫端是否有 **許可權** 引數所指定的匯總許可權，不只是在檔案物件上，而是在共用上的檔案或目錄位於共用) 的 (。<br/> |
| [**重新命名**](rename-method-in-class-win32-codecfile.md)                                           | 類別方法，會將物件路徑中指定的邏輯檔案 (或目錄) 重新命名。<br/>                                                                                                                     |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-codecfile.md)                             | 取得物件路徑中指定之邏輯檔案的擁有權。<br/>                                                                                                                                         |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-codecfile.md)                         | 取得物件路徑中所指定之邏輯檔案擁有權的類別方法。<br/>                                                                                                                       |
| [**解壓**](uncompress-method-in-class-win32-codecfile.md)                                   | Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。<br/>                                                                                                                                  |
| [**UncompressEx**](uncompressex-method-in-class-win32-codecfile.md)                               | Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。<br/>                                                                                                                                  |



 

### <a name="properties"></a>屬性

**Win32 \_ CodecFile** 類別具有這些屬性。

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) 
</dt> </dl>

代表在編解碼器檔案上存取或執行特定作業所需存取權限的位元遮罩。 如需位值，請參閱檔案 [**和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)。

> [!Note]  
> 在 FAT 磁片區上，會改為傳回 **完整 \_ 存取** 值，表示物件上未設定任何安全性。

 

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

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "應該封存" ) 
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

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

物件的簡短描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「壓縮」 ) 
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

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Compression Method" ) 
</dt> </dl>

用來壓縮邏輯檔案的演算法或工具。 若無法 (或不需要的) 描述壓縮配置 (可能因為不知道) ，請使用下列文字：「未知」表示不知道邏輯檔案是否已壓縮;「已壓縮」表示壓縮檔案，但其壓縮配置未知或未洩漏;和「未壓縮」表示邏輯檔案未壓縮。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) 
</dt> </dl>

第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建立日期" ) 
</dt> </dl>

檔案建立日期。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統類別名稱」 ) 
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

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CSName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「電腦系統名稱」 ) 
</dt> </dl>

代表電腦系統名稱的字串。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (描述) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ MediaResources \\ \\ icm \| Description" ) 
</dt> </dl>

編解碼器驅動程式的完整名稱。 這個字串的目的是要以大量 (描述性) 空間來顯示。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

範例：「Microsoft PCM 轉換器」

</dd> <dt>

**磁碟機**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Drive" ) 
</dt> </dl>

磁碟機號 (包括檔案的冒號) 。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

範例： "c："

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "八點三個檔案名" ) 
</dt> </dl>

這個檔案的 DOS 相容檔案名。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

範例： "c： \\ progra ~ 1"

</dd> <dt>

**已加密**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encrypted" ) 
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

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encryption Method" ) 
</dt> </dl>

用來加密邏輯檔案的演算法或工具。 如果 (或不需要的) 描述加密配置 (可能基於安全性理由) ，請使用下列文字：「未知」表示不知道邏輯檔案是否已加密;「已加密」表示檔案已加密，但其加密配置不知道或未洩漏;和「未加密」表示邏輯檔案未加密。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**分機**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Extension" ) 
</dt> </dl>

副檔名 (沒有點) 。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

範例： "txt"、"mof"、"mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) 
</dt> </dl>

不含副檔名) 的 (名稱。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

範例： "autoexec"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) 
</dt> </dl>

檔案大小 (以位元組為單位) 。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "檔案類型" ) 
</dt> </dl>

**延伸** 模組屬性) 指定的檔案類型 (。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 檔案系統類別名稱 ") 
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

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 的 [**CIM \_ 檔案系統**](cim-filesystem.md)。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" File System Name ") 
</dt> </dl>

檔案系統的名稱。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**群組**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion driver \\ \\ . desc" ) 
</dt> </dl>

此類別所代表的編解碼器。

值如下：

<dl> <dd>視聽</dd> <dd>攝像機</dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

**音訊** ( "音訊" ) 


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**影片** ( 「影片」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「隱藏」 ) 
</dt> </dl>

若 **為 True**，則表示檔案已隱藏。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

已安裝物件。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「目前的檔案開啟計數」 ) 
</dt> </dl>

檔案目前作用中的「檔案開啟」數目。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次存取」 ) 
</dt> </dl>

上次存取檔案的時間。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次修改」 ) 
</dt> </dl>

上次修改檔案的時間。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "製造商" ) 
</dt> </dl>

版本資源中的製造商字串（如果有的話）。

這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

作為檔案系統內邏輯檔案實例之索引鍵的繼承名稱。 應提供完整路徑名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

範例： "C： \\ Windows \\ system \\win.ini"

</dd> <dt>

**路徑**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Path" ) 
</dt> </dl>

檔案的路徑。 這包括開頭和尾端的反斜線。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

範例： " \\ windows \\ system \\ "

</dd> <dt>

**讀**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可讀取" ) 
</dt> </dl>

可以讀取檔案。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

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

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "System File" ) 
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

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Version" ) 
</dt> </dl>

版本資源中的版本字串（如果有的話）。

這個屬性繼承自 [**CIM \_ 資料檔案**](cim-datafile.md)。

</dd> <dt>

**可寫入**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可寫入" ) 
</dt> </dl>

若 **為 True**，則表示可以寫入檔案。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ CodecFile** 類別衍生自 [**CIM \_ 資料檔案**](cim-datafile.md)。

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

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

