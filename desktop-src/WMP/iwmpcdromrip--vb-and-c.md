---
title: 'IWMPCdromRip (VB 和 C ) 介面 (h.264. h) '
description: 提供屬性和方法來管理從音訊 CD 複製或翻錄的追蹤。使用 IWMPCdromRip 介面來翻錄 CD，其效果與使用 Windows Media Player 使用者介面來將音樂翻錄的效果相同。
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- IWMPCdromRip (VB 和 C ) 介面 Windows Media Player
- IWMPCdromRip (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPCdromRip (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d069fd8bd727d6a2a380c2ef29ce7c086db88d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995747"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>IWMPCdromRip (VB 和 c # ) 介面

提供屬性和方法來管理從音訊 CD 複製或 *翻錄* 的曲目。

使用 **IWMPCdromRip** 介面來將 CD 翻錄，與使用 Windows Media Player 使用者介面來將音樂翻錄的效果相同。 已翻錄的內容會根據使用者的喜好設定自動新增至程式庫。 如需 CD 翻錄使用者喜好設定的詳細資訊，請參閱 Windows Media Player 說明中的「從 Cd 翻錄音樂」。

**IWMPCdromRip** 介面會公開下列屬性。

## <a name="members"></a>成員

**IWMPCdromRip (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPCdromRip (VB 和 c # )** 介面都有這些方法。



| 方法                                                                 | 描述                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | 將 CD 翻錄。<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | 停止 CD 翻錄進程。<br/> |



 

### <a name="properties"></a>屬性

**IWMPCdromRip (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                | 存取類型          | Description                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripProgress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | 唯讀<br/> | 取得完成百分比的 CD 翻錄進度。<br/>                                  |
| [**ripState**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | 唯讀<br/> | 取得列舉值，這個值表示目前的翻錄進程狀態。<br/> |



 

藉由轉換您要翻錄之 CD 的 **IWMPCdrom** 介面，來取得 **IWMPCdromRip** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**將 CD 翻錄**](ripping-a-cd.md)
</dt> </dl>

 

 





