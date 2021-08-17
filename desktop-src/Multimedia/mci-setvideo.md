---
title: 'MCI_SETVIDEO 命令 (Mmsystem .h) '
description: MCI \_ SETVIDEO 命令會設定與影片播放相關聯的值。 數位影片和 VCR 裝置會辨識此命令。
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- MCI_SETVIDEO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23206d169ad5e273927ead247c44194660c8d6b201c725e1b4d4ab24fd5e1544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803375"
---
# <a name="mci_setvideo-command"></a>MCI \_ SETVIDEO 命令

MCI \_ SETVIDEO 命令會設定與影片播放相關聯的值。 數位影片和 VCR 裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
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

**MCI \_通知**、 **mci \_ 等候** 或 **MCI \_ 測試**。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標會搭配 "digitalvideo" 裝置類型使用：

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ SETVIDEO \_ ALG
</dt> <dd>

*LpSetVideo* 所識別之結構的 **lpstrAlgorithm** 成員包含包含視訊壓縮演算法名稱的緩衝區位址。 壓縮演算法會由後續的 [mci \_ 保留](mci-reserve.md) 或 [MCI \_ 記錄](mci-record.md) 命令使用。 可用的演算法取決於裝置。

如果指定的演算法與目前的檔案格式不相容，則檔案格式會變更為演算法的預設格式。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME
</dt> <dd>

搭配 **MCI \_ DGV \_ SETVIDEO \_** 使用時，表示指定時間（以毫秒為單位），且為絕對時間。  (這次無法在工作區的播放中執行。 ) 

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI \_ DGV \_ SETVIDEO \_ 輸入
</dt> <dd>

修改 **MCI \_ DGV \_ SETVIDEO \_ 亮度**、 **mci \_ DGV \_ SETVIDEO \_ COLOR**、 **mci \_ DGV \_ SETVIDEO \_ 對比度**、 **MCI \_ DGV \_ SETVIDEO \_ GAMMA**、 **mci \_ DGV \_ SETVIDEO \_ 銳利** 或 **mci DGV SETVIDEO \_ \_ \_ 淡色** ，使其影響輸入信號並修改記錄的內容。 可能的話，這是監視輸入時的預設值。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI \_ DGV \_ SETVIDEO \_ 專案
</dt> <dd>

影片常數是在 *lpSetVideo* 所識別之結構的 **dwItem** 成員中指定。 常數可識別正在設定的值。 您可以使用此旗標來指定下列常數：

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI \_ AVI \_ SETVIDEO \_ DRAW \_ 程式
</dt> <dd>

在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定了新的繪圖程式位址。 只有在裝置閒置時，才可以指定新的繪圖程式。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。 字串命令介面中沒有此旗標的對等專案。

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI \_ AVI \_ SETVIDEO \_ 調色板 \_ 色彩
</dt> <dd>

在 *lpSetVideo* 所識別之結構的 **dwOver** 和 **dwValue** 成員中指定了新的調色板色彩。 **DwOver** 成員會指定要變更之色彩的調色板索引，而 **dwValue** 成員會以 RGB 值指定新的色彩。 當您使用此常數時，您也必須使用 **mci \_ DGV \_ SETVIDEO \_ 專案** 來指定 **mci \_ DGV \_ SETVIDEO \_ OVER** 和 **mci \_ DGV \_ SETVIDEO \_ 值** 旗標。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI \_ AVI \_ SETVIDEO \_ 調色板 \_ 半色調
</dt> <dd>

指出應該使用半色調調色板，而不是預設的調色板。 只有 MCIAVI 數位視訊驅動程式能辨識此旗標。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL
</dt> <dd>

依 *lpSetVideo* 所識別之結構的 **dwValue** 成員，指定每個圖元的位數。 每圖元的位數會用來儲存已捕捉或已記錄的資料

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI \_ DGV \_ SETVIDEO \_ 亮度
</dt> <dd>

影片亮度層級會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的因素。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI \_ DGV \_ SETVIDEO \_ 色彩
</dt> <dd>

影片色彩飽和度層級會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的因素。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI \_ DGV \_ SETVIDEO \_ 對比
</dt> <dd>

影片對比層級會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的一個因素。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI \_ DGV \_ SETVIDEO \_ 幀 \_ 速率
</dt> <dd>

畫面播放速率是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。 速率是以每秒的畫面格時間單位（1000）來指定。 例如，每秒29.97 個畫面格會指定為29970。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ SETVIDEO \_ GAMMA
</dt> <dd>

