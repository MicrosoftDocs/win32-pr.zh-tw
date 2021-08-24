---
description: 影像意圖常數會指定影像所代表的資料類型。
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: '影像意圖常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 78130128a26057ed521512dd21acc5a1bd7e98c47ed689eaabc250a972c2a003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814118"
---
# <a name="image-intent-constants"></a>影像意圖常數

影像意圖常數會指定影像所代表的資料類型。 [ [**WIA \_ ip 的 \_ 當前 \_ 意圖**](-wia-wiaitempropscanneritem.md) 掃描器] 屬性會使用這些旗標。 若要提供意圖，請使用 OR 運算子結合預期的影像類型旗標與預期的大小/品質旗標。 WIA \_ 意圖「 \_ 無」不應與任何其他旗標合併。 請注意，影像不能同時為灰階和彩色。

以下是有效的影像意圖常數：



| 預定的影像類型旗標           | 描述                                  |
|-------------------------------------|----------------------------------------------|
| WIA \_ 意圖 \_ 無                   | 預設值。 請勿預設設定任何屬性。 |
| WIA \_ 意圖 \_ 影像 \_ 類型 \_ 色彩     | 色彩內容的預設屬性。         |
| WIA \_ 意圖 \_ 影像 \_ 類型 \_ 灰階 | 灰階內容的預設屬性。     |
| WIA \_ 意圖 \_ 影像 \_ 類型 \_ 文字      | 文字內容的預設屬性。          |
| WIA \_ 意圖 \_ 影像 \_ 類型 \_ 遮罩      | 所有影像類型旗標的遮罩。        |



 



| 預定的影像大小/品質旗標 | 描述                                  |
|-----------------------------------|----------------------------------------------|
| WIA \_ 意圖 \_ 最小化 \_ 大小       | 用來將影像大小降至最低的預設屬性。    |
| WIA \_ 意圖 \_ 最大化 \_ 品質    | 將影像品質最大化的預設屬性。 |
| WIA \_ 意圖 \_ 大小 \_ 遮罩           | 所有大小/品質旗標的遮罩。      |
| WIA \_ 意圖 \_ 最佳 \_ 預覽        | 指定最佳品質預覽。          |



 

下列清單顯示 C/c + + 常數名稱，後面接著以括弧括住的對應名稱（用於腳本處理）。 腳本名稱是來自 WiaIntent 列舉型別。 請注意，並非所有常數都可透過腳本來使用。



| 常數/值                                                                                                                                                                                                                                                                         | 描述                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WIA \_意圖 \_ 影像 \_ 類型 \_ 色彩**</dt> <dt>0x00000001</dt> </dl>             | 色彩內容的預設屬性。<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WIA \_意圖 \_ 影像 \_ 類型 \_ 灰階**</dt> <dt>0x00000002</dt> </dl> | 灰階內容的預設屬性。<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WIA \_意圖 \_ 影像 \_ 類型 \_ 文字**</dt> <dt>0x00000004</dt> </dl>                | 文字內容的預設屬性。<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WIA \_意圖 \_ 最小化 \_ 大小**</dt> <dt>0x00010000</dt> </dl>                       | 用來將影像大小降至最低的預設屬性。<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WIA \_意圖 \_ 最大化 \_ 品質**</dt> <dt>0x00020000</dt> </dl>              | 將影像品質最大化的預設屬性。<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WIA \_意圖 \_ 最適合 \_ 預覽**</dt> <dt>0x00040000</dt> </dl>                          | 指定最佳品質預覽。<br/>          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 




