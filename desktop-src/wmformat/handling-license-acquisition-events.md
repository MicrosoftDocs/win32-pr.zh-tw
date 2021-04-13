---
title: 處理授權取得事件
description: 處理授權取得事件
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media Format SDK，處理授權取得事件
- Windows Media Format SDK，授權取得事件
- Advanced Systems Format (ASF) ，處理授權取得事件
- ASF (Advanced Systems Format) ，處理授權取得事件
- Advanced Systems Format (ASF) 、授權取得事件
- ASF (Advanced Systems Format) 、授權取得事件
- 數位版權管理 (DRM) ，處理授權取得事件
- DRM (數位版權管理) ，處理授權取得事件
- 數位版權管理 (DRM) 、授權取得事件
- DRM (數位版權管理) 、授權取得事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374470"
---
# <a name="handling-license-acquisition-events"></a>處理授權取得事件

在其 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法中，已啟用 DRM 的讀取器應用程式會處理下列四個與授權取得程式相關的事件：

-   **WMT \_ LICENSEURL 簽章 \_ \_ 狀態**
-   **WMT \_ 無 \_ 許可權**
-   **WMT \_ 沒有任何 \_ 許可權， \_ 例如**
-   **WMT \_ 取得 \_ 授權**

**WMT \_ LICENSEURL 簽章 \_ \_ 狀態**

當 DRM 元件偵測到受 DRM 版本7保護的內容時，它會先在本機系統上尋找有效的授權。 如果不存在，則會在檔案的 DRM 標頭中評估授權取得 URL，並將 *pValue* 設定為其中一個 [**WMT \_ DRMLA \_ 信任**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust)值的 **WMT LICENSEURL 簽章 \_ \_ \_ 狀態** 事件，指出 URL 是否受信任、未受信任或已遭修改。 如果 URL 不受信任，則應用程式應該警告使用者。 如果 URL 已遭修改，則應該將檔案視為損毀，而且應用程式不應該在不發出強烈警告的情況下流覽至 URL。

**WMT \_ 無 \_ 許可權**

**WMT 「 \_ 沒有 \_ 許可權**」事件只會傳送給 DRM 第1版內容，這表示必須以非無訊息方式取得授權。 換句話說，使用者必須流覽至網頁才能取得授權。 頁面的 URL 會從 **OnStatus** 方法中的 *pValue* 參數，以寬字元的 null 終止字串形式取出。

如果有的話，應用程式可讓使用者更輕鬆地流覽至網頁，方法是在不同的進程中開啟 Internet Explorer，或是裝載網頁瀏覽器控制項。 但是，這不是必要的。 應用程式至少可以在訊息方塊中顯示使用者的 URL，並提示他們將它貼入 Internet Explorer 的 [網址] 列。 >audioplayer 範例會示範如何正確處理 **WMT \_ 無 \_ 許可權** 事件，包括如何格式化 URL 字串，以及如何使用 **CreateProcess** 方法開啟 INTERNET EXPLORER 並流覽至指定的 URL。

因為應用程式無法得知何時取得 DRM 第1版授權，所以使用者必須在取得授權之後再次嘗試開啟檔案。

這個相同的非無訊息授權取得程式也可以用於版本7授權，但在此情況下，應用程式可以先呼叫 [**IWMDRMReader：： MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition)。 這個方法將會重複檢查本機授權存放區，直到找到新檔案的授權為止。 屆時，應用程式將會收到 **WMT \_ 取得 \_ 授權** 事件。 針對所有版本7的授權，建議應用程式提供使用者以無訊息方式或非無訊息方式取得授權的選項。

**WMT \_ 沒有任何 \_ 許可權， \_ 例如**

**WMT \_ NO \_ RIGHTS \_ EX** 事件表示內容受到 DRM 版本7的保護，因此授權取得程式可以無訊息方式或以無訊息方式進行。 一般情況下，使用者的無訊息授權取得較方便，但有些人偏好以非無訊息方式取得所有授權。 當授權取得要求使用者提交付款或個人資訊時，應一律以非無訊息模式執行此流程。 非無訊息授權取得的說明位於 **WMT \_ NO \_ RIGHTS** 標題之下。 無訊息取得會繼續進行，如下所示：

1.  將 *pValue* 參數轉換為 [**WM \_ GET \_ 授權 \_ 資料**](wm-get-license-data.md) 結構，並儲存結構，以防稍後在非無訊息授權取得時需要它。
2.  呼叫讀取器物件上的 **QueryInterface** 來取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) 介面。
3.  呼叫 [**IWMDRMReader：： AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) ，並在 *dwFlags* 參數中指定0x1 以表示無訊息語言取得。 這是非同步呼叫，會立即傳回。
4.  等候 **WMT \_ 取得 \_ 授權** 事件。

**WMT \_ 取得 \_ 授權**

**WMT \_ 取得 \_ 授權** 事件會在取得 DRM 第7版授權的授權取得程式完成之後傳送。 [**IWMDRMReader：： AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) 會導致傳送此事件以進行無訊息取得，而 [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) 則會將它傳送給非無訊息的取得。 在您的事件處理常式中，將 *pValue* 轉換為 [**WM \_ GET \_ 授權 \_ 資料**](wm-get-license-data.md) 結構的指標，並檢查 **hr** 成員以判斷是否成功取得授權。 如果 **hr** 等於 NS \_ E \_ DRM \_ 沒有任何 \_ 許可權，則表示授權必須以非無訊息的方式取得。 應用程式應可讓使用者隨時取消授權取得程式。 這是藉由呼叫 [**IWMDRMReader：： CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition)來完成。 呼叫這個方法將會傳送 **WMT \_ 取得 \_ 授權** 事件，其 **HRESULT** 值為 NS \_ S 的 \_ DRM 已 \_ \_ 取消。

如果已取得 **hr** 等於 NS \_ S \_ \_ 的 DRM 授權，則 \_ 會取得授權，而且應用程式可以嘗試播放該檔案，或將它複製到裝置，或執行任何已要求許可權的動作。

在 Windows XP 上引進了新的錯誤碼： NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED。 每當 Windows XP 上的 Windows Media Format 執行時間元件無法在無訊息授權取得期間取得授權時，就會產生此錯誤碼。 在其他平臺上， \_ \_ \_ \_ \_ 當授權取得失敗時，通常會傳回 NS E DRM 授權存放區錯誤。 新的錯誤碼旨在區別授權取得失敗，以及 \_ 產生 NS E \_ DRM \_ 授權 \_ 存放區 \_ 錯誤的其他失敗情況。

下列程式碼片段會顯示在無訊息授權取得嘗試之後傳回這些錯誤的建議方式：


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**讀取受保護的檔案**](reading-protected-files.md)
</dt> </dl>

 

 




