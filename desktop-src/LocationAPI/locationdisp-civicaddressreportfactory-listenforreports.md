---
description: 要求市政位址報告事件。
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: 'LocationDisp. CivicAddressReportFactory. ListenForReports 方法 (Locationapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945335"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>LocationDisp. CivicAddressReportFactory. ListenForReports 方法

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]

要求市政位址報告事件。

## <a name="syntax"></a>語法


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> 代表在市政位址報告事件之間要求時間的 (**double word**) 數目（以毫秒為單位）。 請參閱＜備註＞。</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

不需要位置提供者來提供您要求的精確度。 讀取 [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) 屬性的值，以探索真正的報表間隔設定。

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱 [接聽市政位址報表事件](/uwp/api/Windows.Devices.Geolocation)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                |
| 標頭<br/>                   | <dl> <dt>Locationapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NewCivicAddressReport 事件**](newcivicaddressreport.md)
</dt> </dl>

 

