---
description: 刪除邏輯音訊或影片編解碼器檔案 (或物件路徑中指定的目錄) 。
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: Win32_CodecFile 類別的 DeleteEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df5527be497176f167ac368b872253fa3254a404
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847214"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a>Win32 CodecFile 類別的 DeleteEx 方法 \_

**DeleteEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會刪除邏輯音訊或影片編解碼器檔案 (或物件路徑中指定的目錄) 。 **DeleteEx** 是 [**刪除**](delete-method-in-class-win32-directory.md) 方法的擴充版本。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StopFileName* \[擴展\]
</dt> <dd>

**DeleteEx** 方法失敗之檔案或目錄的名稱。 如果方法成功，此參數將會是 **null** 。

</dd> <dt>

*StartFileName* \[在\]
</dt> <dd>

將子檔案或目錄命名為 **DeleteEx** 的起點。 *StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。 如果這個參數是 **Null**，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。 這是選擇性參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數值 0 (零) 如果成功刪除檔案，則傳回任何其他數位，表示錯誤。

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

 

