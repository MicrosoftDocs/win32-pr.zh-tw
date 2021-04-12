---
description: CurrentButton 屬性會抓取選取的功能表按鈕數目。
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: CurrentButton 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317720"
---
# <a name="currentbutton-property"></a>CurrentButton 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

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

 

 



