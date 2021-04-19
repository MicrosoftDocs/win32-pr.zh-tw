---
description: 變更 TPM 裝置的擁有者授權認證。 需要舊的和新的擁有者授權密碼。
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: CIM_TPM 類別的 ChangeOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974629"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>CIM TPM 類別的 ChangeOwnerAuth 方法 \_

變更 TPM 裝置的擁有者授權認證。 需要舊的和新的擁有者授權密碼。

## <a name="syntax"></a>語法


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OldOwnerAuth* \[在\]
</dt> <dd>

代表取得 TPM 裝置擁有權所需的舊擁有者授權認證。Cim **\_ SharedCredential** 的非 null 值可能需要 **cim \_ SharedCredential** 子類別。參數的 Secret 屬性。

</dd> <dt>

*NewOwnerAuth* \[在\]
</dt> <dd>

代表取得 TPM 裝置擁有權所需的新擁有者授權認證。Cim **\_ SharedCredential** 的非 null 值可能需要 **cim \_ SharedCredential** 子類別。參數的 Secret 屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**未知/未指定的錯誤** (2) 
</dt> <dt>

**DMTF 保留** (3. 4095) 
</dt> <dt>

**方法保留** (4096. 32767) 
</dt> <dt>

**指定的廠商** (32768. 65535) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ TPM**](cim-tpm.md)
</dt> </dl>

 

 




