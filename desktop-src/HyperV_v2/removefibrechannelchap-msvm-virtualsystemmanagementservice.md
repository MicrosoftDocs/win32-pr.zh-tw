---
description: 從虛擬機器中的綜合光纖通道埠，移除 DH-CHAP (Diffie-hellman 與挑戰交握驗證通訊協定) 參數。
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Msvm_VirtualSystemManagementService 類別的 RemoveFibreChannelChap 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b934839f6d908594ee58f0838c884fdedc48f372de061482ddf2147123a351c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147791"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 RemoveFibreChannelChap 方法 \_

從虛擬機器中的綜合光纖通道埠，移除 DH-CHAP (Diffie-hellman 與挑戰交握驗證通訊協定) 參數。 如果虛擬機器正在執行，這個方法將會失敗。

## <a name="syntax"></a>語法


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FcPortSettings* \[在\]
</dt> <dd>

字串陣列，其中包含 [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) 類別的內嵌實例，此類別會定義要從中移除 DH CHAP 參數的綜合光纖通道埠。 每個實例的 **InstanceID** 屬性都會識別要修改的元素。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**系統正在使用中** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




