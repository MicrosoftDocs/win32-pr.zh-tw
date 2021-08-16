---
description: PHONESTATUSFLAGS \_ 位旗標常數描述各種電話裝置狀態資訊。
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: 'PHONESTATUSFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b42f8e13adfae54c56e44244d04b3961216edb87e29730fec6f689f315380a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060646"
---
# <a name="phonestatusflags_-constants"></a>PHONESTATUSFLAGS \_ 常數

**PHONESTATUSFLAGS \_** 位旗標常數描述各種電話裝置狀態資訊。

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ 已連線**
</dt> <dd> <dl> <dt>



指定電話目前是否已連接到 TAPI。 如果已連接 **則為 TRUE** ，否則為 **FALSE** 。


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS 已 \_ 暫止**
</dt> <dd> <dl> <dt>



指定是否暫停 TAPI 的電話裝置操作。 如果已暫止，**則為 TRUE** ，否則為 **FALSE** 。 當交換器想要以無法容忍應用程式干擾的方式來操作電話時，可以暫時暫停應用程式使用的電話裝置。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




