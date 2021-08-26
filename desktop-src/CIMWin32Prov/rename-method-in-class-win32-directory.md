---
description: 重新命名物件路徑中指定的目錄專案檔。
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Win32_Directory 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 86b6bd35b14ee2a342dee27615c1ff21d9274a5f3020c4f804df5065f430813f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077438"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Win32 目錄類別的重新命名方法 \_

**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名物件路徑中指定的目錄專案檔。 如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FileName* 
</dt> <dd>

檔案 (或目錄) 的完整新名稱。 範例： c： \\ temp \\newfile.txt。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功重新命名檔案，則傳回值為 0 (零) ，以及表示錯誤的其他任何數位。

<dl> <dt>

**0**
</dt> <dd>

要求成功。

</dd> <dt>

**2**
</dt> <dd>

存取遭到拒絕。

</dd> <dt>

**8**
</dt> <dd>

發生未指定的失敗。

</dd> <dt>

**9**
</dt> <dd>

指定的名稱無效。

</dd> <dt>

**10**
</dt> <dd>

指定的物件已經存在。

</dd> <dt>

**11**
</dt> <dd>

檔案系統不是 NTFS。

</dd> <dt>

**12**
</dt> <dd>

平臺未 Windows。

</dd> <dt>

**13**
</dt> <dd>

磁片磁碟機不相同。

</dd> <dt>

**14**
</dt> <dd>

目錄不是空的。

</dd> <dt>

**15**
</dt> <dd>

發生共用違規。

</dd> <dt>

**16**
</dt> <dd>

指定的起始檔無效。

</dd> <dt>

**17**
</dt> <dd>

不會保留操作所需的許可權。

</dd> <dt>

**21**
</dt> <dd>

指定的參數無效。

</dd> </dl>

## <a name="remarks"></a>備註

若要重新命名資料夾，請先系結至有問題的資料夾，然後呼叫重新命名方法。 作為方法的唯一參數，以完整路徑名稱傳遞資料夾的新名稱。 例如，如果 C： script 記錄備份中的 \\ 資料夾 \\ 要重新命名為 \\ c： \\ scripts \\ Archive，您必須傳遞 c： script \\ \\ archive 作為完整的資料夾名稱。 只傳遞資料夾名稱-封存-會導致不正確路徑錯誤。

Win32 \_ 目錄類別不提供移動資料夾的逐步方法。 相反地，移動資料夾通常包含兩個步驟：

<dl> 1. 將資料夾複製到新位置  
2. 正在刪除原始檔案夾  
</dl>

這項雙步驟程式的唯一例外，就是將資料夾移至相同磁片磁碟機上的新位置。 例如，假設您想要將 C： \\ Temp 移至 c： \\ 編寫 \\ 暫存檔案封存 \\ 的腳本。 只要目前的位置和新的位置都在相同的磁片磁碟機上，只要呼叫 Rename 方法並傳遞新的位置做為方法參數，就可以移動資料夾。 這種方法可以有效地讓您在單一步驟中移動資料夾。 但是，如果目前磁片磁碟機和新磁片磁碟機不同，腳本就會失敗。 嘗試將 C： temp 重新命名 \\ 為 D： \\ temp 失敗，並出現「磁片磁碟機不相同」錯誤。

## <a name="examples"></a>範例

下列程式碼會從 TechNet 資源庫上 [使用 WMI VBScript 範例移動資料夾](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) ，使用重新命名方法將資料夾 c： \\ 腳本移至 c： \\ Admins 檔封存 \\ \\ \\ VBScript。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
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

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 目錄**](win32-directory.md)
</dt> </dl>

 

