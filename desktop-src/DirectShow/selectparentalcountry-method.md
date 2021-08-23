---
description: SelectParentalCountry 方法會設定指定的家長/區域以進行後續播放。
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: SelectParentalCountry 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d148145f2c38cdb01da209e02f6400301da851e1d2b41e5adaf84b2338ad21c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684058"
---
# <a name="selectparentalcountry-method"></a>SelectParentalCountry 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`SelectParentalCountry`方法會設定指定的家長/區域以進行後續播放。

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

將國家/地區指定為整數。

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

將目前登入的使用者指定為字串。  (目前已忽略。 ) 

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

指定應用程式密碼字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

家長監護/區域會決定如何解讀家長監護。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



