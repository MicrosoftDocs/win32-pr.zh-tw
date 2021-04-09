---
title: 'DRV_CONFIGURE 訊息 (Mmsystem .h) '
description: 指示可安裝的驅動程式顯示其設定對話方塊，並讓使用者為指定的可安裝驅動程式實例指定新設定。
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- DRV_CONFIGURE message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935077"
---
# <a name="drv_configure-message"></a>WINSPOOL.DRV \_ 設定訊息

指示可安裝的驅動程式顯示其設定對話方塊，並讓使用者為指定的可安裝驅動程式實例指定新設定。

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

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

父視窗的控制碼。 此視窗會用來做為 [設定] 對話方塊的父視窗。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

[**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)結構的位址或 **Null**。 如果指定了結構，它就會包含與驅動程式相關聯的登錄機碼和值的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值：



| 需求 | 值 |
|-----------------|----------------------------------------------------------------------------------------------------|
| DRVCNF \_ 確定      | 設定成功;不需要採取任何進一步的動作。                                    |
| DRVCNF \_ 取消  | 使用者取消了對話方塊;不需要採取任何進一步的動作。                                   |
| DRVCNF \_ 重新開機 | 設定成功，但在重新開機系統之前，變更不會生效。 |



 

## <a name="remarks"></a>備註

有些可安裝的驅動程式會將設定資訊附加至指派給與驅動程式相關聯之登錄值的值。

WINSPOOL.DRV \_ cancel、Winspool.drv \_ OK 和 Winspool.drv \_ 重新開機傳回值已過時; 它們已分別由 DRVCNF \_ CANCEL、DRVCNF \_ OK 和 DRVCNF \_ restart 取代。

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

 

