---
title: 'DRV_INSTALL 訊息 (Mmsystem .h) '
description: 通知驅動程式正在安裝。 驅動程式應該建立並初始化任何所需的登錄機碼和值，並確認支援的驅動程式和硬體已安裝並正確設定。
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- DRV_INSTALL message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935074"
---
# <a name="drv_install-message"></a>WINSPOOL.DRV \_ 安裝訊息

通知驅動程式正在安裝。 驅動程式應該建立並初始化任何所需的登錄機碼和值，並確認支援的驅動程式和硬體已安裝並正確設定。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

可安裝驅動程式的識別碼。 這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

可安裝的驅動程式實例的控制碼。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

[**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)結構的位址或 **Null**。 如果指定了結構，它就會包含與驅動程式相關聯的登錄機碼和值的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值：



| 需求 | 值 |
|-----------------|--------------------------------------------------------------------------------------------|
| DRVCNF \_ 確定      | 安裝成功;不需要採取任何進一步的動作。                             |
| DRVCNF \_ 取消  | 安裝失敗。                                                                  |
| DRVCNF \_ 重新開機 | 安裝成功，但在系統重新開機之前不會生效。 |



 

## <a name="remarks"></a>備註

未使用 *lParam1* 參數。

有些可安裝的驅動程式會將設定資訊附加至指派給與驅動程式相關聯之登錄值的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[可安裝的驅動程式](installable-drivers.md)
</dt> <dt>

[可安裝的驅動程式訊息](installable-driver-messages.md)
</dt> </dl>

 

