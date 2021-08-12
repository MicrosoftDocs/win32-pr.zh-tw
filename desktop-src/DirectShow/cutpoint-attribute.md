---
description: Cutpoint 屬性會指定當轉換轉譯為剪下時，轉換會從某個來源減少到下一個來源。 值相對於轉換開始。
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: cutpoint 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7332d3ef1b608b192b18e0d32bc99bce547058754950847e0a9767eb500a1553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654589"
---
# <a name="cutpoint-attribute"></a>cutpoint 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

當轉換轉譯 `cutpoint` 為剪下時，屬性會指定當轉換從某個來源減少到下一個來源時。 值相對於轉換開始。

## <a name="possible-values"></a>可能的值

必須是格式為 *hh： mm： ss* 格式的字串，其中 *hh* = hours， *mm* = 分鐘， *ss* = 秒，而 *ff* = 秒數的分數。 範例：1：04：30.512。 您可以省略前置單位。 例如，3:00 (三分鐘) 和 45 (45 秒) 都有效。

## <a name="applies-to"></a>套用至

[**過渡**](transition-element.md)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



