---
description: CIM_DataFile 類別的 CompressEx 方法-使用 NTFS 壓縮來壓縮物件路徑中所指定的邏輯檔案 (或目錄) 。 這個方法繼承自 CIM \_ LogicalFile。
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 CompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad63096e34283ae6ea763690045072b5d2e5579ce1f459bcc7c7bc92d671e0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420156"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a>CIM \_ 資料檔案類別的 CompressEx 方法

**CompressEx** 方法會使用 NTFS 壓縮來壓縮物件路徑中指定的邏輯檔案 (或目錄) 。 這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。 這個方法是 [**壓縮**](compress-method-in-class-cim-datafile.md) 方法的擴充版本，會繼承自 [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StopFileName* \[擴展\]
</dt> <dd>

字串，代表方法失敗 (或目錄) 的名稱。 如果方法成功，則此參數為 null。

</dd> <dt>

*StartFileName* \[在\]
</dt> <dd>

字串，表示要作為此方法起點的子檔 (或目錄) 。 一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。 如果這個參數是 null，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。

如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。

</dd> <dt>

*遞迴* \[在\]
</dt> <dd>

若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ 資料檔案**](cim-datafile.md) 實例所指定之目錄中的檔案和目錄。 若為檔案實例，則會忽略這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

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

[**CIM \_ 資料檔案**](cim-datafile.md)中的 **COMPRESSEX** 方法是由 WMI 所執行。

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

[CIM \_ 資料檔案](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ 資料檔案**](cim-datafile.md)
</dt> <dt>

[WMI 工作：檔案和資料夾](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**檔案和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

