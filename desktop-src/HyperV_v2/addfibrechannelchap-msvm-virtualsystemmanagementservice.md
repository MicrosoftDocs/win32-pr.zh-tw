---
description: 將 DH-CHAP (Diffie-hellman 的) 參數新增到虛擬機器上的綜合光纖通道埠。
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Msvm_VirtualSystemManagementService 類別的 AddFibreChannelChap 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26a9f99826e92a35462f0c42e8fce723168799177e96e0ae429aad45c99de928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562358"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 AddFibreChannelChap 方法 \_

將 DH-CHAP (Diffie-hellman 的) 參數新增到虛擬機器上的綜合光纖通道埠。 如果虛擬機器正在執行，這個方法將會失敗。

## <a name="syntax"></a>語法


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FcPortSettings* \[在\]
</dt> <dd>

字串陣列，其中包含 [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) 類別的內嵌實例，描述虛擬機器的綜合光纖通道埠的設定。 每個實例的 **InstanceID** 屬性都會識別要修改的元素。

</dd> <dt>

*SecretEncoding* \[在\]
</dt> <dd>

指定共用密碼的編碼類型。

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

**可列印的 ASCII** (1) 


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**二元** (2) 


</dt> <dd></dd> </dl> </dd> <dt>

*SharedSecret* \[在\]
</dt> <dd>

指定共用機密。

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

 

 




