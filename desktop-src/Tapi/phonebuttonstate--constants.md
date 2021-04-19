---
description: PHONEBUTTONSTATE 位旗標常數描述按鈕的位置。
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: 'PHONEBUTTONSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001035"
---
# <a name="phonebuttonstate_-constants"></a>PHONEBUTTONSTATE_ 常數

**PHONEBUTTONSTATE_** 位旗標常數描述按鈕的位置。

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



按鈕處於「關閉」狀態 (按下) 。


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



指出服務提供者不知道按鈕的向上或向下狀態，而且未來將不會知道。  (TAPI 1.4 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



指出目前不知道按鈕的向上或向下狀態，但未來可能會變成已知狀態。  (TAPI 1.4 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



按鈕處於「up」狀態。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

為了回溯相容性，服務提供者必須負責檢查手機上的已協商 API 版本，並且不使用所協商版本不支援的 PHONEBUTTONSTATE_ 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




