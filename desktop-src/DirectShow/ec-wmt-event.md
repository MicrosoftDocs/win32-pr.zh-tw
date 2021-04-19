---
description: 由 WM ASF 讀取器篩選器在讀取受數位版權管理保護的 ASF 檔案 (DRM) 時傳送。
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: 'EC_WMT_EVENT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982940"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (Dshow) 

由 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器在讀取受數位版權管理保護的 ASF 檔案 (DRM) 時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

下列其中一個 **WMT \_ 狀態值** ：



| 值                         | 描述                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| WMT \_ 取得 \_ 授權         | 當 DRM 元件已完成授權取得程式時（無論成功或失敗）傳送。 |
| WMT \_ 賦予            | 安全性升級程式已完成，可能是成功或失敗。                                |
| WMT \_ 需要具有 \_ 個人化 | 檔案要求應用程式在執行要求的動作之前，先收到安全性升級。          |
| WMT \_ 無 \_ 許可權               | 應用程式沒有許可權可對受 DRM 第1版保護的檔案執行要求的動作。                |
| WMT \_ 沒有任何 \_ 許可權， \_ 例如           | 應用程式沒有許可權可對受 DRM 版本7保護的檔案執行要求的動作。                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

[**AM \_ WMT \_ 事件 \_ 資料**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data)結構的指標，其中包含事件的相關資訊或 **Null**。 此結構的 **.pdata** 成員會指向其他資料，而此資料的類型取決於 **lParam1** 的值，如下表所示。



| lParam1                       | AM \_ WMT \_ 事件 \_ 資料。 .pdata                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ 取得 \_ 授權         | [**WM \_ 取得 \_ 授權 \_ 資料**](/windows/desktop/wmformat/wm-get-license-data)結構的指標。 此結構記載于 Windows Media Format SDK 中。 |
| WMT \_ 賦予            | [**WM \_ 賦予 \_ 狀態**](/windows/desktop/wmformat/wm-individualize-status)結構的指標。                                                        |
| WMT \_ 需要具有 \_ 個人化 | **Null**。                                                                                                                                        |
| WMT \_ 無 \_ 許可權               | 包含挑戰 URL 的寬字元字串指標。                                                                                   |
| WMT \_ 沒有任何 \_ 許可權， \_ 例如           | [**WM \_ 取得 \_ 授權 \_ 資料**](/windows/desktop/wmformat/wm-get-license-data)結構的指標。                                                               |



 

*LParam2* 的值可能是 **Null**。 請先檢查值，然後再取值指標。

</dd> </dl>

## <a name="remarks"></a>備註

如需啟用受 DRM 保護之檔案的播放詳細資訊，請參閱 Windows Media Format SDK 檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

