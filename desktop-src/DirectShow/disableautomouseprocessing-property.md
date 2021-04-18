---
description: DisableAutoMouseProcessing 屬性會啟用或停用 MSWebDVD 物件的滑鼠處理功能。
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: DisableAutoMouseProcessing 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467476"
---
# <a name="disableautomouseprocessing-property"></a>DisableAutoMouseProcessing 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`DisableAutoMouseProcessing`屬性會啟用或停用 **MSWebDVD** 物件的滑鼠處理功能。

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>傳回值

傳回布林值，指出是否要停用預設的滑鼠處理。

## <a name="remarks"></a>備註

這個屬性是讀取/寫入，預設值是 false。 依預設， **MSWebDVD** 物件會自動處理 DVD 螢幕功能表上的滑鼠動作;使用者可以反白顯示並啟用功能表按鈕，而不需要由應用程式進行特殊程式設計。 應用程式可以將這個屬性設定為 **true**，以關閉這個預設的滑鼠處理功能。 當自動關閉滑鼠處理功能時，應用程式必須使用各種按鈕相關的方法和屬性，來處理螢幕功能表上的滑鼠移動和滑鼠點擊。 此外，應用程式也可以使用按鈕相關的方法來覆寫自動滑鼠處理，即使當 `DisableAutoMouseProcessing` 設定為 **false** 時也一樣。

 

 