Gamma 更正指數值是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。 Gamma 修正會調整在展示來源中編碼的強度與顯示的亮度之間的對應。 值是指數乘以1000。 例如，2200表示2.2 的指數。 值為1000時，表示指數為1，不會套用 gamma 更正。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ COLOR
</dt> <dd>

索引鍵色彩是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。 按鍵色彩是 RGB 值。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI \_ DGV \_ SETVIDEO \_ KEY \_ INDEX
</dt> <dd>

索引鍵索引值是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。 Index 參數是實體的調色板索引。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE
</dt> <dd>

在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定了調色板控制碼。 調色板控制碼包含在低序位字組中。 數位影片裝置不應該釋出使用此命令傳遞的調色板。 應用程式應該在關閉裝置之後釋放。 只有使用調色板的裝置才支援此旗標。 如果這個指定的調色板控制碼為零，則會使用預設的調色板。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI \_ DGV \_ SETVIDEO \_ 清晰度
</dt> <dd>

影片清晰度值會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的一個因素。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI \_ DGV \_ SETVIDEO \_ 來源
</dt> <dd>

指定影片輸入來源的常數會指定于 *lpSetVideo* 所識別之結構的 **dwValue** 成員中。 以下是定義的常數：

-   **MCI \_DGV \_ SETVIDEO \_ SRC \_ NTSC**： ntsc 電視。
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ pal： pal 電視。
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB： rgb video。
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM： SECAM 電視。
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO： S-Video。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI \_ DGV \_ SETVIDEO \_ STREAM
</dt> <dd>

影片資料流程是在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中指定。 整數值指定從工作區播放的影片串流。 如果未指定資料流程，且檔案格式未定義預設資料流程，則會播放第一個實際交錯的影片資料流程。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI \_ DGV \_ SETVIDEO \_ 淡色
</dt> <dd>

影片色調值會指定為 *lpSetVideo* 所識別之結構的 **dwValue** 成員中的一個因素。 一般而言，這項調整會在許多彩色電視集的淡色控制項之後進行模型化，並將250定義為綠色、750定義為紅色，而 0 (或 1000) 定義為藍色。 名義值一律為500。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI \_ DGV \_ SETVIDEO \_ 輸出
</dt> <dd>

**Mci \_ DGV \_ SETVIDEO \_ 亮度**、 **mci \_ DGV \_ SETVIDEO \_ COLOR**、 **mci \_ DGV \_ SETVIDEO \_ 對比**、 **MCI \_ DGV \_ SETVIDEO \_ GAMMA**、 **MCI \_ DGV \_ SETVIDEO \_ 銳利** 或 **mci DGV SETVIDEO \_ \_ \_ 淡色** 旗標會被修改，因此只會影響顯示的信號，而不會影響所錄製的信號。 可能的話，這是監視檔案時的預設值。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_
</dt> <dd>

轉換長度參數會包含在由 *lpSetVideo* 所識別之結構的 **dwOver** 成員中。 轉換長度會指定以目前時間格式 (的時間長度，) 進行變更所需的時間。 如果未使用此旗標，則會立即進行變更。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI \_ DGV \_ SETVIDEO \_ 品質
</dt> <dd>

*LpSetVideo* 所識別之結構的 **lpstrQuality** 成員包含描述影片品質的緩衝區位址。 緩衝區中的文字字串會指定影片壓縮演算法的特性。

您可以使用 **MCI \_ DGV \_ SETVIDEO \_ ALG** 旗標來選取指定演算法的品質描述項。 如果省略此旗標，則會使用目前的演算法。

可用的演算法和描述項名稱取決於裝置。 每個裝置都會提供可用演算法的相關檔，以及適用描述項名稱的描述。 [MCI \_ QUALITY](mci-quality.md)命令可以定義其他描述項名稱。 所有裝置都支援描述項「低」、「中」和「高」。 預設值為 [驅動程式特定]。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI \_ DGV \_ SETVIDEO \_ 記錄
</dt> <dd>

指定錄製是否包含或排除影片資料。 當結合的 **MCI \_ 設定 \_** 為時，會記錄影片資料。 當您 **將 MCI \_ 設定為 \_ OFF** 時，就會排除影片資料。 預設值包括影片資料。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ SETVIDEO \_ SRC \_ NUMBER
</dt> <dd>

