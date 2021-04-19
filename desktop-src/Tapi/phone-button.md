---
description: 傳送 TAPI 電話 \_ 按鈕訊息以通知應用程式，如果偵測到按鈕按下本機電話，則會啟用按鈕的按下監視。
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: 'PHONE_BUTTON 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997708"
---
# <a name="phone_button-message"></a>電話 \_ 按鈕訊息

傳送 TAPI **電話 \_ 按鈕** 訊息以通知應用程式，如果偵測到按鈕按下本機電話，則會啟用按鈕的按下監視。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPhone* 
</dt> <dd>

手機裝置的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟手機裝置時提供的應用程式回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

已按下按鈕的按鈕/燈泡識別碼。 請注意，按鈕識別碼0到11一律是鍵台按鈕，' 0 ' 是按鈕識別碼零，' 1 ' 是按鈕識別碼 1 (依此類推，透過按鈕識別碼 9) ，以及 ' ' 是按鈕識別碼 \* 10，而 ' \# ' 是按鈕識別碼11。 使用 [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) 和 [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)時，可以取得有關按鈕識別碼的其他資訊。

</dd> <dt>

*dwParam2* 
</dt> <dd>

按鈕的按鈕模式。 此參數會使用其中一個 [**PHONEBUTTONMODE \_ 常數**](phonebuttonmode--constants.md)。

</dd> <dt>

*dwParam3* 
</dt> <dd>

指定這是按鈕關閉事件或按鈕的事件。 此參數會使用其中一個 [**PHONEBUTTONSTATE \_ 常數**](phonebuttonstate--constants.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

每當按鈕變更狀態時，就會傳送 **電話 \_ 按鈕** 訊息。 應用程式可保證每個按鈕關閉事件最後都會傳送對應的按鈕 up 事件。 無法偵測實際按鈕的服務提供者，必須在每個按鈕按下按鈕之後，立即產生按鈕的訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




