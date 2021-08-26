---
title: WM/InitialKey 屬性
description: WM/InitialKey 屬性是音樂的初始金鑰。
ms.assetid: 1458f1a2-3d46-4491-8b89-731276d7c024
keywords:
- WM/InitialKey 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/InitialKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3d5cb7576f7dc4c4c6a65a80c09222c30a3312e54230535bd64494a4eeae4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000998"
---
# <a name="wminitialkey-attribute"></a>WM/InitialKey 屬性

**WM/InitialKey** 屬性是音樂的初始金鑰。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMInitialKey。

**InitialKey** 是此屬性的別名。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





