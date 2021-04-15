---
description: '>colorkey 屬性會設定或抓取隱藏式輔助字幕中使用的色彩索引鍵。'
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: '>colorkey 屬性'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467556"
---
# <a name="colorkey-property"></a>>colorkey 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`ColorKey`屬性會設定或抓取隱藏式輔助字幕中使用的色彩索引鍵。

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>傳回值

傳回整數值，表示用來做為封閉標題文字之透明背景的色彩。 256色彩中的預設值為洋紅，而在任何其他色彩深度中為非黑色。

## <a name="remarks"></a>備註

這是可讀寫的屬性。 這個屬性只適用于已隱藏的標題（如果有的話），而不會套用至子圖片資料流程。

 

 



