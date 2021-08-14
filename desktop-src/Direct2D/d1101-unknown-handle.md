---
title: D1101 未知的控制碼
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: 未由此 DLL 配置的介面傳遞給它。
keywords:
- D1101 未知的控制碼 Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 37e84b9e5117732784267374ad9e6618e60d3b4020a6d23863b069b3b8233aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160999"
---
# <a name="d1101-unknown-handle"></a>D1101：未知的控制碼

未由此 DLL 配置的介面 \[ *介面* \] 傳遞給它。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*介面*
</dt> <dd>

介面的位址。

</dd> </dl> 




 

## <a name="possible-causes"></a>可能的原因

不正確資源使用量。 在 Direct2D 之外建立的資源會與 Direct2D factory 搭配使用，或在一個 factory 上建立的資源會與另一個 factory 建立的資源搭配使用。

 

 




