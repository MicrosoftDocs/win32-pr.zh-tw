---
title: quality 命令
description: Quality 命令會定義音訊、影片或靜止影像資料壓縮的自訂品質層級。 數位影片裝置辨識此命令。
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- 品質命令 Windows 多媒體
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50f019b0e89f21d792f75c13e6c8e755486009d38d242878fec3121333fb9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372323"
---
# <a name="quality-command"></a>quality 命令

Quality 命令會定義音訊、影片或靜止影像資料壓縮的自訂品質層級。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*
</dt> <dd>

下列一或多個旗標。  (必須有三個旗標「音訊」、「仍」和「影片」的其中一個。 ) 



| 值                 | 意義                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 演算法 *演算法* | 將品質層級與指定的 *演算法* 產生關聯。 裝置必須支援此 *演算法* ，且必須與使用的「音訊」、「仍」或「影片」旗標相容。 如果省略，則會使用目前的演算法。 |
| 音訊 *名稱*          | 指出此命令指定以 *名稱* 識別的「音訊」品質層級。                                                                                                                                                   |
| 對話                | 要求裝置顯示對話方塊。 此對話方塊具有演算法特定欄位，這些欄位會由裝置在內部使用，以建立描述特定品質層級的結構。                                    |
| 句 *柄*       | 指定結構的 *控制碼* ，其中包含描述特定品質層級的演算法特定資料。 這個控制碼所參考的資料結構是裝置特定的。                                         |
| 仍然是 *名稱*          | 表示命令指定以名稱識別的「仍」品質層級 *。*                                                                                                                                                     |
| 影片 *名稱*          | 表示命令指定以 *名稱* 識別的「影片」品質層級。                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

此命令會定義品質層級的字串名稱，然後以 [setvideo](setvideo.md) 的「品質」、setvideo 「仍品質」或 [setaudio](setaudio.md) 「品質」命令來建立，以將其建立為目前的影片、靜止或音訊壓縮品質層級。

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

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

