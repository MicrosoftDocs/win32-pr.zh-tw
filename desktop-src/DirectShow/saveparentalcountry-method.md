---
description: DVDAdm. SaveParentalCountry 方法會將應用程式的新家長/區域儲存至登錄。
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: 'SaveParentalCountry 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982632"
---
# <a name="saveparentalcountry-method"></a>SaveParentalCountry 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會將 `DVDAdm.SaveParentalCountry` 應用程式的新家長/區域儲存至登錄。

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

將家長的國家/地區指定為整數。

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

將使用者名稱指定為字串。  (目前已忽略。 ) 

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

將密碼指定為字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

此方法可讓知道目前密碼的使用者將新的家長監護/區域設定儲存至登錄。 如同 **MSDVDAdm** 的所有方法，這個方法不會影響播放程式中目前的層級;它只會變更登錄設定，以便下一次建立 MSWebDVD 物件時，會以新的國家/地區開啟。 若要在 player 中變更家長監護/區域，請呼叫 [**SelectParentalCountry**](selectparentalcountry-method.md)，而不會變更登錄設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>區段。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SaveParentalLevel**](saveparentallevel-method.md)
</dt> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 




