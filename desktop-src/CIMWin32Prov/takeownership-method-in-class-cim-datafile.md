---
description: TakeOwnerShip 方法會取得物件路徑中所指定之邏輯檔案的擁有權。
ms.assetid: 0835c335-0ada-44c1-9e71-44ba2041d8e2
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 TakeOwnerShip 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf1965c82c810400921d9a6bb3e4e64551338bd40d7289e4863bab10abd189d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751868"
---
# <a name="takeownership-method-of-the-cim_datafile-class"></a>CIM \_ 資料檔案類別的 TakeOwnerShip 方法

**TakeOwnerShip** 方法會取得物件路徑中所指定之邏輯檔案的擁有權。 如果邏輯檔案是目錄，則此方法會以遞迴方式執行，以取得目錄包含的所有檔案和子目錄的擁有權。 這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

在成功時傳回0的值，並傳回任何其他數位以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**0**
</dt> <dd>

成功。

</dd> <dt>

**2**
</dt> <dd>

拒絕存取。

</dd> <dt>

**8**
</dt> <dd>

未指定的失敗。

</dd> <dt>

**9**
</dt> <dd>

不正確物件。

</dd> <dt>

**10**
</dt> <dd>

物件已存在。

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

目錄未清空。

</dd> <dt>

**15**
</dt> <dd>

共用違規。

</dd> <dt>

**16**
</dt> <dd>

不正確啟動檔案。

</dd> <dt>

**17**
</dt> <dd>

未保留許可權。

</dd> <dt>

**21**
</dt> <dd>

無效的參數。

</dd> </dl>

## <a name="remarks"></a>備註

[**CIM \_ 資料檔案**](cim-datafile.md)中的 **TAKEOWNERSHIP** 方法是由 WMI 所執行。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

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

[CIM \_ 資料檔案](takeownership-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ 資料檔案**](cim-datafile.md)
</dt> <dt>

[WMI 工作：檔案和資料夾](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**檔案和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

