---
description: Copy 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。
ms.assetid: 13bd7da8-a562-414b-8d23-6f58e1c55878
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 Copy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c126f1cd54470e50a700fdea1c121776d687a9dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972560"
---
# <a name="copy-method-of-the-cim_datafile-class"></a>CIM \_ 資料檔案類別的 Copy 方法

**Copy** 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。 如果需要覆寫現有的邏輯檔案，則不支援複本。 這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

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

目的地檔 (或目錄) 的完整名稱。

範例： "c： \\ temp \\ newdirectory"

</dd> </dl>

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

平臺不是 Windows。

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

[**CIM \_ 資料檔案**](cim-datafile.md)中的 **COPY** 方法是由 WMI 所執行。

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

[CIM \_ 資料檔案](copy-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ 資料檔案**](cim-datafile.md)
</dt> <dt>

[WMI 工作：檔案和資料夾](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**檔案和目錄存取權限常數**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

