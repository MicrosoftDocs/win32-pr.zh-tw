---
description: GetTitleParentalLevels 方法會為指定的標題抓取家長管理層級。
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: GetTitleParentalLevels 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385706"
---
# <a name="gettitleparentallevels-method"></a>GetTitleParentalLevels 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`GetTitleParentalLevels`方法會針對指定的標題抓取家長管理層級。

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

將標題指定為整數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數值，其個別位表示在指定的標題中設定 (>PROCMONTRACE.PML) 的家長管理層級。

## <a name="remarks"></a>備註

標題可能有章節或更短的區段，其 >PROCMONTRACE.PML 與標題的整體 >PROCMONTRACE.PML 不同。 您可以使用這個方法來判斷播放指定的標題時，將會遇到的所有 PMLs。 傳回的整數是一組位旗標，定義如下表所示。 在 *iLevels* 和每個可能的值上執行位 and 運算。 如果作業傳回 **true**，表示會在此標題的某個時間點遇到 >procmontrace.pml。



| 值  | 描述          |
|--------|----------------------|
| 0x100  | DVD 父母層級1 |
| 0x200  | DVD 父母層級2 |
| 0x400  | DVD 家長監護層級3 |
| 0x800  | DVD 家長監護層級4 |
| 0x1000 | DVD 父母層級5 |
| 0x2000 | DVD 父母層級6 |
| 0x4000 | DVD 父母層級7 |
| 0x8000 | DVD 父母層級8 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 



