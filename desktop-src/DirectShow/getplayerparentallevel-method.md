---
description: GetPlayerParentalLevel 會捕獲 MSWebDVD 物件中所設定的家長管理層級。
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: GetPlayerParentalLevel 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108500"
---
# <a name="getplayerparentallevel-method"></a>GetPlayerParentalLevel 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

會抓取 `GetPlayerParentalLevel` **MSWebDVD** 物件中設定的家長管理層級。

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>傳回值

傳回整數值，這個值會指定 DVD 導覽中的目前家長層級，如果停用家長管理，則傳回-1。

## <a name="remarks"></a>備註

播放機應用程式負責強制執行家長監護控制項。 Media player 家長監護是由應用程式所設定的值，其可用來指出目前使用者可查看的最高家長能等級。 當 DVD 導覽器遇到新的家長監護時，請使用這個方法來判斷新的層級是否大於應用程式透過 [**SelectParentalLevel**](selectparentallevel-method.md)所設定的層級。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



