---
description: 當產生新的緯度/經度報表時發生。
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: NewLatLongReport 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975573"
---
# <a name="newlatlongreport-event"></a>NewLatLongReport 事件

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]

當產生新的緯度/經度報表時發生。

## <a name="syntax"></a>語法


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*newReport* 
</dt> <dd>

新的 [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="examples"></a>範例

如需如何使用此事件的範例，請參閱 [接聽 LatLong 報表事件](/uwp/api/Windows.Devices.Geolocation)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

