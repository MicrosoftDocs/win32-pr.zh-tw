---
title: 設定。速率
description: '[速率] 屬性會指定或抓取影片媒體的目前播放速率。'
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- 設定. 速率 Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01936462593b8b27a8d45f2e3e4090b9cf242d79e1d9b1c2cda00c152bd41182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646398"
---
# <a name="settingsrate"></a>設定。速率

[ **速率** ] 屬性會指定或抓取影片媒體的目前播放速率。

## <a name="syntax"></a>Syntax

player. 設定速率

## <a name="possible-values"></a>可能的值

這個屬性是 (**雙精度**) 的讀/寫 **數位**，預設值為1.0。

## <a name="remarks"></a>備註

這個屬性會作為乘數值，讓您以更快或較慢的速率播放剪輯。 預設值1.0 表示撰寫的速度。 請注意，在低於0.5 或高於1.5 的速率中，音訊播放軌會變得很難理解。 播放速率2等於正常播放速度的兩倍。

Windows Media Player 將嘗試使用四種不同播放模式的最有效方式。 這些模式是流暢的影片播放，並維持音訊音調、不維護音訊、順暢的影片播放、無音訊的流暢影片播放，以及不含音訊的主要畫面格影片播放。 播放程式選擇的模式取決於許多因素，包括檔案類型和位置、作業系統、網路和伺服器。

其他考慮也適用于不同的媒體類型：

-   Windows媒體格式 (WMV) 和 ASF 檔案：此屬性的最佳值為1到10，或從1到10以進行反向播放。 從0.5 到1.0 或從-0.5 到-1.0 的值可能也適用于可以維持音訊音調的情況，例如，播放位於本機電腦上的檔案時。 允許絕對值大於10的值，但沒有什麼意義。
-   其他影片媒體類型：這個屬性的範圍可以從0到9。 不允許負數值。 小於1的值表示緩慢的移動。 允許超過9個值，但沒有什麼意義。

*控制項*。**fastForward** 方法會將 **速率** 的值變更為5.0，而 *控制項* 則變更。**fastReverse** 方法會將 **速率** 變更為5.0。

某些媒體類型的播放率無法改變。 使用 *設定*。**isAvailable** 方法，以判斷是否可以針對特定媒體專案指定這個屬性。

**Windows Media Player 10** 行動裝置版：此屬性只接受或傳回值-5.0、1.0 或5.0。

## <a name="examples"></a>範例

下列範例會建立 HTML SELECT 元素，讓使用者可以變更目前媒體的播放速度。 選取選項提供一般速度、半速度和雙速度的播放速率。 使用 ID = "Player" 建立 **player** 物件。


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FastForward**](controls-fastforward.md)
</dt> <dt>

[**FastReverse**](controls-fastreverse.md)
</dt> <dt>

[**設定物件**](settings-object.md)
</dt> <dt>

[**設定. isAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





