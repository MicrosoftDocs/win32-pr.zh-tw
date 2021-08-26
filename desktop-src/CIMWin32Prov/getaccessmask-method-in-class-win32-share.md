---
description: Win32_Share 類別的 GetAccessMask 方法-傳回 uint32 點陣圖，其具有使用者或群組所持有之共用的存取權限，該共用會傳回該實例。
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Win32_Share 類別的 GetAccessMask 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ebc2b2620b0bdc019e117f9a4b2c376be6320be968fdae42509dc3f62c3cc9a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077658"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a>Win32 共用類別的 GetAccessMask 方法 \_

**GetAccessMask** 方法會傳回具有使用者或群組（代表傳回實例）所持有之共用的存取權限的 uint32 點陣圖。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

使用者或群組所持有之共用的存取權限。

<dl> <dt>

**檔案 \_ 清單 \_ 目錄**
</dt> <dd>

1 (0x1) 

授與從檔案讀取資料的許可權。 若為目錄，此值會授與許可權來列出目錄的內容。

</dd> <dt>

**檔案 \_ 新增 \_ 檔案**
</dt> <dd>

2 (0x2) 

授與將資料寫入檔案的許可權。 若為目錄，此值會授與在目錄中建立檔案的許可權。

</dd> <dt>

**檔案 \_ 新增 \_ 子目錄**
</dt> <dd>

4 (0x4) 

授與將資料附加至檔案的許可權。 若為目錄，此值會授與建立子目錄的許可權。

</dd> <dt>

**檔案 \_ 讀取 \_ EA**
</dt> <dd>

8 (0x8) 

授與讀取擴充屬性的許可權。

</dd> <dt>

**檔案 \_ 寫入 \_ EA**
</dt> <dd>

16 (0x10) 

授予寫入擴充屬性的許可權。

</dd> <dt>

**檔案 \_ 遍歷**
</dt> <dd>

32 (0x20) 

授與許可權來執行檔案。 若為目錄，可以進行目錄的往返。

</dd> <dt>

**檔案 \_ 刪除 \_ 子系**
</dt> <dd>

64 (0x40) 

授與刪除目錄的許可權，以及它所包含的所有檔案 (其子) ，即使檔案是唯讀的。

</dd> <dt>

**檔案 \_ 讀取 \_ 屬性**
</dt> <dd>

128 (0x80) 

授與讀取檔案屬性的許可權。

</dd> <dt>

**檔案 \_ 寫入 \_ 屬性**
</dt> <dd>

256 (0x100)

授與變更檔案屬性的許可權。

</dd> <dt>

**DELETE**
</dt> <dd>

65536 (0x10000) 

授與刪除存取權。

</dd> <dt>

**讀取 \_ 控制**
</dt> <dd>

131072 (0x20000) 

授與安全描述項和擁有者的讀取權限。

</dd> <dt>

**寫入 \_ DAC**
</dt> <dd>

262144 (0x40000) 

授與任意存取控制清單 (DACL) 的寫入權限。

</dd> <dt>

**寫入 \_ 擁有者**
</dt> <dd>

524288 (0x80000) 

指派寫入擁有者。

</dd> <dt>

**同步**
</dt> <dd>

1048576 (0x100000) 

同步存取，並允許進程等候物件進入已發出信號的狀態。

</dd> </dl>

## <a name="remarks"></a>備註

**GetAccessMask** 方法是物件方法，並用於這個類別的出現位置。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會建立共用資料夾，然後取得安全描述項中保護共用資料夾的存取遮罩值。


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
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

[**Win32 \_ 共用**](win32-share.md)
</dt> </dl>

 

