---
title: 天棚區段
description: 天棚區段
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Windows Media Player行動外觀、字幕
- 外觀、字幕
- 建立外觀、天棚區段
- 撰寫面板的程式碼，天棚區段
- 外觀、字幕區段中的字幕
- 外觀定義檔，天棚區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ddb53edd3f1efbbcbc5491604fd4022673b1234038770fcf44cd29ef4f3aca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123438"
---
# <a name="marquee-section"></a>天棚區段

[字幕] 區段包含 [字幕] 文字方塊的相關資訊，此文字方塊將會顯示滾動文字：


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



這會顯示目前媒體專案的標題和作者，雖然您可以在字幕中顯示任何文字類型。 例如，您也可以在字幕中包含檔案名、狀態和播放清單。

> [!Note]  
> 若要維持與 Windows Media Player 10 行動裝置版 Windows Media Player mobile 的相容性，在面板定義檔中使用 "Marquis" 仍會被視為有效。

 

如需 [字幕] 區段的詳細資訊，請參閱面板參考中的 [[字幕]](marquee.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**撰寫程式碼**](writing-the-code.md)
</dt> </dl>

 

 




