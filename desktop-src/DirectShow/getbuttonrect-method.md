---
description: GetButtonRect 方法會在視窗座標中，取得指定之按鈕的矩形。
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: GetButtonRect 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108524"
---
# <a name="getbuttonrect-method"></a>GetButtonRect 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`GetButtonRect`方法會在視窗座標中，取得指定之按鈕的矩形。

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*
</dt> <dd>

將按鈕編號指定為整數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回定義矩形的 [DVDRect](dvdrect-object.md) 物件。

## <a name="remarks"></a>備註

將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



