---
description: Msvm_MetricService 類別的 ModifyServiceSettings 方法-修改服務的設定資料。
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Msvm_MetricService 類別的 ModifyServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 51af98d230433687d9a16cb3ab858fd746b7ff1ca4e17eaf0b36cce16e92c875
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693908"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Msvm MetricService 類別的 ModifyServiceSettings 方法 \_

修改服務的設定資料。

## <a name="syntax"></a>語法


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SettingData* \[在\]
</dt> <dd>

包含 [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) 類別的內嵌實例，其中包含服務已修改的設定資料。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。



| 傳回碼/值                                                                                                                                                                | 描述                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**已完成，沒有錯誤**</dt> <dt>0</dt> </dl>                    | 成功。<br/>                                |
| <dl> <dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt> </dl> | 已檢查方法參數，作業已啟動。<br/> |
| <dl> <dt>**失敗**</dt> <dt>32768</dt> </dl>                                 | 失敗。<br/>                                 |
| <dl> <dt>**拒絕存取**</dt> <dt>32769</dt> </dl>                          | 拒絕存取。<br/>                          |
| <dl> <dt>**不支援**</dt> <dt>32770</dt> </dl>                          | 不支援。<br/>                          |
| <dl> <dt>**狀態為未知**</dt> <dt>32771</dt> </dl>                      | 狀態未知。<br/>                      |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | 超時時間。<br/>                               |
| <dl> <dt>**不正確參數**</dt> <dt>32773</dt> </dl>                      | 無效的參數。<br/>                      |
| <dl> <dt>**系統使用中**</dt> <dt>32774</dt> </dl>                       | 系統正在使用中。<br/>                       |
| <dl> <dt>**此操作的狀態無效**</dt> <dt>32775</dt> </dl>       | 此操作的狀態無效。<br/>       |
| <dl> <dt>**不正確的資料類型**</dt> <dt>32776</dt> </dl>                    | 不正確的資料類型。<br/>                    |
| <dl> <dt>**系統無法使用**</dt> <dt>32777</dt> </dl>                | 系統無法使用。<br/>                |
| <dl> <dt>**記憶體不足**</dt> <dt>32778</dt> </dl>                          | 記憶體不足。<br/>                          |



 

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

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

