---
description: 當重迭表面已移動或調整大小，或其色彩索引鍵已變更時，就會傳送 UpdateOverlay 事件。
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: 'UpdateOverlay (Ddraw) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205b4ca002ec06862b006dc3e3b6facec2f5cb7f0ffb92f3e5a65bc2bb0a161c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650820"
---
# <a name="updateoverlay"></a>UpdateOverlay

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

當重迭表面已移動或調整大小，或其色彩索引鍵已變更時，就會傳送 **UpdateOverlay** 事件。

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>備註

應用程式永遠不會擔心調整大小或移動的重迭表面。 這是在內部處理。 但是，當顏色按鍵變更時，也會傳送此事件。 這表示，如果應用程式將 MSWebDVD 裝載為無視窗控制項，並在全螢幕模式下的影片表面上顯示浮動按鈕，則應該取得 **>colorkey** 屬性的新值，讓它可以正確地繪製按鈕，以回應此事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Ddraw。h</dt> </dl> |



 

 




