---
title: 剪下命令
description: 剪下的命令會從工作區中移除資料，並將資料複製到剪貼簿。 數位影片裝置辨識此命令。
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- 剪下命令 Windows 多媒體
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934883"
---
# <a name="cut-command"></a>剪下命令

剪下的命令會從工作區中移除資料，並將資料複製到剪貼簿。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

下列其中一個識別要剪下之專案的旗標。



| 值                 | 意義                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在 *矩形*        | 指定每個框架剪下的部分。 如果省略，則會預設為整個框架。 指定此專案時，不會刪除畫面格。 而是矩形內的區域會變成黑色。                                       |
| 音訊串流 *串流* | 指定工作區中受命令影響的音訊串流。 如果您使用此旗標，而且也想要剪下影片，您也必須使用「影片串流」旗標。  (如果未指定任何旗標，則會剪下所有音訊和影片串流。 )  |
| 從 *位置*       | 指定剪下的範圍開始。 如果省略，則會預設為目前的位置。                                                                                                                                                |
| *定位*         | 指定剪下的範圍結尾。 音訊和影片資料剪下是此位置專屬的。 如果省略，則會預設為工作區的結尾。                                                                                  |
| 影片串流 *串流* | 在工作區中指定受命令影響的影片串流。 如果您使用此旗標，而且也想要剪下音訊，您也必須使用「音訊串流」旗標。  (如果未指定任何旗標，則會剪下所有音訊和影片串流。 )  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

只有在明確儲存資料時，變更才會變成永久;不過，播放的行為就如同已移除資料一樣。

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
</dt> </dl>

 

