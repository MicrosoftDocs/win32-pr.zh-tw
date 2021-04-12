---
title: 'MCI_RESERVE 命令 (Mmsystem .h) '
description: MCI \_ RESERVE 命令會為設備磁碟機實例的工作區配置連續的磁碟空間，以用於後續錄製。 數位影片裝置辨識此命令。
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934842"
---
# <a name="mci_reserve-command"></a>MCI \_ 保留命令

MCI \_ RESERVE 命令會為設備磁碟機實例的工作區配置連續的磁碟空間，以用於後續錄製。 數位影片裝置辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
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

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

[**MCI \_ DGV \_ 保留 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

如果工作區包含未儲存的資料，這項資料就會遺失。 如果在錄製之前未保留磁碟空間， [MCI \_ 記錄](mci-record.md) 命令會使用裝置特定的預設參數來執行隱含的保留。 在某些情況下，不需要保留，且可能會被設備磁碟機忽略。 明確保留空間可讓您更充分掌控磁片配置的延遲、配置的空間量，以及配置磁碟空間的位置。 您可以藉由再次發行 MCI 保留來變更已保留給此裝置實例的磁碟空間數量和位置 \_ 。 任何已配置且仍未使用的磁碟空間都不會解除配置，直到任何記錄的資料儲存或關閉設備磁碟機實例為止。

如果使用 \_ [mci \_ SETVIDEO](mci-setvideo.md) 命令的 mci off 旗標關閉影片，則保留的空間不會包含任何影片。 如果使用 \_ [mci \_ SETAUDIO](mci-setaudio.md) 命令的 mci off 旗標關閉音訊，則保留的空間不會包含任何音訊。 如果音訊和影片都已關閉，或者要求的大小為零，則不會保留任何空間，而且會解除配置任何現有的保留空間。

下列其他旗標適用于數位視訊裝置：

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI \_ DGV \_ 保留 \_
</dt> <dd>

*LpReserve* 所識別之結構的 **lpstrPath** 成員包含包含暫存檔案位置的緩衝區位址。 緩衝區只包含用來保存記錄資料之檔案的磁片磁碟機和目錄路徑;檔案名是由設備磁碟機所指定。 如果裝置實例已被明確儲存，則會刪除此暫存檔案。 如果省略此旗標，設備磁碟機會指定磁碟空間的配置位置。

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI \_ DGV \_ 保留 \_ 大小
</dt> <dd>

*LpReserve* 所識別之結構的 **dwSize** 成員會指定要在工作區中保留的磁碟空間量，以進行錄製。 值是以目前時間格式指定。 磁碟空間的數量是從要求的時間，以及檔案格式和影片和音訊演算法和品質值的結果所估計。 如果省略此旗標，設備磁碟機可能會使用它所定義的預設值。

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

 

