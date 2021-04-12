---
description: DefaultSubpictureLanguageExt 屬性會抓取預設的 DVD 子圖片語言延伸模組。
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: DefaultSubpictureLanguageExt 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509848"
---
# <a name="defaultsubpicturelanguageext-property"></a>DefaultSubpictureLanguageExt 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `DefaultSubpictureLanguageExt` 預設的 DVD 子圖片語言延伸模組。

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a>傳回值

傳回整數值，指出預設的 DVD 子圖片語言延伸模組。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 下表顯示可能的值。



| 值 | 描述                    |
|-------|--------------------------------|
| 0     | 未指定擴充功能        |
| 1     | 一般字幕                |
| 2     | 大標題                   |
| 3     | 子女的標題            |
| 5     | 一般隱藏式輔助字幕         |
| 6     | 大型隱藏式輔助字幕            |
| 7     | 兒童隱藏式輔助字幕     |
| 9     | Forced                         |
| 13    | 一般導演的留言     |
| 14    | 大型總監的評論        |
| 15    | 子女的 Director's 批註 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SelectDefaultSubpictureLanguage**](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



