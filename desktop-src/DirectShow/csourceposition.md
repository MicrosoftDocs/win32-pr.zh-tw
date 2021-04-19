---
description: CSourcePosition 是一個抽象類別，可在來源篩選器上執行 IMediaPosition 介面。
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: CSourcePosition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991589"
---
# <a name="csourceposition-class"></a>CSourcePosition 類別

`CSourcePosition` 是在來源篩選器上執行 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面的抽象類別。

這個類別已經過時。 如果來源篩選準則是可搜尋的，則應該公開 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面，而不是 **IMediaPosition**。 您可以針對此用途使用 [**CSourceSeeking**](csourceseeking.md) 基類。

 

 



