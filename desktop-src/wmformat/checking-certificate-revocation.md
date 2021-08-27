---
title: 檢查憑證撤銷
description: 檢查憑證撤銷
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows媒體格式 SDK，DRM 匯入
- Windows媒體格式 SDK，匯入
- Windows媒體格式 SDK，憑證撤銷
- Windows媒體格式 SDK，撤銷憑證
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) ，憑證撤銷
- DRM (數位版權管理) ，憑證撤銷
- 數位版權管理 (DRM) ，撤銷憑證
- DRM (數位版權管理) ，撤銷憑證
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api，憑證撤銷
- 用戶端擴充 Api，憑證撤銷
- DRM 用戶端擴充 Api，撤銷憑證
- 用戶端擴充的 Api，撤銷憑證
- 憑證，撤銷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d9f8aaa299873513f88a2be258cf2ddd96147934e461cbde49630542fd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028066"
---
# <a name="checking-certificate-revocation"></a>檢查憑證撤銷

將內容匯入 Windows 媒體 DRM 時，您必須確認此集合中沒有任何憑證在撤銷清單中，以確定憑證集合中沒有任何憑證遭到撤銷。 撤銷清單是使用 [**IWMDRMSecurity：： GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) 方法來解壓縮。

然後，您可以使用 [**IWMDRMSecurity：： CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) 方法來確認憑證未被撤銷。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 匯入**](drm-import.md)
</dt> </dl>

 

 




