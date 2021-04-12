---
description: ButtonsAvailable 屬性會抓取目前功能表上的總按鈕數目。
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: ButtonsAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385770"
---
# <a name="buttonsavailable-property"></a>ButtonsAvailable 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `ButtonsAvailable` 目前功能表上的總按鈕數目。

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>傳回值

傳回代表按鈕數目的整數值。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。

呼叫這個方法，以取得有效按鈕編號範圍的上限。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



