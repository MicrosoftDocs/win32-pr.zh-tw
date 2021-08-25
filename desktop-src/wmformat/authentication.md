---
title: '驗證 (Windows 媒體格式 11 SDK) '
description: 驗證
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows媒體格式 SDK，驗證
- Windows媒體格式 SDK，網路驗證
- Advanced Systems Format (ASF) 、驗證
- ASF (Advanced 系統格式) 、驗證
- Advanced Systems Format (ASF) ，網路驗證
- ASF (Advanced Systems Format) ，網路驗證
- 驗證 (authentication)
- 網路驗證，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee276bc2800ad7f2d5fa94f00e282dc7d4f5402396d69eb7e3b240fd4303f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007118"
---
# <a name="authentication-windows-media-format-11-sdk"></a>驗證 (Windows 媒體格式 11 SDK) 

讀取器物件可以處理網路驗證挑戰，包括摘要式驗證和 NTLM 驗證。 在某些情況下，應用程式必須透過回呼介面提供使用者的認證：

-   摘要式驗證：應用程式必須執行 **IWMCredentialCallback** 介面，如本主題稍後所述。
-   NTLM 驗證：讀取器會自動回應使用者的登入認證。 如果目前的使用者已獲授權登入伺服器，則應用程式不需要執行任何動作。 如果使用者沒有授權，應用程式必須執行 **IWMCredentialCallback** 介面。

    > [!Note]  
    > Windows Media Services 版本4.1 不支援透過 proxy 伺服器進行 NTLM 驗證。 NTLM 驗證需要相同連線上的數個用戶端-伺服器交換，而4.1 版則不會持續與 proxy 的連接。 Microsoft Windows Server 2003 Windows Media Services 9 系列支援透過 proxy 伺服器進行 NTLM 驗證，只要 proxy 支援 keep-alive 連線即可。

     

如所述，在某些情況下，應用程式必須提供使用者的認證。 這會透過 **IWMCredentialCallback** 介面發生，該介面具有單一方法 **AcquireCredentials**。 若要支援驗證，請在您的應用程式中執行這個介面。 讀取器物件會藉由在 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)方法中從應用程式收到的 [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)指標上呼叫 **QueryInterface** ，來查詢此介面。 如果讀取器物件需要取得使用者的認證，則會呼叫應用程式的 **AcquireCredentials** 方法。

如果透過網路傳送認證時沒有加密，則讀取器會 \_ \_ \_ 在 *PDWFLAGS* 參數中設定 WMT 認證純文字旗標。 這可讓應用程式有機會警告使用者其認證將以純文字傳送。

否則，讀取器物件會自動加密認證，然後再透過網路傳送。 應用程式可將其以純文字格式傳回給 reader 物件。 此外，如果讀取器物件設定 WMT \_ 認證 \_ 加密旗標，則表示讀取器支援從應用程式取得加密的認證。 在此情況下，應用程式可以使用純文字格式傳回認證，或使用 **CryptProtectData** 函式將其本身加密，如 Platform SDK 檔中所述。 如果應用程式加密認證，它必須 \_ \_ 在方法傳回之前，在 *pdwFlags* 參數中設定 WMT 認證加密旗標。

一般而言，不需要將資料加密，因為必要時，讀取器物件會加密資料。 但是，如果應用程式將使用者名稱和密碼保存在記憶體中，加密可能會很有用，因為它可防止攻擊者檢查進程的記憶體傾印。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMCredentialCallback 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




