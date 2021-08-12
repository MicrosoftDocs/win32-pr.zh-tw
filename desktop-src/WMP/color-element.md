---
title: Color 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |Color 元素
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Color 元素 Windows Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8576f94c2d1aa88608f8f40cbfe32c2d1dc315e0e4578ca6554fa5fcde82c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580753"
---
# <a name="color-element"></a>Color 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

Color 元素會指定線上商店導覽按鈕、按鈕文字和功能工作列的背景色彩。

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (必要) 
</dt> <dd>

十六進位 RGB 色彩值。 指定按鈕與工作列的背景色彩。

</dd> <dt>

<span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (必要) 
</dt> <dd>

十六進位 RGB 色彩值。 指定按鈕文字的色彩。

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

**MediaPlayer** 的預設值為 \# 7C9AD6。 **MediaPlayerText** 的預設值為 \# FFFFFF。

請務必使用可讓使用者更容易閱讀按鈕文字的色彩。 例如，您應該避免使用淺色按鈕的白色按鈕文字。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





