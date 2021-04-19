---
description: GetDVDTextNumberOfStrings 方法會抓取指定語言可用的文字字串數目。
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: GetDVDTextNumberOfStrings 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970702"
---
# <a name="getdvdtextnumberofstrings-method"></a>GetDVDTextNumberOfStrings 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會抓取 `GetDVDTextNumberOfStrings` 指定語言可用的文字字串數目。

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

將語言指定為整數。 值的範圍必須介於零到1之間，且小於 [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md)傳回的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數值，指定光碟在指定的語言中包含多少個字串。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSWebDVD 物件](mswebdvd-object.md)
</dt> </dl>

 

 



