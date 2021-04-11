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
# <a name="cim_datafile-class"></a>CIM \_ 資料檔案類別

**CIM 資料 \_ 檔** 類別代表資料的命名集合或可執行檔程式碼。 只會傳回本機固定磁片上的檔案實例。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

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

## <a name="members"></a>成員

**CIM \_ 資料檔案** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ 資料檔案** 類別有這些方法。



| 方法                                                                                          | 描述                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md)     | 變更物件路徑中指定之邏輯檔案的安全性許可權。 由 WMI 所執行。<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-datafile.md) | 變更物件路徑中指定之邏輯檔案的安全性許可權。 由 WMI 所執行。<br/>                                   |
| [**壓縮**](compress-method-in-class-cim-datafile.md)                                       | 使用 NTFS 壓縮來壓縮物件路徑中指定的邏輯檔案 (或目錄) 。 由 WMI 所執行。<br/>                       |
| [**CompressEx**](compressex-method-in-class-cim-datafile.md)                                   | 壓縮物件路徑中指定的邏輯檔案 (或目錄) 。 由 WMI 所執行。<br/>                                              |
| [**複製**](copy-method-in-class-cim-datafile.md)                                               | 將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。 由 WMI 所執行。<br/> |
| [**CopyEx**](copyex-method-in-class-cim-datafile.md)                                           | 將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。 由 WMI 所執行。<br/> |
| [**刪除**](delete-method-in-class-cim-datafile.md)                                           | 刪除在物件路徑中指定的邏輯檔案 (或目錄) 。 由 WMI 所執行。<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-datafile.md)                                       | 刪除在物件路徑中指定的邏輯檔案 (或目錄) 。 由 WMI 所執行。<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-datafile.md)           | 判斷呼叫端是否具有 **許可權** 引數所指定的匯總許可權。 由 WMI 所執行。<br/>                |
| [**重新命名**](rename-method-in-class-cim-datafile.md)                                           | 重新命名在物件路徑中指定的邏輯檔案 (或目錄) 。 由 WMI 所執行。<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md)                             | 取得物件路徑中指定之邏輯檔案的擁有權。 由 WMI 所執行。<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-datafile.md)                         | 取得物件路徑中指定之邏輯檔案的擁有權。 由 WMI 所執行。<br/>                                                   |
| [**解壓**](uncompress-method-in-class-cim-datafile.md)                                   | Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。 由 WMI 所執行。<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-datafile.md)                               | Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。 由 WMI 所執行。<br/>                                            |



 

### <a name="properties"></a>屬性

**CIM \_ 資料檔案** 類別具有這些屬性。

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "存取權限" ) 
</dt> </dl>

位元遮罩，表示存取或執行檔案上特定作業所需的存取權限。 如需位值，請參閱檔案 [**和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)。

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

自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。 如果壓縮配置未知或未描述，請使用「未知」。 如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。 如果邏輯檔案未壓縮，請使用「未壓縮」。

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

類別的名稱。

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

建立檔案的日期和時間。

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

電腦系統的名稱。

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

磁碟機號 (包括在檔案的磁碟機號) 後面的冒號。

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

識別用來加密邏輯檔案之演算法或工具的自由格式字串。 如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。 如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。 如果邏輯檔案未加密，請使用「未加密」。

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

限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Name" ) 
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

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Size" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) 
</dt> </dl>

檔案的大小（以位元組為單位）。

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

表示 **擴充** 屬性所表示之檔案類型的描述元。

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

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

這個屬性繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次存取」 ) 
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

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「上次修改」 ) 
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

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "製造商" ) 
</dt> </dl>

版本資源 (的製造商字串（如果有的話) ）。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name 屬性是一個字串，代表繼承的名稱，做為檔案系統內的邏輯檔案實例的索引鍵。 應提供完整路徑名稱。

範例： C： \\ Windows \\ system \\win.ini

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

檔案的路徑，包括開頭和尾端的反斜線。 範例： " \\ windows \\ system \\ "

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

若 **為 True**，則表示可以讀取檔案。

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

表示物件目前狀態的字串。 您可以定義操作和非運作狀態。 操作狀態可以包含「確定」、「降級」和「Pred 失敗」。 「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。

非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。 「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

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

版本資源 (的版本字串（如果有的話）) 。

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

**Cim \_ 資料檔案** 類別衍生自 [**cim \_ LogicalFile**](cim-logicalfile.md)。

WMI 會實行 **CIM \_ 資料檔案** 類別及其所有方法。 **CIM \_ 資料檔案** 類別是動態類別。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

基於安全性考慮，WMI 不直接支援呼叫遠端電腦，並指示它將檔案複製到本身。 不過，您可以使用相關的程式設計語言來呼叫 FTP 或 RoboCopy。

## <a name="examples"></a>範例

下列腳本中心程式 [代碼範例](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) 會使用 **CIM \_ 資料檔案** 類別作為較大應用程式的一部分，以使用 Powershell 來產生 exchange 環境報告。

TechNet 元件庫中的 [Find files WITH WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) 程式碼範例會使用 **CIM \_ 資料檔案** 來搜尋多部電腦上的一個或多個檔案。

下列 VBS 程式碼範例說明如何在資料檔案上執行標準萬用字元搜尋。 請注意，反斜線分隔符號必須以另一個反斜線 () 來進行轉義 \\ \\ 。 此外，使用「**CIM \_ 資料檔案**」時。**FileName**"WHERE 子句中的 WMIPRVSE 進程會掃描任何可用儲存裝置上的所有目錄。 這可能需要一些時間，特別是如果您已對應遠端共用，而且可能會觸發防毒軟體警告。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



下列程式碼片段會將搜尋範圍限制為特定磁片磁碟機、路徑和副檔名。


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



下列 PowerShell 程式碼範例會捕獲單一屬性值。


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
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

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dt>

[WMI 工作：檔案和資料夾](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**檔案和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

