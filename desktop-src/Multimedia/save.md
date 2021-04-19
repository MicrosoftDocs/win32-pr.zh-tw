---
title: 儲存命令
description: Save 命令會儲存 MCI 檔案。 影片-重迭和波形-音訊裝置會辨識此命令。 雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不支援。
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- 儲存命令 Windows 多媒體
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966490"
---
# <a name="save-command"></a>儲存命令

Save 命令會儲存 MCI 檔案。 影片-重迭和波形-音訊裝置會辨識此命令。 雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不支援。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*
</dt> <dd>

旗標，指定要儲存的檔案名，以及選擇性地修改儲存作業的其他旗標。 下表列出可辨識 **儲存** 命令的裝置類型，以及每種類型所使用的旗標。



| 值        | 意義              | 意義               |
|--------------|----------------------|-----------------------|
| digitalvideo | 在 *矩形* 中中止 | *檔案名* keepreserve |
| overlay      | 在 *矩形*       | *filename*            |
| 排序器    | *filename*           |                       |
| waveaudio    | *filename*           |                       |



 

下表列出可在 **lpszFilename** 參數中指定的旗標，以及它們的意義。



| 值          | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abort          | 停止進行中的 **儲存** 作業。 如果使用的話，這必須是唯一的專案。                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 在 *矩形* | 指定相對於框架緩衝區來源的矩形。 *矩形* 會指定為 *X1 Y1 X2 Y2*。 座標 *X1 Y1* 指定左上角，而座標 *X2 Y2* 指定寬度和高度。若為數位視訊裝置，則會使用 [capture](capture.md) 命令來捕獲框架緩衝區的內容。<br/>                                                                                                                                               |
| *filename*     | 指定要指派給資料檔案的檔案名。 如果未指定路徑，則會將檔案放在磁片上，並放在先前在明確或隱含 [保留](reserve.md) 命令上指定的目錄中。 如果尚未發出 **保留** ，則預設磁片磁碟機和目錄是與應用程式工作相關聯的磁片磁碟機和目錄。 如果指定路徑，則裝置可能會要求它位於明確或隱含 **保留** 所指定的磁片磁碟機上。 此為必要旗標。 |
| keepreserve    | 指定從原始 **保留** 命令剩餘未使用的磁碟空間未解除配置。                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

如果裝置是使用「新的」裝置識別碼來開啟，則需要 *filename* 變數。

## <a name="examples"></a>範例

下列命令會將整個影片緩衝區儲存至名為 VCAPFILE 的檔案。Tga。

``` syntax
save vboard c:\vcap\vcapfile.tga
```

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

[捕獲](capture.md)
</dt> <dt>

[儲備](reserve.md)
</dt> </dl>

 

