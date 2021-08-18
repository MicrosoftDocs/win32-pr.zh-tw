---
description: 指出數值密碼是否符合此驗證值的特殊格式需求。
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Win32_EncryptableVolume 類別的 IsNumericalPasswordValid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0aed00554d7a8e284f83659dc92266b1ce5e098f1b102e6444bfc07fd2909066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739638"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 IsNumericalPasswordValid 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **IsNumericalPasswordValid** 方法會指出數值密碼是否符合此驗證值的特殊格式需求。

## <a name="syntax"></a>語法


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumericalPassword* \[在\]
</dt> <dd>

類型： **字串**

指定數位密碼的字串。

數值密碼必須包含48位數。 這些數位可以分為6位數的8個群組，每個群組中的最後一個數位指出群組的總和檢查碼值。 6位數的每個群組都必須可以整除11個，且必須小於720896。 假設有一組六位數標示為 x1、x2、x3、x4、x5 和 x6，則總和檢查碼 x6 數位的計算方式為– x1 + x2 – x3 + x4 – x5 mod 11。

您可以選擇性地以空格或連字號分隔數位群組。 因此，"xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" 或 "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" 也可能包含有效的數值密碼。

</dd> <dt>

*IsNumericalPasswordValid* \[擴展\]
</dt> <dd>

類型： **布林值**

如果數值密碼符合此驗證值的特殊格式需求，則布林值為 true，否則值為 false。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                 | 描述                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista Enterprise，僅 Windows vista 旗艦版傳統型 \[ 應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
