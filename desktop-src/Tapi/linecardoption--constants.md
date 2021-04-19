---
description: LINECARDOPTION \_ 常數會定義 LINECARDENTRY 結構的 >dwoptions 成員所使用的值，這些值會在 lineGetTranslateCaps 所傳回之 LINETRANSLATECAPS 結構的一部分傳回。
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: 'LINECARDOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994909"
---
# <a name="linecardoption_-constants"></a>LINECARDOPTION \_ 常數

**LINECARDOPTION \_ 常數** 會定義 [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry)結構的 **>dwoptions** 成員所使用的值，這些值會在 [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)所傳回之 [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)結構的一部分傳回。 **LINECARDOPTION \_ 常數** t 具有下列值：

<dl> <dt>

<span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**\_隱藏 LINECARDOPTION**
</dt> <dd> <dl> <dt>



使用者已隱藏此電話卡。 撥號協助程式未顯示在可用電話卡的主要清單中，但會顯示在可從中複製撥號規則的卡片清單中。


</dt> </dl> </dd> <dt>

<span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ 預先定義**
</dt> <dd> <dl> <dt>



這張電話卡是 Microsoft 電話語音隨附的其中一個預先定義的電話卡定義。 無法使用撥號協助程式完全移除：如果使用者嘗試移除它，就會變成隱藏狀態。 如此一來，就可以繼續存取撥號規則。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

不可延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




