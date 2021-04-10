---
description: 將物件路徑中指定的邏輯分頁檔或目錄複寫到輸入參數所指定的位置。
ms.assetid: e1ff3e91-dc30-4849-b80a-8838b527ad63
ms.tgt_platform: multiple
title: Win32_PageFile 類別的 Copy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bde9e0b5cf9b8ab88b5efa1c6aae58a9b8a54cfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187748"
---
# <a name="copy-method-of-the-win32_pagefile-class"></a>Win32 \_ 分頁檔類別的 Copy 方法

**複製** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將物件路徑中指定的邏輯分頁檔或目錄複寫到輸入參數所指定的位置。 如果需要覆寫現有的邏輯檔案，則不支援複製。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

 (或目錄) 之檔案複本的完整名稱。

範例： c： \\ temp \\ newdirectory

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

[**Win32 \_ 分頁檔**](win32-pagefile.md)
</dt> </dl>

 

