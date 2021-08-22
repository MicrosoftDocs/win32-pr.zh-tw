---
description: 取得物件路徑中指定之邏輯目錄專案檔的擁有權。 這個方法是 TakeOwnerShip 方法的擴充版本，會繼承自 CIM \_ LogicalFile。
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: CIM_Directory 類別的 TakeOwnerShipEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5637e45c6dad7eec3f79ffd045a4a8d0dd3f3ba51ed5a60c09916c11802b1130
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332778"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a>CIM 目錄類別的 TakeOwnerShipEx 方法 \_

**TakeOwnerShipEx** 方法會取得物件路徑中指定之邏輯目錄專案檔的擁有權。 這個方法是 [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) 方法的擴充版本，會繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。 如果邏輯檔案是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
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

字串，表示要作為此方法起點的子檔 (或目錄) 。 一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。 如果這個參數是 null，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。

</dd> <dt>

*遞迴* \[在\]
</dt> <dd>

若 **為 True**，則會以遞迴方式將方法套用至 [**CIM \_ 目錄**](cim-directory.md) 實例所指定之目錄中的檔案和目錄。 若為檔案實例，則會忽略這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回0的值，並傳回任何其他數位以表示錯誤。

<dl> <dt>


</dt> <dd>

0

成功。

</dd> <dt>


</dt> <dd>

2

拒絕存取。

</dd> <dt>


</dt> <dd>

8

未指定的失敗。

</dd> <dt>


</dt> <dd>

9

不正確物件。

</dd> <dt>


</dt> <dd>

10

物件已存在。

</dd> <dt>


</dt> <dd>

11

檔案系統不是 NTFS。

</dd> <dt>


</dt> <dd>

12

平臺未 Windows。

</dd> <dt>


</dt> <dd>

13

磁片磁碟機不相同。

</dd> <dt>


</dt> <dd>

14

目錄未清空。

</dd> <dt>


</dt> <dd>

15

共用違規。

</dd> <dt>


</dt> <dd>

16

不正確啟動檔案。

</dd> <dt>


</dt> <dd>

17

未保留許可權。

</dd> <dt>


</dt> <dd>

21

無效的參數。

</dd> </dl>

## <a name="remarks"></a>備註

這個方法目前不是由 WMI 所執行。 若要使用這個方法，您必須在自己的提供者中加以執行。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="examples"></a>範例

下列 Visual Basic 腳本程式碼會呼叫 **TakeOwnerShipEx** 方法來取得 C： temp 資料夾的擁有權 \\ 。


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
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

[CIM \_ 目錄](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[**CIM \_ 目錄**](cim-directory.md)
</dt> </dl>

 

