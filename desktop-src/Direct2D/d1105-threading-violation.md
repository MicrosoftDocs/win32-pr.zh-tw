---
title: D1105 執行緒違規
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: 從多個執行緒同時存取出租執行緒介面。
keywords:
- D1105 執行緒違規 Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 12e7321fd40437bc262439c6ddb319a0aa6dba145d05d3feebba2813c904bbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537968"
---
# <a name="d1105-threading-violation"></a>D1105：執行緒違規

\[  \] 從多個執行緒同時存取出租執行緒介面介面。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*介面*
</dt> <dd>

多個執行緒所存取的介面位址。

</dd> </dl> 




 

## <a name="possible-causes"></a>可能的原因

從兩個不同的執行緒使用相同單一執行緒處理站中的物件實例。

 

 




