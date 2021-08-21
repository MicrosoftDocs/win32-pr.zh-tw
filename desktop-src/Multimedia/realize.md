---
title: 實現命令
description: 「實現」命令會指示裝置在顯示的視窗中，選取並實現其調色板的顯示內容。 數位影片裝置辨識此命令。
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- 實現命令 Windows 多媒體
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0aba1e610f4636c7dbfb71fbc959d9b4b8496cc23e91a97100ef6edce133b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371433"
---
# <a name="realize-command"></a>實現命令

「實現」命令會指示裝置在顯示的視窗中，選取並實現其調色板的顯示內容。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*
</dt> <dd>

下列其中一個旗標。



| 值      | 意義                                                                   |
|------------|---------------------------------------------------------------------------|
| 背景資訊 | 將調色板視為背景調色板。                             |
| 正常     | 瞭解最上層視窗的調色板。 這是預設值。 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 若為數位視訊裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

只有當您的應用程式使用視窗控制碼，並收到 **wm \_ QUERYNEWPALLETTE** 或 **WM \_ PALETTECHANGED** 訊息時，才能使用此命令。

## <a name="examples"></a>範例

下列命令會告知 "myvideo" 裝置，以實現其調色板。

``` syntax
realize myvideo normal
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> </dl>

 

