---
description: PHONELAMPMODE 位旗標常數描述電話燈可亮起的各種方式。
ms.assetid: 4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe
title: 'PHONELAMPMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8df5920df79e6fc59eb12bf1f517b4070e617d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984893"
---
# <a name="phonelampmode_-constants"></a>PHONELAMPMODE_ 常數

**PHONELAMPMODE_** 位旗標常數描述電話燈可亮起的各種方式。

<dl> <dt>

<span id="PHONELAMPMODE_DUMMY"></span><span id="phonelampmode_dummy"></span>**PHONELAMPMODE_DUMMY**
</dt> <dd> <dl> <dt>



此值可用來描述沒有對應燈泡的按鈕/燈泡位置。


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_BROKENFLUTTER"></span><span id="phonelampmode_brokenflutter"></span>**PHONELAMPMODE_BROKENFLUTTER**
</dt> <dd> <dl> <dt>



中斷的 flutter 是 flash 和 flutter 的迭加。


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLASH"></span><span id="phonelampmode_flash"></span>**PHONELAMPMODE_FLASH**
</dt> <dd> <dl> <dt>



Flash 表示開啟和關閉的速度很慢。


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLUTTER"></span><span id="phonelampmode_flutter"></span>**PHONELAMPMODE_FLUTTER**
</dt> <dd> <dl> <dt>



Flutter 表示快速開啟和關閉。


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_OFF"></span><span id="phonelampmode_off"></span>**PHONELAMPMODE_OFF**
</dt> <dd> <dl> <dt>



燈泡已關閉。


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_STEADY"></span><span id="phonelampmode_steady"></span>**PHONELAMPMODE_STEADY**
</dt> <dd> <dl> <dt>



穩定表示燈泡會持續發亮。


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_UNKNOWN"></span><span id="phonelampmode_unknown"></span>**PHONELAMPMODE_UNKNOWN**
</dt> <dd> <dl> <dt>



燈泡模式目前未知。


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_WINK"></span><span id="phonelampmode_wink"></span>**PHONELAMPMODE_WINK**
</dt> <dd> <dl> <dt>



瞬間表示正常的速率。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

在不同廠商的電話組中，確切的開啟和關閉步調可能不同，將大部分手機的實際燈泡照明模式對應到上列值應該很簡單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




