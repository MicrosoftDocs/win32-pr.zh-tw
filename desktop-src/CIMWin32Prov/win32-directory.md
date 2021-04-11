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
# <a name="win32_directory-class"></a>Win32 \_ 目錄類別

**Win32 \_ 目錄** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 的電腦系統上的目錄專案。 目錄是一種以邏輯方式將資料檔案分組，並提供群組檔案之路徑資訊的檔案類型。 範例： C： \\ TEMP。 **Win32 \_目錄** 不包含網路磁碟機機的目錄。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

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

## <a name="members"></a>成員

**Win32 \_ 目錄** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ 目錄** 類別具有這些方法。



| 方法                                                                                             | 描述                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md)     | 類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。<br/>                                                                                                                        |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-directory.md) | 類別方法，這個方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。<br/>                                                                                                                        |
| [**壓縮**](compress-method-in-class-win32-directory.md)                                       | 類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。<br/>                                                                                                                                   |
| [**CompressEx**](compressex-method-in-class-win32-directory.md)                                   | 類別方法，會將邏輯檔案壓縮 (或物件路徑中指定的目錄) 。<br/>                                                                                                                                   |
| [**複製**](copy-method-in-class-win32-directory.md)                                               | 類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到輸入參數所指定的位置。<br/>                                                                                        |
| [**CopyEx**](copyex-method-in-class-win32-directory.md)                                           | 類別方法，會將物件路徑中指定的邏輯檔案或目錄複寫到 *FileName* 參數所指定的位置。<br/>                                                                                   |
| [**刪除**](delete-method-in-class-win32-directory.md)                                           | 類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。<br/>                                                                                                                                      |
| [**DeleteEx**](deleteex-method-in-class-win32-directory.md)                                       | 類別方法，會刪除物件路徑中指定的邏輯檔案 (或目錄) 。<br/>                                                                                                                                      |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-directory.md)           | 類別方法，這個方法會判斷呼叫端是否有 *許可權* 引數所指定的匯總許可權，不只是在檔案物件上，而是在共用上的檔案或目錄位於共用) 的 (。<br/> |
| [**重新命名**](rename-method-in-class-win32-directory.md)                                           | 類別方法，會將物件路徑中指定的邏輯檔案 (或目錄) 重新命名。<br/>                                                                                                                                      |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md)                             | 取得物件路徑中所指定之邏輯檔案擁有權的類別方法。<br/>                                                                                                                                        |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-directory.md)                         | 取得物件路徑中所指定之邏輯檔案擁有權的類別方法。<br/>                                                                                                                                        |
| [**解壓**](uncompress-method-in-class-win32-directory.md)                                   | Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。<br/>                                                                                                                                 |
| [**UncompressEx**](uncompressex-method-in-class-win32-directory.md)                               | Uncompresses 邏輯檔案的類別方法， (或在物件路徑中指定的目錄) 。<br/>                                                                                                                                 |



 

### <a name="properties"></a>屬性

**Win32 \_ 目錄** 類別具有這些屬性。

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) 
</dt> </dl>

位元遮罩，表示存取或執行目錄上特定作業所需的存取權限。 如需位值，請參閱檔案 [**和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)。

> [!Note]  
> 在 FAT 磁片區上，會改為傳回 **完整 \_ 存取** 值，表示物件上未設定任何安全性。

 

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 或檔案 \_ 清單 \_ 目錄 (目錄)** (1) 


</dt> <dd>

授與從檔案讀取資料的許可權。 若為目錄，此值會授與許可權來列出目錄的內容。

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 或檔案 \_ 新增檔案 \_ (目錄)** (2) 


</dt> <dd>

授與將資料寫入檔案的許可權。 若為目錄，此值會授與在目錄中建立檔案的許可權。

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**檔案 \_\_將資料附加)  (檔案，或 \_ 將檔案新增 \_ 子目錄** (4) 


</dt> <dd>

授與將資料附加至檔案的許可權。 若為目錄，此值會授與建立子目錄的許可權。

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8) 


