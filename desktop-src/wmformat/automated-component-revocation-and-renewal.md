---
title: 自動化元件撤銷和更新
description: 自動化元件撤銷和更新
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media Format SDK、自動撤銷和更新
- Windows Media Format SDK，撤銷
- Windows Media Format SDK，續約
- 數位版權管理 (DRM) 、自動化撤銷和更新
- DRM (數位版權管理) 、自動化撤銷和更新
- 數位版權管理 (DRM) ，撤銷
- DRM (數位版權管理) ，撤銷
- 數位版權管理 (DRM) ，續約
- DRM (數位版權管理) ，續約
- DRM 用戶端擴充 Api、自動化撤銷和更新
- 用戶端擴充 Api、自動化撤銷和更新
- DRM 用戶端擴充 Api，撤銷
- 用戶端擴充 Api，撤銷
- DRM 用戶端擴充 Api，更新
- 用戶端擴充 Api，續約
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316000"
---
# <a name="automated-component-revocation-and-renewal"></a>自動化元件撤銷和更新

Microsoft 會撤銷被視為遭入侵的軟體應用程式或元件。 Windows Media Format 用戶端擴充 API 提供自動撤銷和更新元件的機制。

撤銷的元件會列在由 Microsoft 發佈的憑證撤銷清單中。 撤銷元件時，會將其憑證新增到憑證撤銷清單中，並在 Microsoft 伺服器上更新撤銷資訊 BLOB (REV \_ 資訊) 。

若要在使用者嘗試處理 Windows Media 受 DRM 保護的內容時執行自動撤銷和更新，您的應用程式必須執行下列動作：

1.  \_從授權中解壓縮 REV INFO 版本。 REV \_ INFO 版本號碼位於 XMR 授權中的下列位置：
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  藉 \_ \_ 由呼叫 [**IWMDRMSecurity：： GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) 方法，將授權的修訂資訊版本號碼與本機存放區中的 rev info 版本號碼進行比較。
3.  如果 REV \_ 資訊版本不是最新版本，請呼叫 [**IWMDRMSecurity：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) 方法，並 \_ \_ \_ \_ 在 *dwFlags* 參數中傳遞 WMDRM 安全性執行撤銷重新整理旗標。
4.  藉由呼叫 [**IWMDRMSecurity：： GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) 方法，從本機存放區取出憑證撤銷清單。
5.  剖析撤銷清單，並檢查 Windows Media DRM 撤銷。 如需詳細資訊，請參閱 [檢查憑證撤銷](checking-certificate-revocation.md)。
6.  如果有任何 Windows Media DRM 撤銷：
    1.  藉由呼叫 [**IWMDRMSecurity：： GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) 方法，建立內容啟用程式以更新撤銷的元件。
    2.  呼叫 **IMFContentEnabler：： AutomaticEnable** ，以將使用者導向包含元件續約資訊的 URL。 此方法記載于 [媒體基礎 SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx) 。
        > [!Note]  
        > 您必須使用隱私權聲明來向使用者說明此程式，因為更新程式會將用戶端電腦的資訊傳送至 Microsoft 網站。

         

    3.  如果可能的話，使用者將會自動或依照特定指示，從 URL 更新元件。 在某些情況下，元件無法更新。
    4.  請嘗試再次存取內容，直到沒有其他撤銷，或由於某些原因而停止進程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](drm-programming-guide.md)
</dt> </dl>

 

 