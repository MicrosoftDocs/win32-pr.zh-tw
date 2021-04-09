---
description: 將物件路徑中指定的邏輯目錄專案檔或目錄複寫到輸入參數所指定的位置。
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Win32_Directory 類別的 Copy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110808"
---
# <a name="copy-method-of-the-win32_directory-class"></a>Win32 目錄類別的 Copy 方法 \_

**複製** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將物件路徑中指定的邏輯目錄專案檔或目錄複寫到輸入參數所指定的位置。 如果需要覆寫現有的邏輯檔案，則不支援複製。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FileName* 
</dt> <dd>

 (或目錄) 之檔案複本的完整名稱。 範例： c： \\ temp \\ newdirectory

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功複製檔案，則傳回 0 (零) 的值，以及表示錯誤的其他任何數位。

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

平臺不是 Windows。

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

資料夾通常需要從一個位置複製到另一個位置。 例如，您可以將資料夾從一部伺服器複製到另一部伺服器，以建立該資料夾的備份複本。 或者，您可能會有需要複製到使用者工作站的 [範本] 資料夾，或是應該複製到所有 DNS 伺服器的 [腳本] 資料夾。

Win32 \_ 目錄複寫方法可讓您在同一部 (電腦上將資料夾從一個位置複製到另一個位置，例如，將資料夾從磁片磁碟機 C 複製到磁片磁碟機 D) 或在遠端電腦上。 若要複製資料夾，您可以傳回要複製之資料夾的實例，然後呼叫 Copy 方法，以參數的方式傳遞新資料夾複本的目標位置。 例如，這行程式碼會將資料夾複製到磁片磁碟機 F 上的 Scripts 資料夾：

`objFolder.Copy("F:\Scripts")`

執行複製方法時，WMI 不會覆寫現有的資料夾。 這表示，如果目的地資料夾存在，則複製作業會失敗。 例如，假設您有一個名為 Scripts 的資料夾，而且您嘗試將該資料夾複製到名為「 \\ \\ atl-fs-01 封存」的遠端共用 \\ 。 如果該共用上已有名稱為 Scripts 的資料夾，複製作業會失敗。

## <a name="examples"></a>範例

從 [使用 WMI 複製資料夾](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2)中取得的下列程式碼範例會使用複製方法，將資料夾 C： \\ 腳本複製到 D： \\ Archive。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
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

 

