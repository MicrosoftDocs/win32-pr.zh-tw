---
title: capture 命令
description: Capture 命令會複製框架緩衝區的內容，並將其儲存在指定的檔案中。 數位影片裝置辨識此命令。
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- 捕捉命令 Windows 多媒體
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105918"
---
# <a name="capture-command"></a>capture 命令

Capture 命令會複製框架緩衝區的內容，並將其儲存在指定的檔案中。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*
</dt> <dd>

下列其中一個或多個旗標：



| 值          | 意義                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| as *路徑名稱*  | 指定所捕獲映射的目的地路徑和檔案名。 此為必要旗標。                                                                                                                                                                |
| 在 *矩形* | 指定框架緩衝區內裝置裁切並儲存至磁片的矩形區域。 如果省略，則裁剪的區域預設為此裝置實例先前 [放置](put.md) "source" 命令上指定或預設的矩形。 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

如果裝置目前現正播放運動影片，或執行其他需要大量資源的作業，此命令可能會失敗。 如果框架緩衝區正在即時更新，則更新會短暫暫停，以便捕獲完整的映射。 如果裝置暫停更新，可能會有視覺效果或聲音效果。 如果檔案格式、壓縮演算法和品質層級尚未設定，則會使用其預設值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> <dt>

[把](put.md)
</dt> </dl>

 

