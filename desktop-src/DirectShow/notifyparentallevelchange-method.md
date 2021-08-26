---
description: NotifyParentalLevelChange 方法會啟用或停用暫存家長管理層級命令的事件處理。
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: 'NotifyParentalLevelChange 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8382b52f64d4196b0ef74e5f3285e9bb047a4e1f77d3b0e5bec4da218ee753b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997358"
---
# <a name="notifyparentallevelchange-method"></a>NotifyParentalLevelChange 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`NotifyParentalLevelChange`方法會啟用或停用暫存家長管理層級命令的事件處理。

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*
</dt> <dd>

指定布林值，指出當 MSWebDVD 物件遇到分級高於整個光碟評等的影片區段時，是否要通知應用程式。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

預設會停用家長監護的管理通知。 這表示允許來自光碟的暫存家長命令，但會忽略，而不會中斷光碟的播放。 如果您需要處理來自光碟的臨時家長管理層級命令，請在初始化應用程式期間呼叫此方法。若要在啟用「家長管理」之後加以停用，請使用 false 的引數來呼叫這個方法。 如需有關家長管理的詳細資訊，請參閱 [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>區段。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 




