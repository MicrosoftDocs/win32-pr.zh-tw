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
ms.openlocfilehash: b3c8b49256b3e7009985e9acf6d2b581e2fe436e50325c26f1f7de59cb3b0b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075562"
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

 

 




