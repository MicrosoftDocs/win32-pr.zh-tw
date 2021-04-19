---
description: LINETERMMODE \_ 位旗標常數描述可路由傳送至終端機裝置的電話線路上不同類型的事件。
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: 'LINETERMMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998770"
---
# <a name="linetermmode_-constants"></a>LINETERMMODE \_ 常數

**LINETERMMODE \_** 位旗標常數描述可路由傳送至終端機裝置的電話線路上不同類型的事件。

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE \_ 按鈕**
</dt> <dd> <dl> <dt>



這些是從終端機傳送至該行的按鍵事件。


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE \_ 顯示**
</dt> <dd> <dl> <dt>



這會顯示從該行傳送到終端機的資訊。


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**
</dt> <dd> <dl> <dt>



這些是從終端機傳送至該行的 hookswitch 事件。


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE \_ 燈**
</dt> <dd> <dl> <dt>



這些是從該行傳送到終端機的燈光事件。


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**
</dt> <dd> <dl> <dt>



這是與線條和終端機上的呼叫相關聯的雙向媒體資料流程。 當呼叫之媒體資料流程的單向通道的路由無法獨立控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**
</dt> <dd> <dl> <dt>



這是從線條到與線路上的呼叫相關聯的終端機的單向媒體資料流程。 當呼叫之媒體資料流程的單向通道的路由可以獨立控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**
</dt> <dd> <dl> <dt>



這是從終端機到與該行通話相關聯之線條的單向媒體資料流程。 當呼叫之媒體資料流程的單向通道的路由可以獨立控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE \_ 響鈴**
</dt> <dd> <dl> <dt>



這是從交換器傳送到終端機的響鈴控制資訊。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

這些常數描述可直接線上路裝置與終端機裝置 (（例如電話組) ）之間路由的控制項和資訊資料流程的類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




