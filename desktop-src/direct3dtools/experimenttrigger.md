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
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846212"
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

 

 



