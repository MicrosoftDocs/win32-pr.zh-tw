---
title: 'MCI_BREAK 命令 (Mmsystem .h) '
description: MCI \_ BREAK 命令會設定 mci 裝置的 BREAK 鍵。 MCI 直接支援此命令，而不是將它傳遞至裝置。 任何 MCI 應用程式都可以使用此命令。
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07006ddfb38e1a57f6e08cb73d9b33021d139b9542245aec137e0969378140e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803967"
---
# <a name="mci_break-command"></a>MCI \_ BREAK 命令

MCI \_ BREAK 命令會設定 mci 裝置的 BREAK 鍵。 MCI 直接支援此命令，而不是將它傳遞至裝置。 任何 MCI 應用程式都可以使用此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
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

\_ \_ (VCR) 裝置、mci 測試的 mci 通知、mci 等候，或。 \_ 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

[**MCI \_ 中斷 \_ PARMS**](mci-break-parms.md)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

您可能必須多次按下 break 鍵，以中斷等候作業。 在裝置等待取消之後按下 break 鍵，可以將中斷傳送至應用程式。 如果應用程式有針對虛擬機器碼程式碼定義的動作，則可能會不慎回應中斷。 例如，如果應用程式使用 VK \_ CANCEL 作為快速鍵，則如果在等候取消之後按下它，就可以回應預設的 CTRL + BREAK 鍵。

下列其他旗標適用于所有裝置：

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI \_ BREAK \_ HWND
</dt> <dd>

*LpBreak* 所識別之結構的 **hwndBreak** 成員包含必須是目前視窗的視窗控制碼，才能啟用該 MCI 裝置的中斷偵測。 這通常是應用程式的主視窗。 如果省略，MCI 不會檢查目前視窗的視窗控制碼。

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI \_ 中斷 \_ 金鑰
</dt> <dd>

由 *lpBreak* 所識別之結構的 **nVirtKey** 成員會指定用於 break 索引鍵的虛擬機器碼程式碼。 根據預設，MCI 會將 CTRL + BREAK 指派為 break 鍵。 如果 \_ 未指定 MCI BREAK，則需要此旗標 \_ 。

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI \_ 中斷 \_
</dt> <dd>

停用指定裝置的任何現有 break 鍵。

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

 

