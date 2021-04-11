---
description: 計算 RemoteFX 虛擬機器所需的視訊記憶體數量。
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Msvm_Synth3dVideoPool 類別的 CalculateVideoMemoryRequirements 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113629"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>Msvm Synth3dVideoPool 類別的 CalculateVideoMemoryRequirements 方法 \_

計算 RemoteFX 虛擬機器所需的視訊記憶體數量。

## <a name="syntax"></a>語法


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*monitorResolution* \[在\]
</dt> <dd>

虛擬機器的最大監視器解析度。 這必須是下列值之一。



| 值                                                                        | 意義                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 最大解析度為 1024 768。<br/>  |
| <dl> <dt>1</dt> </dl> | 最大解析度為 1280 1024。<br/> |
| <dl> <dt>2</dt> </dl> | 最大解析度為 1600 1200。<br/> |
| <dl> <dt>3</dt> </dl> | 最大解析度為 1920 1200。<br/> |



 

</dd> <dt>

*numberOfMonitors* \[在\]
</dt> <dd>

虛擬機器的監視器數目上限。 監視器的最小數目是1，而最大值則取決於螢幕解析度上限。 下表定義允許不同解析度的監視器數目上限。



| 解決方案             | 監視器上限 |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

*requiredVideoMemory* \[擴展\]
</dt> <dd>

接收所需的視訊記憶體數量（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回狀態碼，這可以是下列其中一個值。



| 傳回碼/值                                                                                                                                                                | Description                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**已完成，沒有錯誤**</dt> <dt>0</dt> </dl>                    | 成功。<br/>                                |
| <dl> <dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt> </dl> | 作業已啟動。<br/>                               |
| <dl> <dt>**失敗**</dt> <dt>32768</dt> </dl>                                 | 失敗。<br/>                                    |
| <dl> <dt>**拒絕存取**</dt> <dt>32769</dt> </dl>                          | 拒絕存取。<br/>                             |
| <dl> <dt>**不支援**</dt> <dt>32770</dt> </dl>                          | 不支援。<br/>                             |
| <dl> <dt>**狀態為未知**</dt> <dt>32771</dt> </dl>                      | 狀態未知。<br/>                         |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | 逾時。<br/>                                   |
| <dl> <dt>**不正確參數**</dt> <dt>32773</dt> </dl>                      | 參數無效。<br/>                  |
| <dl> <dt>**系統使用的是**</dt> <dt>32774</dt> </dl>                      | 系統正在使用中。<br/>                          |
| <dl> <dt>**此操作的狀態無效**</dt> <dt>32775</dt> </dl>       | 此操作的狀態無效。<br/> |
| <dl> <dt>**不正確的資料類型**</dt> <dt>32776</dt> </dl>                    | 不正確的資料類型。<br/>                       |
| <dl> <dt>**系統無法使用**</dt> <dt>32777</dt> </dl>                | 系統無法使用。<br/>                   |
| <dl> <dt>**記憶體不足**</dt> <dt>32778</dt> </dl>                          | 記憶體不足。<br/>                             |



 

## <a name="remarks"></a>備註

通常會在主機系統上呼叫這個方法，以判斷主機是否有足夠的可用視訊記憶體來裝載 RemoteFX 虛擬機器。 若要這樣做，請將這個方法所計算的視訊記憶體數量與 [**Msvm \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) 屬性進行比較，以判斷主機電腦是否有足夠的可用視訊記憶體。 您可以使用此資訊來判斷是否可以將虛擬機器移至主機系統。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ PhysicalGPUInfo**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**Msvm \_ Synth3dVideoPool**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




