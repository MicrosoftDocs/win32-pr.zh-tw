---
title: D1104 可能的洩漏
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Factory 已釋放，但從它建立的介面仍在運作中。 雖然在釋放 factory 之後釋放資源是有效的，但這種情況可能表示記憶體流失。
keywords:
- D1104 可能的洩漏 Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548673"
---
# <a name="d1104-possible-leak"></a>D1104：可能的洩漏

已釋放 factory 處理站， \[  \] 但 \[  \] 從它建立的介面介面仍在運作中。 雖然在釋放 factory 之後釋放資源是有效的，但這種情況可能表示記憶體流失。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*廠*
</dt> <dd>

已釋放的 factory 位址。

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*介面*
</dt> <dd>

在 *factory* 上建立的介面位址。

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| 錯誤層級 | 資訊 |



 

## <a name="possible-causes"></a>可能的原因

Factory 已釋放，但從它建立的介面仍在運作中。

 

 




