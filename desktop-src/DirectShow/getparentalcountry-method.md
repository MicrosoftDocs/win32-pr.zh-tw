---
description: DVDAdm. GetParentalCountry 方法會抓取最後儲存至登錄的家長監護/區域。
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: 'GetParentalCountry 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeeee55a3e39449c48e1af6b2674db85d5c4a964e730e5a66bb91be6dca2c393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756758"
---
# <a name="getparentalcountry-method"></a>GetParentalCountry 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`DVDAdm.GetParentalCountry`方法會抓取上次儲存至登錄的家長監護/區域。

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>傳回值

傳回整數，指出儲存在登錄中的預設國家/地區代碼。

## <a name="remarks"></a>備註

此方法所抓取的「家長」國家/地區不一定是目前儲存在 MSWebDVD 物件中的相同國家/地區。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>區段。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 




