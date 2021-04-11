---
description: Mlength 屬性會指定原始程式檔的持續時間。 此值必須是實際的持續時間，否則可能會發生轉譯錯誤。
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: mlength 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935604"
---
# <a name="mlength-attribute"></a>mlength 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`mlength`屬性指定原始程式檔的持續時間。 此值必須是實際的持續時間，否則可能會發生轉譯錯誤。

## <a name="applies-to"></a>套用至

[**clip**](clip-element.md)

## <a name="possible-values"></a>可能的值

必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。 範例：1：04：30.512。 您可以省略前置單位。 例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



