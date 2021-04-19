---
description: 代表檔案或目錄（例如 Win32 \_ CodecFile 或 CIM 資料檔案）的 WMI 類別 \_ 包含 AccessMask 屬性。
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: '檔案和目錄存取權限常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999105"
---
# <a name="file-and-directory-access-rights-constants"></a>檔案和目錄存取權限常數

代表檔案或目錄（例如 [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) 或 [**CIM \_ 資料**](/windows/desktop/CIMWin32Prov/cim-datafile)檔）的 WMI 類別包含 **AccessMask** 屬性。 這個屬性包含的位設定會指定使用者或群組對於檔案的特定存取或作業必須擁有的存取權限。 如需詳細資訊，請參閱檔案 [安全性和存取權限](/windows/desktop/FileIO/file-security-and-access-rights) ，以及 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

包含 **AccessMask** 屬性的檔案或目錄類別包括：

-   [**CIM \_ 資料檔案**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**CIM \_ 目錄**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**CIM \_ LogicalFile**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**Win32 \_ 目錄**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**Win32 \_ NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**Win32 \_ 共用**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**Win32 \_ ShortcutFile**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

下列清單列出 **AccessMask** 屬性中的檔案和目錄存取權限的值。 這個屬性是點陣圖。

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**檔案 \_ 讀取 \_ 資料**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



授與從檔案讀取資料的許可權。


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**檔案 \_ 清單 \_ 目錄**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



授與從檔案讀取資料的許可權。 若為目錄，此值會授與許可權來列出目錄的內容。


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**檔案 \_ 寫入 \_ 資料**
</dt> <dd> <dl> <dt>

2 (0x2) 
</dt> <dt>



授與將資料寫入檔案的許可權。


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**檔案 \_ 新增 \_ 檔案**
</dt> <dd> <dl> <dt>

2 (0x2) 
</dt> <dt>



授與將資料寫入檔案的許可權。 若為目錄，此值會授與在目錄中建立檔案的許可權。


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**檔案 \_ 附加 \_ 資料**
</dt> <dd> <dl> <dt>

4 (0x4) 
</dt> <dt>



授與將資料附加至檔案的許可權。 若為目錄，此值會授與建立子目錄的許可權。


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**檔案 \_ 新增 \_ 子目錄**
</dt> <dd> <dl> <dt>

4 (0x4) 
</dt> <dt>



授與將資料附加至檔案的許可權。 若為目錄，此值會授與建立子目錄的許可權。


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_ 讀取 \_ EA**
</dt> <dd> <dl> <dt>

8 (0x8) 
</dt> <dt>



授與讀取擴充屬性的許可權。


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_ 寫入 \_ EA**
</dt> <dd> <dl> <dt>

16 (0x10) 
</dt> <dt>



授予寫入擴充屬性的許可權。


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**檔案 \_ 執行**
</dt> <dd> <dl> <dt>

32 (0x20) 
</dt> <dt>



授與許可權來執行檔案。


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**檔案 \_ 遍歷**
</dt> <dd> <dl> <dt>

32 (0x20) 
</dt> <dt>



授與許可權來執行檔案。 若為目錄，可以進行目錄的往返。


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**檔案 \_ 刪除 \_ 子系**
</dt> <dd> <dl> <dt>

64 (0x40) 
</dt> <dt>



授與刪除目錄的許可權，以及它所包含的所有檔案 (其子) ，即使檔案是唯讀的。


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_ 讀取 \_ 屬性**
</dt> <dd> <dl> <dt>

128 (0x80) 
</dt> <dt>



授與讀取檔案屬性的許可權。


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_ 寫入 \_ 屬性**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



授與變更檔案屬性的許可權。


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**刪除**
</dt> <dd> <dl> <dt>

65536 (0x10000) 
</dt> <dt>



授與刪除物件的許可權。


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_ 控制**
</dt> <dd> <dl> <dt>

131072 (0x20000) 
</dt> <dt>



授與許可權，以讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000) 
</dt> <dt>



授與許可權來修改物件之物件安全描述項中的 DACL。


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_ 擁有者**
</dt> <dd> <dl> <dt>

524288 (0x80000) 
</dt> <dt>



授與許可權來變更物件之安全描述項中的擁有者。


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步**
</dt> <dd> <dl> <dt>

1048576 (0x100000) 
</dt> <dt>



授與使用物件進行同步處理的許可權。 這可讓進程等候，直到物件處於已發出信號的狀態。 某些物件類型不支援此存取權。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winnt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> </dl>

 

