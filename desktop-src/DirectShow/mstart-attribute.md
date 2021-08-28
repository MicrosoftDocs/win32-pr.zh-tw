---
description: Mstart 屬性會指定相對於原始媒體檔案的剪輯開始時間。
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: mstart 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c65ffcb7d3da41f3e1f1232e37a6f5786755980eb63a8bbc554bbe726f453e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050948"
---
# <a name="mstart-attribute"></a>mstart 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`mstart`屬性會指定相對於原始媒體檔案的剪輯開始時間。

## <a name="applies-to"></a>套用至

[**clip**](clip-element.md)

## <a name="possible-values"></a>可能的值

必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。 範例：1：04：30.512。 您可以省略前置單位。 例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



