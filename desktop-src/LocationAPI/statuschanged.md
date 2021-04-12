---
description: 當報表的操作狀態變更時發生。
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: StatusChanged 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195597"
---
# <a name="statuschanged-event"></a>StatusChanged 事件

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]

當報表的操作狀態變更時發生。

## <a name="syntax"></a>語法


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*status* 
</dt> <dd>

新的狀態。



| 狀態                                                                                               | 意義                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 不支援報表。<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 錯誤。<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 拒絕存取。<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | 正在初始化。<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 執行中。<br/>              |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

您應該針對市政位址報告和緯度/經度報表，執行不同的狀態變更報告處理常式。

## <a name="examples"></a>範例

如需如何使用此事件的範例，請參閱 [接聽 LatLong 報表事件](/uwp/api/Windows.Devices.Geolocation)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

