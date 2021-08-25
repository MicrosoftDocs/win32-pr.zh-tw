---
title: IWMDRMSecurity 介面
description: IWMDRMSecurity 介面會管理用戶端電腦和數位版權管理 (DRM) 子系統的各種安全性相關資訊。若要取得這個介面的實例，請呼叫 IWMDRMProvider CreateObject。
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- IWMDRMSecurity 介面 windows 媒體格式
- IWMDRMSecurity 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31593dda35e7fa33540faa3c954f1901e1afa227372b25326c0f36154d443153
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839730"
---
# <a name="iwmdrmsecurity-interface"></a>IWMDRMSecurity 介面

**IWMDRMSecurity** 介面會管理用戶端電腦和數位版權管理 (DRM) 子系統的各種安全性相關資訊。

若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。 將 **IID \_ IWMDRMSecurity** 傳遞為 *riid* 參數。

## <a name="members"></a>成員

**IWMDRMSecurity** 介面繼承自 [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)。 **IWMDRMSecurity** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMSecurity** 介面具有這些方法。



| 方法                                                                                      | 描述                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md)                     | 判斷憑證是否已撤銷。<br/>                                                    |
| [**GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | 抓取內容啟用程式介面，以根據已撤銷的憑證來更新元件。<br/> |
| [**GetContentEnablersFromHashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | 抓取可根據雜湊憑證來更新元件的內容啟用程式介面。<br/>  |
| [**GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | 抓取用戶端電腦上 DRM 子系統的電腦憑證。<br/>                        |
| [**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)                               | 從本機存放區抓取憑證撤銷清單。<br/>                                         |
| [**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)                 | 抓取本機存放區中憑證撤銷清單的版本號碼。<br/>                     |
| [**GetSecurityVersion**](iwmdrmsecurity-getsecurityversion.md)                             | 抓取用戶端電腦上的 DRM 子系統版本。<br/>                                    |
| [**PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md)                       | 在用戶端電腦上起始對 DRM 子系統的安全性更新。<br/>                              |
| [**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)                               | 在本機存放區中設定憑證撤銷清單。<br/>                                                |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 的個人化範例**](drm-individualization-example.md)
</dt> <dt>

[**介面**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





