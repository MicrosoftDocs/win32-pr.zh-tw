---
description: 卸載指定的 PCI 裝置，讓它可以指派。
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Msvm_AssignableDeviceService 類別的 DismountAssignableDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c9b602a26f789b0d7ccded487bafe8c0295133f6e4dd9457d51ce33ee24a8d0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693478"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>Msvm AssignableDeviceService 類別的 DismountAssignableDevice 方法 \_

卸載指定的 PCI 裝置，讓它可以指派。

## <a name="syntax"></a>語法


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DismountSettingData* \[在\]
</dt> <dd>

設定資料物件的內嵌實例，這個物件會指定要卸載的 PCI 裝置。

</dd> <dt>

*DismountedDeviceInstancePath* \[擴展\]
</dt> <dd>

包含已卸載裝置之裝置實例路徑的字串。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果工作已完成) ，則作業 (的參考可以是 null。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，傳回0或 4096;否則，會傳回錯誤。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
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
</dt> <dt>

**找不到** 檔案 (32779) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




