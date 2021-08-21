---
description: 壓縮物件路徑中指定 (或目錄) 的邏輯目錄專案檔。
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: 壓縮 Win32_Directory 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15d9142abb95998fce803c30c439632775cd8ff807f3b7d99653875d08e534e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020666"
---
# <a name="compress-method-of-the-win32_directory-class"></a>壓縮 Win32 \_ 目錄類別的方法

**壓縮** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將邏輯目錄專案檔壓縮 (或在物件路徑中指定的目錄) 。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Compress();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回值 0 (零) 如果檔案已成功壓縮，則為，而任何其他數位表示錯誤。

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

壓縮提供一種方法來釋出磁片磁碟機上的額外儲存空間，而不需要購買新硬體，也不需要移除檔案或資料夾。 根據硬碟的大小以及儲存在該磁片上的檔案類型而定，您或許可以復原數百 mb 的磁碟空間，因此不需要購買新的硬碟，也不需要在安裝新磁片磁碟機的情況下讓電腦離線。

壓縮方法會壓縮指定資料夾內的所有檔案和子資料夾。 此外，此類別也包含可從資料夾中的所有檔案和子資料夾中移除壓縮的解壓縮方法。 CIM 資料檔案類別也會提供類似的方法 \_ 。 這可讓您選擇性地壓縮或解壓縮資料夾中的特定檔案。

由於壓縮 imparts 效能會稍微降低，因此不建議針對例行存取的檔案或資料夾進行存取;例如，您可能不想要壓縮資料庫檔案、記錄檔或使用者設定檔資料夾。 更好的壓縮候選項目為不常存取的檔案和資料夾。 例如，您可以撰寫腳本，以傳回一或多個月未存取之磁片磁碟機上的資料夾集合，然後壓縮每個資料夾。

壓縮資料夾所釋出的磁碟空間量會根據儲存在該資料夾中的檔案類型而有所不同。 例如，.jpg 的檔案已經過壓縮，而進一步的壓縮對檔案的大小沒有太大的影響。 不過，其他檔案類型的節省量可能很可觀。 例如，在 Windows 2000 測試電腦上建立新的資料夾，並在 33 Microsoft Word 檔上，將總磁碟空間占總 15 mb () mb，然後複製到該資料夾。 壓縮檔時，資料夾只佔用 7 MB 的磁碟空間。

## <a name="examples"></a>範例

下列 VBScript 範例會壓縮資料夾 C： \\ 腳本。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
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
</dt> <dt>

[**解壓**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

