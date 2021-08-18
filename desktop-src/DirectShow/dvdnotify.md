---
description: DVDNotify 事件會通知應用程式有許多不同的 DVD 事件和光碟指令。
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: 'DVDNotify (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988deaf53fb2b50555b4cf19a38684610aa0822a270dfba079defab92ce8aec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148701"
---
# <a name="dvdnotify"></a>DVDNotify

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

此 `DVDNotify` 事件會通知應用程式有許多不同的 DVD 事件和光碟指令。

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

指定 DVD 事件通知碼。

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*
</dt> <dd>

可以包含與事件相關的其他資訊。

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

可以包含與事件相關的其他資訊。

</dd> </dl>

## <a name="remarks"></a>備註

[Dvd 事件通知代碼](dvd-notification-codes.md) 提供所有 DVD 事件通知碼及其參數的完整說明。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>區段。h</dt> </dl> |



 

 




