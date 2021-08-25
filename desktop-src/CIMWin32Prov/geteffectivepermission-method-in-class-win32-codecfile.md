---
description: 使用許可權參數中所設定的值，來判斷使用者是否在代表該編解碼器檔案的 Win32 CodecFile 物件的 AccessMask 屬性中設定指定的許可權 \_ 。
ms.assetid: 068dfcaf-037b-4516-b85a-8ba6558ba561
ms.tgt_platform: multiple
title: 'Win32_CodecFile 類別的 GetEffectivePermission 方法 (Aclui) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c3740d1c87b5d74968d0bc4eb92ed8246c9a3c2a0a42a3b0c434c74f306a203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878978"
---
# <a name="geteffectivepermission-method-of-the-win32_codecfile-class"></a>Win32 CodecFile 類別的 GetEffectivePermission 方法 \_

[**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會使用 *許可權* 參數中所設定的值，來判斷使用者是否已在代表該編解碼器檔案的 [**Win32 \_ CodecFile**](win32-codecfile.md)物件的 **AccessMask** 屬性中設定指定的許可權。 許可權適用于檔案、檔案所在的目錄，以及共用（如果目錄或檔案位於共用中）。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*許可權* \[在\]
</dt> <dd>

在 [**Win32 \_ CodecFile**](win32-codecfile.md)物件的 **AccessMask** 屬性中設定的許可權點陣圖。

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**檔案 \_讀取 \_ 資料 (檔) 檔案 \_ 清單 \_ 目錄 (目錄)** (1 (0x1) ) 


</dt> <dd>

授與從檔案讀取資料的許可權。 若為目錄，此值會授與許可權來列出目錄的內容。

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**檔案 \_寫入 \_ 資料 (檔案) 檔案 \_ 新增檔案 \_ (目錄)** (2 (0x2) ) 


</dt> <dd>

授與將資料寫入檔案的許可權。 若為目錄，此值會授與在目錄中建立檔案的許可權。

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**檔案 \_附加 \_ 資料 (檔) 檔案 \_ 新增 \_ 子目錄 (目錄)** (4 (0x4) ) 


</dt> <dd>

授與將資料附加至檔案的許可權。 若為目錄，此值會授與建立子目錄的許可權。

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**檔案 \_讀取 \_ EA** (8 (0x8) ) 


</dt> <dd>

授與讀取擴充屬性的許可權。

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**檔案 \_寫入 \_ EA** (16 (0x10) ) 


</dt> <dd>

授予寫入擴充屬性的許可權。

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**檔案 \_執行 (檔) 檔案 \_ (目錄)** (32 (0x20) ) 


</dt> <dd>

授與許可權來執行檔案。 若為目錄，可以進行目錄的往返。

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**檔案 \_刪除 \_ 子 (目錄)** (64 (0x40) ) 


</dt> <dd>

授與刪除目錄的許可權，以及其包含的所有檔案（即使檔案是唯讀的）。

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**檔案 \_讀取 \_ 屬性** (128 (0x80) ) 


</dt> <dd>

授與讀取檔案屬性的許可權。

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**檔案 \_將 \_ 屬性寫入** (256 (0x100) ) 


</dt> <dd>

授與變更檔案屬性的許可權。

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**刪除** (65536 (0x10000) ) 


</dt> <dd>

授與刪除存取權。

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072 (0x20000) ) 


</dt> <dd>

授與安全描述項和擁有者的讀取權限。

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144 (0x40000) ) 


</dt> <dd>

授與任意存取控制清單 (ACL) 的寫入權限。

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**寫入 \_擁有** 者 (524288 (0x80000) ) 


</dt> <dd>

指派寫入擁有者。

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**同步處理** (1048576 (0x100000) ) 


</dt> <dd>

同步存取，並允許進程等候物件進入已發出信號的狀態。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

當呼叫端具有指定的許可權時傳回 **True** ，當呼叫端沒有指定的許可權時傳回 **false** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| 標頭<br/>                   | <dl> <dt>Aclui。h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ CodecFile**](win32-codecfile.md)
</dt> </dl>

 

