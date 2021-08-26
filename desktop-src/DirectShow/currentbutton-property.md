---
description: CurrentButton 屬性會抓取選取的功能表按鈕數目。
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: CurrentButton 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b246b77283a2632f2feac4c2b374075ef9d9a205bcb71813856b9847df21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053138"
---
# <a name="currentbutton-property"></a>CurrentButton 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `CurrentButton` 所選功能表按鈕的數目。

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a>傳回值

傳回代表按鈕的整數值。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



