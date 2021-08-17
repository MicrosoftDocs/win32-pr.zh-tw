---
description: Uncompresses 邏輯編解碼器檔案 (或在物件路徑中指定的目錄) 。 這個方法是解壓縮方法的擴充版本。
ms.assetid: 257c69fa-c4f7-48be-8317-55db4b01601b
ms.tgt_platform: multiple
title: Win32_CodecFile 類別的 UncompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75a22bbb8050d31778619cb4a5870254e1e840c334fbe8d93d9b7882dc1a9132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834469"
---
# <a name="uncompressex-method-of-the-win32_codecfile-class"></a>Win32 CodecFile 類別的 UncompressEx 方法 \_

**UncompressEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會 uncompresses 物件路徑中指定的邏輯編解碼器檔案 (或目錄) 。 這個方法是 [**解壓縮**](uncompress-method-in-class-win32-directory.md) 方法的擴充版本。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StopFileName* \[擴展\]
</dt> <dd>

**UncompressEx** 方法失敗之檔案或目錄的名稱。 如果方法成功，此參數將會是 **null** 。

</dd> <dt>

*StartFileName* \[在中，選擇性\]
</dt> <dd>

將子檔案或目錄命名為 **UncompressEx** 的起點。 *StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。 如果這個參數是 **Null**，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。

</dd> <dt>

*遞迴* \[在中，選擇性\]
</dt> <dd>

若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。 注意：對於檔案實例， *遞迴* 輸入參數會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功解壓縮檔案，則傳回整數值 0 (零) ，以及表示錯誤的其他任何數位。

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

 