</dt> <dd>

授與讀取擴充屬性的許可權。

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_將 \_ EA 寫入** (16) 


</dt> <dd>

授予寫入擴充屬性的許可權。

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**檔案 \_執行 (檔案) 或檔案往返 \_ (目錄)** (32) 


</dt> <dd>

授與許可權來執行檔案。 若為目錄，可以進行目錄的往返。

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64) 


</dt> <dd>

授與刪除目錄的許可權，以及它所包含的所有檔案 (其子) ，即使檔案是唯讀的。

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128) 


</dt> <dd>

授與讀取檔案屬性的許可權。

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256) 


</dt> <dd>

授與變更檔案屬性的許可權。

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**刪除** (65536) 


</dt> <dd>

授與刪除存取權。

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072) 


</dt> <dd>

授與安全描述項和擁有者的讀取權限。

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144) 


</dt> <dd>

授與任意 ACL 的寫入權限。

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288) 


</dt> <dd>

指派寫入擁有者。

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576) 


</dt> <dd>

同步存取，並允許進程等候物件進入已發出信號的狀態。

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**存取 \_SYSTEM \_ SECURITY** (18809343) 


</dt> <dd>

控制取得或設定物件安全描述項中 SACL 的能力。

</dd> </dl>

</dd> <dt>

**封存**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "應該封存" ) 
</dt> </dl>

指出是否已設定資料夾的封存位。 備份程式會使用封存位來識別應該備份的檔案。 若 **為 True**，則表示應該封存檔案。

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

物件的簡短文字描述。

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

指出資料夾是否已壓縮。 WMI 會辨識使用 WMI 本身或使用圖形化使用者介面壓縮的資料夾;但是，它並不會辨識。壓縮的壓縮檔案。 若 **為 True**，則會壓縮檔案。

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

演算法或工具 (通常是) 用來壓縮邏輯檔案的方法。 若無法 (或不需要的) 描述壓縮配置 (可能因為不知道) ，請使用下列文字：「未知」表示不知道邏輯檔案是否已壓縮;「已壓縮」表示壓縮檔案，但其壓縮配置未知或未洩漏;和「未壓縮」表示邏輯檔案未壓縮。

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

第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。

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

檔案系統物件的建立日期。 如需使用 WMI 日期和時間格式的詳細資訊，請參閱 [wmi 工作：日期和時間](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times)。

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

範圍電腦系統的建立類別名稱。

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

儲存檔案系統物件的電腦名稱稱。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
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

限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Drive" ) 
</dt> </dl>

磁片磁碟機的磁碟機號 (包括儲存檔案系統物件的冒號) 。

範例： "c："

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "八點三個檔案名" ) 
</dt> </dl>

資料夾的 MS-DOS 相容名稱。

範例： "c： \\ progra ~ 1"

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**已加密**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Encrypted" ) 
</dt> </dl>

指出資料夾是否已加密。 若 **為 True**，則會加密資料夾。

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

檔案系統物件的副檔名，不包括點 (。 ) ，可將副檔名與檔案名分隔開來。

範例： "txt"、"mof"、"mdb"

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) 
</dt> </dl>

檔案名 (沒有檔案的點或副檔名) 。

範例： "autoexec"

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) 
</dt> </dl>

檔案系統物件的大小（以位元組為單位）。 雖然資料夾具有 **FileSize** 屬性，但一律會傳回值0。 若要判斷資料夾的大小，請使用 FileSystemObject，或新增資料夾中儲存的所有檔案大小。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

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

例如，.mdb 檔案可能會有 Microsoft Access 應用程式的檔案類型。 .Asp 檔可能會有檔案類型的 HTML 檔案。 資料夾通常是以資料夾的形式來報告。

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

檔案系統的類型 (NTFS、FAT、FAT32) 安裝在檔案或資料夾所在的磁片磁碟機上。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「隱藏」 ) 
</dt> </dl>

