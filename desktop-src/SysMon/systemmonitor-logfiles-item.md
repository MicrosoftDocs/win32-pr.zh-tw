---
title: 記錄檔。 Item 屬性
description: 從集合中抓取指定的 LogFileItem 實例。
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- 專案屬性 SysMon
- Item 屬性 SysMon，記錄檔類別
- 記錄檔類別 SysMon，專案屬性
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024828"
---
# <a name="logfilesitem-property"></a>記錄檔。 Item 屬性

從集合中抓取指定的 [**LogFileItem**](logfileitem.md) 實例。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>屬性值

對應至指定之索引值的 [**LogFileItem**](logfileitem.md)實例。

## <a name="remarks"></a>備註

這是記錄 [**檔物件的**](systemmonitor-logfiles.md) 預設屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





