---
title: 複製命令
description: Copy 命令會將資料複製到剪貼簿。 數位影片裝置辨識此命令。
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- 複製命令 Windows 多媒體
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3d103aae14b9dc13bb0d7d210d0412db993210bc788fa7fedd1a48a7216d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144781"
---
# <a name="copy-command"></a>複製命令

Copy 命令會將資料複製到剪貼簿。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
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

下列其中一個識別要複製之專案的旗標。



| 值                 | 意義                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在 *矩形*        | 指定將複製的每個框架的部分。 如果省略，則預設設定為整個框架。                                                                                                                             |
| 音訊串流 *串流* | 指定工作區中受命令影響的音訊串流。 如果您使用此旗標，而且也想要複製影片，您也必須使用「影片串流」旗標。  (如果未指定任何旗標，則會複製所有音訊和影片串流。 )  |
| 從 *位置*       | 指定複製的範圍開始。 如果省略，則預設設定為目前的位置。                                                                                                                                         |
| *定位*         | 指定複製之範圍的結尾。 複製的音訊和影片資料是此位置專屬的。 如果省略，則預設設定為工作區的結尾。                                                                       |
| 影片串流 *串流* | 在工作區中指定受命令影響的影片串流。 如果您使用此旗標，而且也想要複製音訊，您也必須使用「音訊串流」旗標。  (如果未指定任何旗標，則會複製所有音訊和影片串流。 )  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

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

 

