---
title: 指標訊息旗標
description: 各種指標宏所使用的值 (查看宏) 。
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 70d329c6a48eb92f6f50ff49d5543c2aaf5cfc3ce9ef23b48290c7aa029eecf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602349"
---
# <a name="pointer-message-flags"></a>指標訊息旗標

各種指標宏所使用的值 (查看 [宏](macros.md)) 。

<dl> <dt>

<span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



表示新指標的抵達。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



指出此指標持續存在。 如果未設定此旗標，則表示指標具有左方偵測範圍。

只有當滑鼠停留指標離開偵測範圍時，才會設定這個旗標 (**POINTER_FLAG_UPDATE** 設定) ，或是當與視窗介面的指標離開偵測範圍 (**POINTER_FLAG_UP** 設定為) 時。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



指出此指標與數位板介面相同。 如果未設定此旗標，則會指出滑鼠停留指標。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



指出主要動作，類似于按下滑鼠左鍵。

當觸控指標與數位板介面聯繫時，會設定這個旗標。

當畫筆指標與數位板介面聯繫時，如果未按下任何按鈕，就會設定這個旗標。

當滑鼠左鍵關閉時，滑鼠指標會設定這個旗標。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



表示第二個動作，類似滑鼠向下按鈕。

觸控指標不會使用此旗標。

當畫筆指標與數位板介面一起使用時，會設定此旗標，並按下畫筆圓筒按鈕。

當滑鼠右鍵關閉時，滑鼠指標會設定這個旗標。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



類似滑鼠滾輪按鈕。

觸控指標不會使用此旗標。

畫筆指標不會使用此旗標。

當滑鼠滾輪按鈕關閉時，滑鼠指標會設定這個旗標。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



類似于第一個擴充的滑鼠 (XButton1) 按鈕。

觸控指標不會使用此旗標。

畫筆指標不會使用此旗標。

當第一個擴充的滑鼠 (XBUTTON1) 按鈕關閉時，滑鼠指標會設定這個旗標。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



類似于第二個擴充的滑鼠 (XButton2) 按鈕。

觸控指標不會使用此旗標。

畫筆指標不會使用此旗標。

當第二個擴充的滑鼠 (XBUTTON2) 按鈕關閉時，滑鼠指標會設定這個旗標。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



指出此指標已指定為主要指標。 主要指標是單一指標，可在非主要指標可用的動作之外執行動作。 例如，當主要指標與視窗的介面接觸時，它可能會將 WM_POINTERACTI加值稅E 訊息傳送給視窗，以提供啟動的機會。

主要指標是從系統上所有目前使用者的互動中識別 (滑鼠、觸控、畫筆等) 。 因此，主要指標可能不會與您的應用程式相關聯。 多點觸控互動中的第一個連絡人會設定為主要指標。 識別主要指標之後，必須先提起所有連絡人，才能將新的連絡人識別為主要指標。 針對不處理指標輸入的應用程式，只有主要指標的事件會升級為滑鼠事件。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



信賴度是來自來源裝置的建議，這是指指標是否代表預期或意外的互動，這與意外互動 (的 PT_TOUCH 指標（例如，與掌上的) 可以觸發輸入）特別相關。 此旗標的存在表示來源裝置有很高的信賴度，此輸入是預期互動的一部分。


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



指出指標以異常的方式脫離，例如當系統收到指標的無效輸入，或是具有作用中指標的裝置突然離開時。 如果接收輸入的應用程式是在執行這項作業的位置，則應該將互動視為未完成，並反轉任何相關指標的影響。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

XBUTTON1 和 XBUTTON2 是許多滑鼠裝置上使用的其他按鈕。 它們會傳回與標準滑鼠按鍵相同的資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常數](constants.md)
</dt> <dt>

[巨集](macros.md)
</dt> </dl>

 

 





