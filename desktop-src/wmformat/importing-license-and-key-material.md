---
title: 匯入授權和金鑰內容
description: 匯入授權和金鑰內容
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows媒體格式 SDK，DRM 匯入
- Windows媒體格式 SDK，匯入
- Windows媒體格式 SDK，授權
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 、金鑰材料
- DRM (數位版權管理) 、金鑰材料
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- DRM 用戶端擴充 Api，金鑰材料
- 用戶端擴充 Api，金鑰材料
- 授權，匯入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9852102ab282c983488c2e5c35b7187bf0daccb62d347c312d1afb343b60f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702502"
---
# <a name="importing-license-and-key-material"></a>匯入授權和金鑰內容

如果您的媒體內容是使用協力廠商內容保護系統進行加密，而您想要將授權和金鑰內容匯入 Windows 媒體 DRM 中，請遵循下列步驟：

1.  藉由呼叫 [**IWMDRMSecurity：： GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)方法，取出 Windows 媒體 DRM 電腦憑證集合。
2.  剖析憑證集合，以確保其已正確簽署，並驗證為已知的 Microsoft 根公開金鑰。 憑證集合符合 XMR 架構。 如需詳細資訊，請參閱 [建立 XMR 授權](building-an-xmr-license.md)。
3.  選擇性：藉由呼叫 [**IWMDRMSecurity：： GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) 方法，將撤銷清單解壓縮。
4.  選擇性：確定未撤銷集合中的任何憑證。 如需詳細資訊，請參閱 [檢查憑證撤銷](checking-certificate-revocation.md)。
5.  產生 XMR 格式的授權，以代表匯入內容的原則需求，並包含適當的 Windows 媒體 DRM 金鑰內容。 如需詳細資訊，請參閱 [建立 XMR 授權](building-an-xmr-license.md)的主題。
6.  使用 [**IWMDRMLicenseManagement：： StoreLicense**](iwmdrmlicensemanagement-storelicense.md)方法，將 XMR 授權傳遞給 Windows 媒體 DRM 系統進行處理。

> [!Note]  
> 當您 Windows 媒體 DRM 的授權時，將會為您提供有關 XMR 架構的詳細資料。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檢查憑證撤銷**](checking-certificate-revocation.md)
</dt> <dt>

[**建立 XMR 授權**](building-an-xmr-license.md)
</dt> <dt>

[**DRM 匯入**](drm-import.md)
</dt> </dl>

 

 




