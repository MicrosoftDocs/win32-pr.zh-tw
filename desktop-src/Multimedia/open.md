---
title: '開啟命令 (Corecrt \_) '
description: Open 命令會初始化裝置。 所有 MCI 裝置都會辨識此命令。
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- 開啟命令 Windows 多媒體
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d2e585a44c19093fa0d20ab4870f579c67cd568c3a693523242b84910e6589d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373267"
---
# <a name="open-command"></a>開啟命令

Open 命令會初始化裝置。 所有 MCI 裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*
</dt> <dd>

MCI 裝置或設備磁碟機的識別碼。 這可以是在登錄中指定的裝置名稱 (或 SYSTEM.INI 檔) 或設備磁碟機的檔案名。 如果您指定設備磁碟機的檔案名，則可以選擇性地包含。WINSPOOL.DRV 延伸模組，但您不應該包含檔案的路徑。

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

識別要初始化之內容的旗標。 下表列出可辨識 **開啟** 命令的裝置類型，以及每種類型所使用的旗標。



| 值        | 意義                                                        | 意義                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | 別名 *裝置 \_ 別名* 可共用                                  | 類型 *裝置 \_ 類型*                                                             |
| digitalvideo | 別名 *裝置 \_ aliaselementname* nostatic 父 *hwnd* 可共用 | 樣式子樣式重迭樣式的快顯樣式 *樣式 \_ 類型* 類型 *裝置 \_ 類型* |
| overlay      | 別名 *裝置 \_ 別名* 父系 *hwnd* 可共用樣式子系         | 樣式重迭樣式的快顯樣式 *樣式 \_ 類型* 類型 *裝置 \_* 類型             |
| 排序器    | 別名 *裝置 \_ 別名* 可共用                                 | 類型 *裝置 \_ 類型*                                                             |
| 錄影機          | 別名 *裝置 \_ 別名* 可共用                                  | 類型 *裝置 \_ 類型*                                                             |
| videodisk    | 別名 *裝置 \_ 別名* 可共用                                  | 類型 *裝置 \_ 類型*                                                             |
| waveaudio    | 別名 *裝置 \_ 別名* 緩衝區 *緩衝區 \_ 大小*                     | 可共用的類型 *裝置 \_ 類型*                                                    |



 

下表列出可在 **lpszOpenFlags** 參數中指定的旗標，以及它們的意義。



| 值                 | 意義                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 別名 *裝置 \_ 別名* | 指定指定裝置的替代名稱。 如果有指定，就必須在後續命令中用來作為 *裝置 \_ 識別碼* 。                                                                                                                                                                                                                                          |
| *elementname*         | 指定裝置在裝置開啟時載入 (檔的名稱) 。                                                                                                                                                                                                                                                                                        |
| 緩衝區 *緩衝區 \_ 大小* | 設定波形音訊裝置所使用之緩衝區的大小（以秒為單位）。 安裝或設定波形音訊裝置時，會設定緩衝區的預設大小。 緩衝區大小通常會設定為4秒。 使用 MCIWAVE 裝置時，大小下限為2秒，而大小上限為9秒。                                                |
| 父 *hwnd*         | 指定父視窗的視窗控制碼。                                                                                                                                                                                                                                                                                                                    |
| 共用              | 將裝置或檔案初始化為可共用。 除非您在原始和後續的 **開啟** 命令中指定「可共用」，否則後續開啟裝置或檔案的嘗試都會失敗。 如果裝置已開啟且無法共用，則 MCI 會傳回不正確裝置錯誤。<br/> MCISEQ sequencer 和 MCIWAVE 裝置不支援共用檔案。<br/> |
| 樣式子系           | 開啟具有子視窗樣式的視窗。                                                                                                                                                                                                                                                                                                                            |
| 樣式重迭      | 開啟具有重迭視窗樣式的視窗。                                                                                                                                                                                                                                                                                                                      |
| 樣式快顯視窗           | 以快顯視窗樣式開啟視窗。                                                                                                                                                                                                                                                                                                                           |
| 樣式 *樣式 \_ 類型*   | 表示視窗樣式。                                                                                                                                                                                                                                                                                                                                            |
| 類型 *裝置 \_ 類型*   | 指定檔案的裝置類型。                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

MCI 會針對 CD 音訊裝置類型、"videodisc" （適用于 videodisc 裝置類型）、"sequencer" （適用于 MIDI sequencer 裝置類型）、"AVIVideo" （適用于數位視訊裝置類型）和 "waveaudio" （波形音訊裝置類型）保留 "cdaudio"。

除了「類型」旗標以外，MCI 也可以根據檔案所使用的擴充功能來選取裝置，如登錄或 SYSTEM.INI 檔案的 \[ MCI 延伸區段中所記錄 \] 。

MCI 可以使用檔案介面指標或資料流程介面指標來開啟 AVI 檔。 若要使用任一種類型的介面指標來開啟檔案，請指定 @ 符號 ( @ ) 後面接著介面指標，以取代 *lpszDevice* 參數的檔案或裝置名稱。 如需檔案和資料流程介面的詳細資訊，請參閱「AVIFile 函式 [和宏](avifile-functions-and-macros.md)」。

下列命令會開啟 "mysound" 裝置。

``` syntax
open new type waveaudio alias mysound buffer 6
```

使用裝置名稱 "new" 時，波形驅動程式會準備新的波形資源。 此命令會指派裝置別名 "mysound"，並指定6秒的緩衝區。

如果您將裝置名稱與檔案名結合，則可以消除「類型」旗標。 當您使用下列語法時，MCI 會辨識此組合：

*裝置 \_ 名稱* ！ *元素 \_ 名稱*

驚嘆號會將裝置名稱與檔案名分隔開來。 驚嘆號不應以空格分隔。

下列範例會開啟右邊。使用 "waveaudio" 裝置的 WAV 檔案。

``` syntax
open waveaudio!right.wav
```

MCIWAVE 驅動程式需要非同步波形音訊裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Corecrt \_ 的 io。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> </dl>

 

