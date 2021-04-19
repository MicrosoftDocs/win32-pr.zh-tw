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
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "106994928"
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

 

 




