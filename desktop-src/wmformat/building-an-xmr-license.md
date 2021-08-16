---
title: 建立 XMR 授權
description: 建立 XMR 授權
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows媒體格式 SDK，DRM 匯入
- Windows媒體格式 SDK，匯入
- Windows媒體格式 SDK，XMR 授權
- Windows媒體格式 SDK，授權
- 'Windows媒體格式 SDK，可擴充媒體許可權 (XMR) '
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 、XMR 授權
- DRM (數位版權管理) 、XMR 授權
- '數位版權管理 (DRM) 的可延伸媒體許可權 (XMR) '
- 'DRM (數位版權管理) 、可延伸的媒體許可權 (XMR) '
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api、XMR 授權
- 用戶端擴充 Api、XMR 授權
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- 'DRM 用戶端擴充 Api、可擴充媒體許可權 (XMR) '
- '用戶端擴充 Api，可延伸媒體許可權 (XMR) '
- 授權，XMR
- '可擴充媒體許可權 (XMR) '
- 'XMR (可擴充媒體許可權) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73406d36c6ec7903ee7966f162811336aaecccaac5093e6d467e02c1a56ec71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881399"
---
# <a name="building-an-xmr-license"></a>建立 XMR 授權

若要產生 Windows 媒體 DRM 的授權以進行處理，您必須使用 (XMR) 二進位架構的可延伸媒體許可權。 XMR 是用來傳達媒體許可權和限制的架構，而且需要個別授權。

授權中的重要資料是使用 Windows 媒體 drm 憑證集合中的公開金鑰進行加密，因此只有 Windows 媒體 drm 用戶端擴充 API 子系統才能看到此內容。 .

您必須負責確保授權結構和原則設定有效，且與授權簽發者的意圖一致，而且它們符合合規性規則。

您應該閱讀 Windows 媒體 DRM 匯入合規性規則，以瞭解必須存在於授權中的一組完整 XMR 物件。

若要將 XMR 授權傳遞至 DRM 子系統，請呼叫 [**IWMDRMLicenseManagement：： StoreLicense**](iwmdrmlicensemanagement-storelicense.md) 方法。 使用下列格式，在 *bstrLicenseResponse* 參數中傳遞授權：


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



此字串必須是 Unicode 格式 (UTF-16) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 匯入**](drm-import.md)
</dt> </dl>

 

 




