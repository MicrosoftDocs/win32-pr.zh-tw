---
title: 'MCI_CUE 命令 (Mmsystem .h) '
description: MCI \_ 提示命令會提示裝置，以便從最小延遲開始播放或錄製。 數位-影片、VCR 和波形-音訊裝置會辨識此命令。
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967985"
---
# <a name="mci_cue-command"></a>MCI \_ 提示命令

MCI \_ 提示命令會提示裝置，以便從最小延遲開始播放或錄製。 數位-影片、VCR 和波形-音訊裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

要接收命令訊息之 MCI 裝置的裝置識別碼。

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI \_ DGV \_ 提示 \_ 輸入
</dt> <dd>

數位影片實例應準備進行錄製。 如果應用程式未保留磁碟空間，則裝置會使用其預設參數保留磁碟空間。 如果目前的簡報來源已經是外部輸入，應用程式可以省略此旗標。  (此旗標不會影響選取展示來源。 ) 

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV \_ 提示 \_ NOSHOW
</dt> <dd>

數位影片實例應該準備好播放使用命令指定的框架，而不顯示它。 當指定這個旗標時，即使對應的框架不是目前的位置，顯示器仍會繼續在框架緩衝區中顯示影像。 例如，如果框架緩衝區包含來自框架7的影像，則當使用此旗標將裝置提示至任何其他位置時，裝置會繼續顯示框架7。 未使用此旗標且不含 MCI 旗標的後續提示命令會 \_ 顯示目前的畫面格。

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI \_ DGV \_ 提示 \_ 輸出
</dt> <dd>

數位影片實例應該準備好進行播放。 如果工作區暫停，則不會發生定位。 如果工作區已停止，此位置可能會變更為先前的主要畫面格影像。 如果目前的簡報來源已經是工作區，應用程式可以省略此旗標。

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

工作區位置會包含在 *lpCue* 所識別之結構的 **dwTo** 成員中。 指派給位置值的單位會使用 \_ \_ mci set 命令的 mci set TIME \_ FORMAT 旗 [ \_ ](mci-set.md) 標來指定。 這相當於搜尋位置，但裝置會在命令之後暫停。

</dd> </dl>

針對 **digitalvideo** 裝置， *lpCue* 參數會指向 [**MCI \_ DGV \_ 提示 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) 結構。

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源
</dt> <dd>

*LpCue* 所指向結構的 **dwFrom** 成員包含以目前時間格式指定的起始位置。

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至
</dt> <dd>

*LpCue* 所指向之結構的 **dwTo** 成員包含結束 (目前時間格式所指定的) 位置。

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI \_ VCR \_ 提示 \_ 輸入
</dt> <dd>

準備錄製。

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI \_ VCR \_ 提示 \_ 輸出
</dt> <dd>

準備進行播放。 如果沒有 \_ 指定 mci vcr \_ 提示 \_ 輸入或 mci \_ vcr \_ 提示 \_ 輸出， \_ \_ \_ 則會假設為 mci vcr 提示輸出。

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI \_ VCR \_ 提示預先進行 \_
</dt> <dd>

將裝置提示至目前的位置或 **dwFrom** 位置，減去預先進行的持續時間。 這可讓裝置在進入錄製或播放模式之前做好準備。

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI \_ VCR \_ 提示 \_ 反向
</dt> <dd>

下一個 play 或 record 命令的方向相反。

</dd> </dl>

使用 mci \_ 提示命令搭配 mci vcr 提示輸出旗標來提示播放時 \_ \_ \_ ，您可以藉 \_ 由從、mci [ \_ ](mci-play.md) \_ \_ TO 或 mci \_ VCR \_ 播放的 mci 發出 mci play 命令，來取消 mci 提示 \_ 。

使用 mci vcr 提示輸入旗標來提示記錄時 \_ \_ \_ \_ ，您可以藉 \_ 由發出 mci [ \_ 記錄](mci-record.md) 命令與 mci \_ 、mci \_ TO 或 mci \_ vcr \_ 記錄 \_ 初始化，來取消 mci 提示。

若為 **vcr** 裝置， *lpCue* 參數會指向 [**MCI \_ vcr \_ 提示 \_ PARMS**](mci-vcr-cue-parms.md) 結構。

下列其他旗標適用于 **waveaudio** 裝置類型：

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ 輸入
</dt> <dd>

波形音訊輸入裝置應 cued。

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ 輸出
</dt> <dd>

波形音訊輸出裝置應 cued。 如果未指定旗標，這會是預設旗標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 命令](mci-commands.md)
</dt> </dl>

 

