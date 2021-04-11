---
description: 重新命名物件路徑中指定的編解碼器檔案。
ms.assetid: fd6ce02c-d513-4643-ac27-313c32732f1e
ms.tgt_platform: multiple
title: Win32_CodecFile 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4eb931a0155518ad9644ebb1cce0b604be80602
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936432"
---
# <a name="rename-method-of-the-win32_codecfile-class"></a>Win32 CodecFile 類別的重新命名方法 \_

**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名物件路徑中指定的編解碼器檔案。 如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。

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

傳回整數值 0 (零) 如果成功重新命名檔案，則傳回任何其他數位，表示錯誤。

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

[**Win32 \_ CodecFile**](win32-codecfile.md)
</dt> </dl>

 

