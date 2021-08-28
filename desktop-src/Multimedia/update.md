---
title: update 命令
description: Update 命令會將目前的框架重新繪製到指定的裝置內容 (DC) 。 數位影片裝置辨識此命令。
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- 更新命令 Windows 多媒體
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a5f4f185c16e0ba499e75ed9f445aaf87b9e346dbde9a7929035613f4744ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804698"
---
# <a name="update-command"></a>update 命令

Update 命令會將目前的框架重新繪製到指定的裝置內容 (DC) 。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*
</dt> <dd>

DC 的控制碼。 下表列出可辨識 **update** 命令的裝置類型，以及每種類型所使用的旗標。



| 值        | 意義                       | 意義         |
|--------------|-------------------------------|-----------------|
| digitalvideo | 在 *rect* 的 hdc *hdc* hdc *hdc* | 油漆 hdc *hdc* |



 

下表列出可在 **lpszHDC** 參數中指定的旗標，以及它們的意義。



| 值               | 意義                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| hdc *hdc*           | 指定要繪製之 DC 的控制碼。                                                               |
| *rect* 的 hdc *hdc* | 指定相對於用戶端矩形的裁剪矩形。                                     |
| 油漆 hdc *hdc*     | 當應用程式收到適用于 DC 的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時繪製 dc。 |



 

若要指定 DC 的控制碼，請使用字串 "hdc"，後面接著控制碼的 ASCII 標記法。 矩形會指定為 **X1 Y1 X2 Y2**。 座標 **X1 Y1** 指定矩形的左上角，而座標 **X2 Y2** 指定寬度和高度。

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 若為數位視訊裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="examples"></a>範例

下列命令會更新「電影」裝置所使用的整個顯示視窗。 數位203是從 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) 函式取得之 DC 的控制碼。

``` syntax
update movie hdc 203
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

 

