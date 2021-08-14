---
description: PHONEBUTTONMODE \_ 位旗標常數描述按鈕類別。
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: 'PHONEBUTTONMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9424c23a9fe6497c657081dd9e197526dc5eb897ad773b1e03fb33c9f08113df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761300"
---
# <a name="phonebuttonmode_-constants"></a>PHONEBUTTONMODE \_ 常數

**PHONEBUTTONMODE \_** 位旗標常數描述按鈕類別。

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**PHONEBUTTONMODE \_ 呼叫**
</dt> <dd> <dl> <dt>



按鈕會指派給呼叫外觀。


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**PHONEBUTTONMODE \_ 顯示**
</dt> <dd> <dl> <dt>



按鈕是與手機顯示相關聯的「軟」按鈕。 電話組可以有零或多個顯示按鈕。


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE \_ 虛擬**
</dt> <dd> <dl> <dt>



此值可用來描述沒有對應按鈕但只有燈泡的按鈕/燈泡位置。


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**PHONEBUTTONMODE \_ 功能**
</dt> <dd> <dl> <dt>



此按鈕會指派給從交換器要求的功能，例如保存、會議和傳輸。


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**PHONEBUTTONMODE \_ 鍵台**
</dt> <dd> <dl> <dt>



按鈕是12鍵台按鈕的其中之一，0到9、' \* ' 和 ' \# '。


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ 本機**
</dt> <dd> <dl> <dt>



按鈕是區域的功能按鈕，例如靜音或音量控制。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

此列舉型別會在 [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) 資料結構中用來描述與電話按鈕相關聯的意義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




