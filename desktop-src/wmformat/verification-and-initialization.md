---
title: 驗證與初始化
description: 驗證與初始化
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK，驗證
- Windows Media Format SDK，初始化
- 數位版權管理 (DRM) ，驗證
- DRM (數位版權管理) ，驗證
- 數位版權管理 (DRM) ，初始化
- DRM (數位版權管理) ，初始化
- DRM 用戶端擴充 Api，驗證
- 用戶端擴充 Api，驗證
- DRM 用戶端擴充 Api，初始化
- 用戶端擴充 Api，初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314310"
---
# <a name="verification-and-initialization"></a>驗證與初始化

您應該執行下列步驟來確認是否允許 transcryption，以及初始化將會解密內容的物件：

1.  如果您已經有內容的金鑰識別碼，請跳至步驟5。
2.  呼叫 [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) 函式來建立中繼資料編輯器物件，並取得該物件之 [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) 介面的實例。
3.  呼叫 **IWMMetadataEditor：： QueryInterface** 以取得 [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) 介面的實例。
4.  呼叫 [**IWMDRMEditor：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) 以取得 **DRM \_ DRMHeader \_ KeyID** 屬性。
5.  藉由呼叫 [**WMDRMStartup**](wmdrmstartup.md) 函式來初始化 WINDOWS Media DRM 用戶端擴充 api。
6.  呼叫 [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) 函數來建立安全的提供者物件，並取得該物件之 [**IWMDRMProvider**](iwmdrmprovider.md) 介面的實例。
7.  呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md) 來建立授權管理物件，並取得其 [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) 介面的實例。
8.  呼叫 [**IWMDRMLicenseManagement：： CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)，並傳入金鑰識別碼和許可權，以控制在 transcrypted 後要對內容採取的動作。 此呼叫將會抓取 [**IWMDRMLicense**](iwmdrmlicense.md) 介面的實例，可用來列舉任何相符的授權。
9.  呼叫 [**IWMDRMLicense：： GetInclusionList**](iwmdrmlicense-getinclusionlist.md) ，以根據授權簽發者所指定 (CPS) 取得授權的內容保護系統清單。
10. 剖析包含清單，以確認授權允許輸出 CPS 的 GUID。
11. 如果所需的匯出 GUID 不在包含清單中，請呼叫 [**IWMDRMLicense：： GetNext**](iwmdrmlicense-getnext.md) 來取得下一個適用的授權 (如果有任何) ，然後重複步驟9和10。 如果沒有任何授權在其內含清單中具有所需的 GUID，則無法執行匯出。
12. 呼叫 [**IWMDRMLicense：： CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) 來建立解密器物件。 傳入匯出應用程式憑證。 此呼叫將提供指向解密程式物件之 [**IWMDRMDecrypt**](iwmdrmdecrypt.md) 介面實例的指標，以及包含種子的二進位物件。 目前只支援 Windows Media **DRM \_ 保護 \_ 類型 \_ RC4** 常數作為 *dwFlags* 參數的引數。
13. 使用 RSA OAEP 加密配置來解密初始化向量。
14. 當您輸入 Windows Media DRM 匯出協定時，請使用 Microsoft 提供的 ASF 剖析程式庫，找出每個承載的位移（以位元組為單位）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**匯出壓縮的內容**](exporting-compressed-content.md)
</dt> </dl>

 

 