影片來源的數位是在 *lpSetVideo* 所識別之結構的 **dwSourceNumber** 成員中指定。 如果 **MCI \_ DGV \_ SETVIDEO \_ 值** 所指定的類型有一個以上的輸入，則值會選取輸入。 此旗標一律必須搭配 **MCI \_ DGV \_ SETVIDEO \_ 來源** 使用。 但是，如果已省略 **mci \_ DGV \_ SETVIDEO \_ 值** ，指定的來源編號就會指出要使用的絕對來源，如同 [mci \_ 清單](mci-list.md) 命令中所指定。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_
</dt> <dd>

指定的演算法名稱或品質值適用于靜止影像。

每個設備磁碟機都必須支援 "none" 演算法，這表示沒有壓縮。 此為預設值。 在此情況下，數位影片裝置仍會將影像儲存為 RGB 裝置獨立點陣圖， (Dib) 。

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI \_ DGV \_ SETVIDEO \_ 值
</dt> <dd>

值會包含在 *lpSetVideo* 所識別之結構的 **dwValue** 成員中。 值的意義是由 **MCI \_ DGV \_ SETVIDEO \_ 專案** 旗標所指定。

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI
</dt> <dd>

停用影片輸出。 針對數位視訊裝置，停用影片會設定 [MCI \_ PUT](mci-put.md) 命令所定義之目的矩形中的圖元 (或其預設值，目前視窗的用戶端區域) 為純色，但不會影響框架緩衝區。 如有需要，您可以使用 [MCI \_ 視窗](mci-window.md) 命令來隱藏視窗。 影片的來源（不論是工作區或外部輸入）可能會繼續將新影像儲存在框架緩衝區中，但在啟用影片之前，不會顯示它們。 雖然應用程式應該使用 MCI \_ SETVIDEO 命令來控制此功能，但數位視訊裝置仍然必須支援此旗標。 開啟開啟之後的預設值。

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于
</dt> <dd>

啟用影片輸出。

</dd> </dl>

針對數位影片裝置， *lpSetVideo* 參數會指向 [**MCI \_ DGV \_ SETVIDEO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) 結構。

下列其他旗標會搭配 "vcr" 裝置類型使用：

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI \_ VCR \_ SETVIDEO \_ 記錄
</dt> <dd>

將影片錄製設定為開啟或關閉。 搭配下列其中一個旗標使用：

-   **MCI \_設定為 \_ ON**。 錄製影片。
-   **MCI \_設定為 \_ OFF**。 錄製錄影。 您可能必須先關閉組合錄製 (使用 [mci \_ set](mci-set.md) 命令，並將 [ **mci \_ VCR \_ 組 \_ 組合 \_ 記錄** ] 旗標設為 [關閉]) ，然後才能關閉影片錄製。

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>MCI \_ 曲目
</dt> <dd>

*LpSetVideo* 所識別之結構的 **dwTrack** 成員會指定受命令影響的追蹤。

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI \_ VCR \_ SETVIDEO \_ 來源
</dt> <dd>

設定影片來源，且必須與 **MCI VCR SETVIDEO 搭配使用 \_ \_ \_ 以進行** 旗標。

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI \_ VCR \_ SETVIDEO \_ 監視
</dt> <dd>

設定影片來源監視器，而且必須與 MCI VCR SETVIDEO 搭配使用 \_ \_ \_ 以進行旗標。

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ SETVIDEO \_ 至
</dt> <dd>

*LpSetVideo* 所識別之結構的 **dwTo** 成員包含下列其中一個常數：

<dl> <dd>**MCI \_ VCR \_ SRC \_ 類型 \_ 調諧器**</dd> <dd>**MCI \_ VCR \_ SRC \_ 類型 \_ 行**</dd> <dd>**MCI \_ VCR \_ SRC \_ 類型 \_ AUX**</dd> <dd>**MCI \_ VCR \_ SRC \_ 類型 \_ 泛型**</dd> <dd>**MCI \_ VCR \_ SRC \_ 類型 \_ 靜音**</dd> <dd>**MCI \_ VCR \_ SRC \_ 類型 \_ 輸出**</dd> <dd>**MCI \_ VCR \_ SRC \_ 類型 \_ RGB**</dd> <dd>**MCI \_ VCR \_ SETVIDEO \_ 號碼**</dd> </dl>

*LpSetVideo* 所識別之結構的 **dwNumber** 成員包含要使用的 **dwTo** 成員) 中所指定類型的影片輸入 (。

</dd> </dl>

若為 VCR 裝置， *lpSetVideo* 參數會指向 [**MCI \_ VCR \_ SETVIDEO \_ PARMS**](mci-vcr-setvideo-parms.md) 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 命令](mci-commands.md)
</dt> </dl>

 

