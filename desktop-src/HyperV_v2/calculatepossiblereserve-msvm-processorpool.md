---
description: 這個方法是用來尋找實際的保留，而輸入參數是計算保留的虛擬機器處理器數目。
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Msvm_ProcessorPool 類別的 CalculatePossibleReserve 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06cfa01dd89392c05f460462d8bda5898b47d90b6e027fa885bf039f62488cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042068"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Msvm ProcessorPool 類別的 CalculatePossibleReserve 方法 \_

這個方法是用來尋找實際的保留，而輸入參數是計算保留的虛擬機器處理器數目。 這個方法是必要的，因為處理器資源的保留會高度依賴必須以平行方式排程的處理器數目。

## <a name="syntax"></a>語法


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProcessorCount* \[在\]
</dt> <dd>

類型： **uint16**

計算保留的虛擬機器處理器數目。 這個屬性的最大值是主機電腦的邏輯處理器計數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

可能保留給虛擬機器的 CPU 資源數量。

## <a name="remarks"></a>備註

存取 [**Msvm \_ ProcessorPool**](msvm-processorpool.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**Msvm \_ ProcessorPool**](msvm-processorpool.md)
</dt> </dl>

 

