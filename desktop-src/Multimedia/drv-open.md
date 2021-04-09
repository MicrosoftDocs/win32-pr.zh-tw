---
title: 'DRV_OPEN 訊息 (Mmsystem .h) '
description: 指示驅動程式開啟新的實例。
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106223"
---
# <a name="drv_open-message"></a>WINSPOOL.DRV \_ 開啟的訊息

指示驅動程式開啟新的實例。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

可安裝驅動程式的識別碼。

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

可安裝的驅動程式實例的控制碼。

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

以 null 結束之寬字元字串的位址，指定用來開啟實例的設定資訊。 如果沒有可用的設定資訊，則此字串為空白或參數為 **Null**。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

32位驅動程式特定的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零值，否則傳回零。

## <a name="remarks"></a>備註

如果驅動程式傳回非零值，系統會使用該值做為驅動程式識別碼， (*dwDriverId* 參數在其後傳送至驅動程式實例的訊息中) 。 驅動程式可以傳回任何類型的值做為識別碼。 例如，某些驅動程式會傳回指向實例特定資訊的記憶體位址。 使用這個方法來指定驅動程式實例的識別碼，可讓驅動程式在處理訊息時立即存取訊號。

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

 

 





