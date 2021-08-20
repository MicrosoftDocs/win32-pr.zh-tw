---
title: 'MCI_LIST 命令 (Mmsystem .h) '
description: MCI \_ 清單命令可取得裝置可用輸入的數目和類型的相關資訊。 數位影片和 VCR 裝置會辨識此命令。
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9bd3aa35875791d6fa916d9d6831bdcb83a6db43be6e5859ce582243606f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138634"
---
# <a name="mci_list-command"></a>MCI \_ 清單命令

MCI \_ 清單命令可取得裝置可用輸入的數目和類型的相關資訊。 數位影片和 VCR 裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
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

MCI \_ 通知、mci \_ 等候或 mci \_ 測試。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ 清單 \_ ALG
</dt> <dd>

*LpList* 所識別之結構的 **lpstrAlgorithm** 成員包含包含演算法名稱之緩衝區的位址。 此名稱會用來抓取與演算法相關聯的品質描述項類型。

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI \_ DGV \_ 清單 \_ 計數
</dt> <dd>

傳回指定類型的選項數目。

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI \_ DGV \_ 清單 \_ 專案
</dt> <dd>

常數，表示清單類型包含在 *lpList* 所識別之結構的 **dwItem** 成員中。 此為必要旗標。 您可以使用下列其中一個常數來表示清單類型：

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ 列出 \_ 音訊 \_ ALG
</dt> <dd>

此命令應該會取出音訊演算法的名稱。

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ 列出 \_ 音訊 \_ 品質
</dt> <dd>

此命令應該會取出音訊品質層級。 傳回的層級與 *lpList* 所識別之結構的 **lpstrAlgorithm** 成員所參考的演算法相關聯。 如果使用字串 "current" 指定該成員，則會傳回與目前演算法相關聯的品質。

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI \_ DGV \_ 列出 \_ 音訊 \_ 串流
</dt> <dd>

此命令應該會取出音訊串流的名稱。

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI \_ DGV \_ 清單 \_ 仍在 \_ AL
</dt> <dd>

此命令應該會取出仍為演算法的名稱。

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI \_ DGV \_ 清單 \_ 仍為 \_ 品質
</dt> <dd>

此命令應該會取出品質層級。 傳回的層級與 *lpList* 所識別之結構的 **lpstrAlgorithm** 成員所參考的演算法相關聯。 如果使用字串 "current" 指定該成員，則會傳回與目前演算法相關聯的品質。

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI \_ DGV \_ 列出 \_ 影片 \_ ALG
</dt> <dd>

此命令應該會取出影片演算法的名稱。

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI \_ DGV \_ 列出 \_ 影片 \_ 品質
</dt> <dd>

此命令應該會取出影片品質層級。 傳回的層級與 *lpList* 所識別之結構的 **lpstrAlgorithm** 成員所參考的演算法相關聯。 如果使用字串 "current" 指定該成員，則會傳回與目前演算法相關聯的品質。

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI \_ DGV \_ 列出 \_ 影片 \_ 來源
</dt> <dd>

此命令應該會傳回影片來源的相關資訊。 搭配 MCI \_ DGV \_ LIST COUNT 使用時 \_ ，此命令會傳回影片來源的數目。 搭配 MCI \_ DGV \_ LIST NUMBER 使用時 \_ ，此命令會傳回影片來源的類型。 MCI 定義了下列類型：

-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ GENERIC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ NTSC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO

傳回的每個類型可能會有一個以上的來源。 當該連接器允許一個以上的信號類型時，就會使用泛型來源類型。

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI \_ DGV \_ 列出 \_ 影片 \_ 串流
</dt> <dd>

此命令應該會取出視頻資料流程的名稱。

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI \_ DGV \_ 清單 \_ 編號
</dt> <dd>

在 *lpList* 所識別之結構的 **dwNumber** 成員中指定索引。 索引必須是介於1和針對 MCI \_ DGV \_ LIST COUNT 旗標傳回值之間的整數 \_ 。

</dd> </dl>

針對數位影片裝置， *lpList* 會指向 [**MCI \_ DGV \_ 清單 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) 結構。

下列其他旗標適用于 **vcr** 裝置類型：

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI \_ VCR \_ 清單 \_ 音訊 \_ 來源
</dt> <dd>

列出音訊輸入或類型。

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI \_ VCR \_ 清單 \_ 計數
</dt> <dd>

將 *lpList* 所識別之結構的 **dwReturn** 成員設定為影片或音訊輸入的總數目。

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI \_ VCR \_ 清單 \_ 編號
</dt> <dd>

將 *lpList* 所識別之結構的 **dwReturn** 成員設定為 **dwNumber** 成員所指定之影片或音訊輸入的類型。

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI \_ VCR \_ 清單 \_ 影片 \_ 來源
</dt> <dd>

列出影片輸入或類型。

</dd> </dl>

若為 VCR 裝置， *lpList* 會指向 [**MCI \_ VCR \_ 清單 \_ PARMS**](mci-vcr-list-parms.md) 結構。

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

 

