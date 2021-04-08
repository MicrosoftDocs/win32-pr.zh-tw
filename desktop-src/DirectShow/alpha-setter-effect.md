---
description: Alpha Setter 效果
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Alpha Setter 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687863"
---
# <a name="alpha-setter-effect"></a>Alpha Setter 效果

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

Alpha Setter 效果會設定影片影像上的 Alpha 位。

類別識別碼 (CLSID) ： {506D89AE-909A-44f7-9444-ABD575896E35}

CLSID 變數名稱： CLSID \_ DxtAlphaSetter

易記名稱： "DxtAlphaSetter"

### <a name="properties"></a>屬性



| 屬性  | 類型   | 預設 | 描述                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alpha     | BYTE   | -1      | 設定整個影像的 Alpha。                        |
| AlphaRamp | double | -1.0    | 將 Alpha 設定為原始 Alpha 值的百分比。 |



 

## <a name="remarks"></a>備註

會忽略具有負值的屬性。 只有一個屬性可以有非負數值。 Alpha 屬性為影像中的每個圖元指定常數 Alpha 值。 這個屬性會覆寫原始影像中的 Alpha 值。 AlphaRamp 屬性會將每個圖元的 Alpha 值指定為圖元原始值的百分比，從0.0 到1.0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Alpha 混色](alpha-blending.md)
</dt> </dl>

 

 



