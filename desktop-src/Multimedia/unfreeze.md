---
title: 解除凍結命令
description: 當凍結命令停用 reenables 時，[解除凍結] 命令會將影片捕獲到框架緩衝區。 數位影片、VCR 和影片重迭裝置會辨識此命令。
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- 將 Windows 多媒體的命令解除凍結
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fe45b1346872483a4012c5f5d161dcd61020c64349fee254ae4bf337b4be8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370808"
---
# <a name="unfreeze-command"></a>解除凍結命令

當 [凍結](freeze.md) 命令停用 reenables 時，[解除凍結] 命令會將影片捕獲到框架緩衝區。 數位影片、VCR 和影片重迭裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*
</dt> <dd>

用來重新啟用框架緩衝區取得影片的旗標。 下表列出可辨識 **解除凍結** 命令的裝置類型，以及每種類型所使用的旗標。



| 值        | 意義        |
|--------------|----------------|
| digitalvideo | 在 *矩形* |
| overlay      | 在 *矩形* |
| 錄影機          | 輸入輸出   |



 

下表列出可在 **lpszUnfreeze** 參數中指定的旗標，以及它們的意義。



| 值          | 意義                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在 *矩形* | 指定將重新啟用影片的區域。 矩形相對於影片緩衝區原點，並指定為 *X1 Y1 X2 Y2*。 座標 *X1 Y1* 指定矩形的左上角，而座標 *X2 Y2* 指定寬度和高度。 |
| input          | 解除凍結輸入影像。                                                                                                                                                                                                                                                                  |
| output         | 解除凍結輸出影像。 如果未提供 "input" 和 "output"，則會假設為 "output"。                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="examples"></a>範例

下列命令會 unfreezes 影片緩衝區的區域。

``` syntax
unfreeze vboard at 10 20 90 165
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
</dt> <dt>

[凍結](freeze.md)
</dt> </dl>

 

