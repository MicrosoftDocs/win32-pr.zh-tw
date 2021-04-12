---
title: 'EC_WMT_EVENT (Windows Media Format 11 SDK) '
description: EC \_ WMT \_ 活動
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows Media Format SDK，EC_WMT_EVENT
- DirectShow，EC_WMT_EVENT
- EC_WMT_EVENT
- 數位版權管理 (DRM) ，EC_WMT_EVENT
- DRM (數位版權管理) ，EC_WMT_EVENT
- Advanced Systems Format (ASF) ，EC_WMT_EVENT
- ASF (Advanced Systems Format) ，EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464068"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (Windows Media Format 11 SDK) 

當應用程式使用 ASF 讀取器篩選器來播放受數位版權管理保護的 ASF 檔案時，由 Windows Media 格式 SDK 傳送 (DRM) 。

參數

*lParam1*

可以是下列其中一個 WMT \_ 狀態值。



| WMT \_ 狀態訊息           | Description                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ 無 \_ 許可權               | 檔案受到 DRM 第1版的保護，應用程式沒有許可權可執行要求的動作。                    |
| WMT \_ 取得 \_ 授權         | 授權取得流程已完成。  (這不一定表示已成功取得授權。 )  |
| WMT \_ 沒有任何 \_ 許可權， \_ 例如           | 檔案受到 DRM 版本7的保護，應用程式沒有許可權可執行要求的動作。                    |
| WMT \_ 需要具有 \_ 個人化 | 授權只允許個別的應用程式執行要求的動作。                                           |
| WMT \_ 賦予            | 現在正在執行或已完成的個人化程式。                                                    |



 

*lParam2*

**AM \_ WMT \_ 事件 \_ 資料** 結構的指標，其中包含 **.pdata** 成員指標中事件的相關資訊，以及 Windows Media 格式 SDK 所傳送的 **HRESULT** 狀態碼。 *LParam2* 的值取決於 *lParam1* 的值，如下表所述。  (「WM」 \_ 結構是在 Windows Media FORMAT SDK 中定義。 ) 



| 如果 lParam1 為 .。。              | \_WMT \_ 事件 \_ 資料。 .pdata 是 .。。                            |
|-------------------------------|-------------------------------------------------------------|
| WMT \_ 無 \_ 許可權               | 包含挑戰 URL 的 **WCHAR** 字串指標。 |
| WMT \_ 取得 \_ 授權         | **WM \_ 取得 \_ 授權 \_ 資料** 結構的指標。        |
| WMT \_ 沒有任何 \_ 許可權， \_ 例如           | **WM \_ 取得 \_ 授權 \_ 資料** 結構的指標。        |
| WMT \_ 需要具有 \_ 個人化 | NULL。                                                       |
| WMT \_ 賦予            | **WM \_ 賦予 \_ 狀態** 結構的指標。     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**DirectShow QASF 參考**](directshow-qasf-reference.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




