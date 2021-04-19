---
title: IWMPControls2 (VB 和 C) 介面 (Wmp.h)
description: 提供補充 IWMPControls 介面的方法。
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB 和 C ) 介面 Windows Media Player
- IWMPControls2 (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989824"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>IWMPControls2 (VB 和 c # ) 介面

提供補充 [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) 介面的方法。

## <a name="members"></a>成員

**IWMPControls2 (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMPControls2 (VB 和 c # )** 介面都有這些方法。



| 方法                                                           | 描述                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**步**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | 將目前的影片媒體專案移至下一個畫面格，或移至上一個畫面格，並凍結播放。<br/> |



 

下列範例程式碼顯示如何存取 [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) 介面。 範例程式碼會將 [**AxWindowsMediaPlayer Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)屬性傳回的 [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)值轉換成 **IWMPControls2** 值。

若為 **c #**：


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



針對 **VB**：


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPControls 介面 (VB 和 c # )**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls3 介面 (VB 和 c # )**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





