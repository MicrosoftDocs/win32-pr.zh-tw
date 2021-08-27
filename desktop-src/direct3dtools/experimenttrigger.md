---
description: 代表實驗觸發程式資訊。
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ExperimentTrigger 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 189adeb91467ec25eedd2001922290e1521d8ad69cb0f6e7c1095e608f1ec593
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067568"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger 結構

代表實驗觸發程式資訊。

## <a name="syntax"></a>語法


```C++
} ExperimentTrigger;
```

## <a name="members"></a>成員

**type**  
觸發 (capture) 的實驗類型。

**key**  
當 type 等於 EXPERIMENTTRIGGERTYPE：： KEY 時，用來觸發 capture 的索引鍵。

**frameNumber**  
當 type 等於 EXPERIMENTTRIGGERTYPE：： FRAMENUMBER 時，將會觸發 capture 的框架編號。

**captureCount**  
要捕捉的連續框架數目。

**actionIID**  
動作事件的識別碼 (螢幕擷取畫面、框架捕獲等) 。

**actionPlayload**  
動作事件裝載的指標。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



