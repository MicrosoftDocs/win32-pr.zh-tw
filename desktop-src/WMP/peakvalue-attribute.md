---
title: PeakValue 屬性
description: PeakValue 屬性是16位的波幅值，表示尖峰磁片區層級。
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- PeakValue 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a661342b305155717f4f11336f540e1ae53524ff2d303a2ab790e2c73af7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573582"
---
# <a name="peakvalue-attribute"></a>PeakValue 屬性

**PeakValue** 屬性是16位的波幅值，表示尖峰磁片區層級。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

Windows Media Player 會在下列其中一個實例中設定此值：

-   完成檔案的翻錄之後。
-   當已啟用自動磁片區調節增強功能時，它會在播放檔 () 。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszPeakValue。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