指出是否隱藏檔案系統物件。 若 **為 True**，則表示檔案已隱藏。

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

指出物件的安裝時間。 缺少值並不表示物件未安裝。

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

上次存取檔案的日期。 如需使用 WMI 日期和時間格式的詳細資訊，請參閱 [wmi 工作：日期和時間](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times)。

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

上次修改檔案的日期。 如需使用 WMI 日期和時間格式的詳細資訊，請參閱 [wmi 工作：日期和時間](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times)。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name 屬性是一個字串，代表繼承的名稱，做為檔案系統內的邏輯檔案實例的索引鍵。 應提供完整路徑名稱。 範例： C： \\ Windows \\ system \\win.ini

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**路徑**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Path" ) 
</dt> </dl>

檔案的路徑。 路徑包括開頭和尾端的反斜線，而不是磁碟機號或資料夾名稱。

針對 c： \\ windows \\ system32 wbem 資料夾 \\ ，路徑為 \\ windows \\ system32 \\ 。 針對資料夾 c： \\ 腳本，路徑為 \\ 。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**讀**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "可讀取" ) 
</dt> </dl>

指出您是否可以讀取資料夾中的專案。 若 **為 True**，則表示可以讀取檔案。

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

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "System File" ) 
</dt> </dl>

指出物件是否為系統檔案。 若 **為 True**，表示檔案是系統檔案

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

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

**Win32 \_ 目錄** 類別衍生自 [**CIM \_ 目錄**](cim-directory.md)。

**概觀**

資料夾是設計來包含其他檔案系統物件的檔案系統物件。 但是，這並不表示所有資料夾都是一樣的。 相反地，資料夾會有相當大的差異。 某些資料夾是操作系統資料夾，通常不應由腳本修改。 某些資料夾是唯讀的，這表示使用者可以存取該資料夾的內容，但無法新增、刪除或修改這些內容。 某些資料夾會針對最佳儲存體進行壓縮，而其他資料夾則會被隱藏，使用者看不到。

WMI 使用 **Win32 \_ 目錄** 類別來管理資料夾。 此類別中提供的屬性和方法明顯與 [**CIM \_ 資料檔案**](cim-datafile.md) 類別中可用的屬性和方法相同，後者是用來管理檔案的類別。 這表示在您學到如何使用 WMI 管理資料夾之後，您將不需要任何額外的工作，也知道如何管理檔案。

[**Win32 \_ 子目錄**](win32-subdirectory.md)關聯類別也用來管理檔案和資料夾。 **Win32 \_ 子目錄** 類別會關聯資料夾及其直屬子資料夾。 例如，在資料夾結構 C： \\ scripts 記錄檔中 \\ ，記錄是腳本的子資料夾，而腳本是根資料夾 C：的子資料夾 \\ 。 不過，記錄不會被視為 C：的子資料夾 \\ 。

您可以使用 **Win32 \_ 目錄** 類別取出檔案系統中任何資料夾的屬性。 使用這個類別的可用屬性會顯示在表11.1 中。 若要抓取單一資料夾的屬性，請將 Windows 查詢語言 (WQL) Query 中的 **Win32 \_ 目錄** 類別，確定您包含資料夾的名稱。 例如，此查詢系結至資料夾 D： \\ Archive：

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

在 WQL 查詢中指定檔案或資料夾名稱時，請確定您使用兩個反斜線 (\\ \\) 來分隔路徑元件。

如果您想要限制單一磁片磁碟機的資料抓取，請包含指定磁碟機號的 Where 子句。 例如，此查詢會傳回磁片磁碟機 C：上所有資料夾的清單。

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

如果您需要列舉電腦上的所有資料夾，請注意此查詢可能需要花費很長的時間才能完成。

## <a name="examples"></a>範例

下列 VBScript 範例會抓取資料夾 C：腳本的屬性 \\ 。


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



下列 VBScript 範例會傳回電腦上所有隱藏資料夾的清單。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
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

[**CIM \_ 目錄**](cim-directory.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

