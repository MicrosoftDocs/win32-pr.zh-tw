---
description: DVDAdm. GetParentalCountry 方法會抓取最後儲存至登錄的家長監護/區域。
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: 'GetParentalCountry 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997021"
---
# <a name="getparentalcountry-method"></a>GetParentalCountry 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

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

 

 




