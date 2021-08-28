---
description: 將功能設定新增至乙太網路交換器埠的設定。
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Msvm_VirtualEthernetSwitchManagementService 類別的 AddFeatureSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 679e4dbba4b8d3e90691955a0642f9a22692d73824059419f5faceacc85abaf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829658"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Msvm VirtualEthernetSwitchManagementService 類別的 AddFeatureSettings 方法 \_

將功能設定新增至乙太網路交換器埠的設定。

## <a name="syntax"></a>語法


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedConfiguration* \[在\]
</dt> <dd>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))衍生類別的參考，代表受影響的乙太網路交換器埠或乙太網路交換器設定。

</dd> <dt>

*FeatureSettings* \[在\]
</dt> <dd>

字串的陣列，其中包含衍生自 [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) 類別之類別的內嵌實例，以描述要新增至交換器埠設定的功能設定。

</dd> <dt>

*ResultingFeatureSettings* \[擴展\]
</dt> <dd>

[**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md)類別實例的參考陣列，代表已加入的功能設定。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**失敗** (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**不正確參數** (4) 
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**方法保留** (4097. 32767) 
</dt> <dt>

**廠商特定** (32768. 65535) 
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

[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

