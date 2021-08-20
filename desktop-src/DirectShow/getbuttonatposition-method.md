---
description: GetButtonAtPosition 方法會在指定的座標處抓取按鈕的數目，而不需要選取或啟用它。
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: GetButtonAtPosition 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ad30e3cc9bb9b3f93d731c19f4418d8e567a0cb80e63832dfe27b8c4553921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000270"
---
# <a name="getbuttonatposition-method"></a>GetButtonAtPosition 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`GetButtonAtPosition`方法會在指定的座標處抓取按鈕的數目，而不選取或啟用它。

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

將滑鼠指標的 x 座標指定為整數。

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

將滑鼠指標的 y 座標指定為整數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數值，指定指定位置的按鈕（如果有的話）。

## <a name="remarks"></a>備註

如果指定的座標沒有任何按鈕，這個方法會傳回零。 將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



