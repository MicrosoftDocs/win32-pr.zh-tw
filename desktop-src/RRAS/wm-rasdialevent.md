---
title: 'WM_RASDIALEVENT 訊息 (Ras) '
description: '\_當 RAS 連接程式期間發生狀態事件變更時，作業系統會將 WM RASDIALEVENT 訊息傳送至視窗程式。'
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT 訊息 RAS
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969752"
---
# <a name="wm_rasdialevent-message"></a>WM \_ RASDIALEVENT 訊息

當 RAS 連接程式期間發生狀態事件變更時，作業系統會將 **WM \_ RASDIALEVENT** 訊息傳送至視窗程式。 使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)*的通知程式參數指定* 視窗來處理這類事件的通知時，就會發生這種情況。

這兩個訊息參數相當於與 [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) 和 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) 回呼函數搭配使用之相同名稱的參數。


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*rasconnstate* 
</dt> <dd>

*WParam* 的值。 相當於 [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)和 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)回呼函數的 *rasconnstate* 參數。 指定 [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) 列舉值，這個值表示 RasDial 遠端存取連接程式即將進入的狀態。

</dd> <dt>

*dwError* 
</dt> <dd>

*LParam* 的值。 相當於 [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)和 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)回呼函數的 *dwError* 參數。 非零值表示發生的錯誤，如果未發生錯誤，則為零。

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 會在進入每個連接狀態時，將 *dwError* 設定為零的訊息傳送。 如果狀態中發生錯誤，則會再次傳送該狀態的訊息，這次會有非零的 *dwError* 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Ras。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端存取服務 (RAS) 總覽](about-remote-access-service.md)
</dt> <dt>

[遠端存取服務訊息](remote-access-service-messages.md)
</dt> <dt>

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

