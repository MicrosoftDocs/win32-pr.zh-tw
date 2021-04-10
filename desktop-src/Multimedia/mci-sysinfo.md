---
title: 'MCI_SYSINFO 命令 (Mmsystem .h) '
description: MCI \_ SYSINFO 命令會捕獲 mci 裝置的相關資訊。
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- MCI_SYSINFO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934485"
---
# <a name="mci_sysinfo-command"></a>MCI \_ SYSINFO 命令

MCI \_ SYSINFO 命令會捕獲 mci 裝置的相關資訊。 MCI 直接支援此命令，而不是將它傳遞至裝置。 任何 MCI 應用程式都可以使用此命令。 在由 *lpSysInfo* 所識別之結構的 **lpstrReturn** 成員所指向的應用程式提供的緩衝區中，會傳回字串資訊。 數值資訊會以 **DWORD** 值的形式傳回，放在應用程式提供的緩衝區中。 **DwRetSize** 成員指定緩衝區長度。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
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

下列一或多個標準和命令特定的旗標：

</dd> <dt>

<span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI \_ SYSINFO \_ INSTALLNAME
</dt> <dd>

取得登錄中列出的名稱 (或用來安裝裝置的 SYSTEM.INI 檔案) 。

</dd> <dt>

<span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI \_ SYSINFO \_ 名稱
</dt> <dd>

取得與 **lpSysInfo** 所識別之結構的 **dwNumber** 成員中指定的裝置編號對應的裝置名稱。 如果 \_ \_ 已設定 mci SYSINFO 開啟旗標，mci 會傳回開啟裝置的名稱。

</dd> <dt>

<span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI \_ SYSINFO \_ 開啟
</dt> <dd>

取得開啟裝置的數量或名稱。

</dd> <dt>

<span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI \_ SYSINFO \_ 數量
</dt> <dd>

取得登錄或 SYSTEM.INI 檔案的 mci 區段中所列指定類型的裝置數目 \[ \] 。 如果 \_ \_ 已設定 MCI SYSINFO 開啟旗標，則會傳回開啟的裝置數目。

</dd> <dt>

<span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*
</dt> <dd>

[**MCI \_ SYSINFO \_ PARMS**](mci-sysinfo-parms.md)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

*LpSysInfo* 所識別之結構的 **wDeviceType** 成員是用來指出查詢的裝置類型。 如果 *wDeviceID* 參數設定為 MCI \_ 所有 \_ 裝置 \_ 識別碼，則會覆寫 **wDeviceType** 的值。 如需裝置類型的清單，請參閱 [MCI 裝置類型](mci-device-types.md)。

整數傳回值是由 *lpSysInfo* 所識別之結構的 **lpstrReturn** 成員所指向之緩衝區中傳回的 **DWORD** 值。

字串傳回值是以 null 終止的字串，在由 *lpSysInfo* 所識別之結構的 **lpstrReturn** 成員所指向的緩衝區中傳回。

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

 

