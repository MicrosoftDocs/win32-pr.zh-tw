---
title: 'MCI_QUALITY 命令 (Mmsystem .h) '
description: MCI \_ quality 命令會定義音訊、影片或靜止影像資料壓縮的自訂品質層級。 數位影片裝置辨識此命令。
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1237d9b70c9f06782342c404c19dd23cf6f0848f8c7b33523bce35990287fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138219"
---
# <a name="mci_quality-command"></a>MCI \_ 品質命令

MCI \_ quality 命令會定義音訊、影片或靜止影像資料壓縮的自訂品質層級。 數位影片裝置辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
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

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

[**MCI \_ DGV \_ QUALITY \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

使用 [mci \_ SETAUDIO](mci-setaudio.md) 和 [mci \_ SETVIDEO](mci-setvideo.md) 命令設定音訊、影片或仍有品質時，可使用為此品質層級定義的名稱。

下列其他旗標適用于數位視訊裝置：

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ 品質 \_ ALG
</dt> <dd>

*LpQuality* 所識別之結構的 **lpstrAlgorithm** 成員包含包含演算法名稱的緩衝區位址。 設備磁碟機必須支援此演算法，且必須與使用的音訊、仍然或影片描述項相容。 如果省略此旗標，則會使用目前的演算法。

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI \_ 品質 \_ 對話方塊
</dt> <dd>

設備磁碟機應該會顯示用來指定品質層級的對話方塊。 此對話方塊包含設備磁碟機內部所使用的演算法特定欄位，以建立描述特定品質層級的結構。

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI \_ 品質 \_ 控制碼
</dt> <dd>

*LpQuality* 所識別之結構的 **dwHandle** 成員包含結構的控制碼。 結構包含描述特定品質層級的演算法特定資料。 演算法的結構格式取決於裝置。

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI \_ 品質 \_ 專案
</dt> <dd>

常數，表示演算法的類型會包含在 *lpQuality* 所識別之結構的 **dwItem** 成員中。

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI \_ 品質 \_ 名稱
</dt> <dd>

*LpQuality* 所識別之結構的 **lpstrName** 成員包含包含品質描述項的緩衝區位址。

</dd> </dl>

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

 

