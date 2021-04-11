---
description: Mstop 屬性會指定剪輯的停止時間（相對於原始媒體檔案）。
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: mstop 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108480"
---
# <a name="mstop-attribute"></a>mstop 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`mstop`屬性會指定相對於原始媒體檔案的剪輯停止時間。

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

 

 



