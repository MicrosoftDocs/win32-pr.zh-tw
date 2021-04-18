---
title: 建立和初始化 DRM 寫入器
description: 建立和初始化 DRM 寫入器
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media Format SDK，DRM 寫入器
- 數位版權管理 (DRM) ，建立 DRM 寫入器
- DRM (數位版權管理) ，建立 DRM 寫入器
- 數位版權管理 (DRM) ，初始化 DRM 寫入器
- DRM (數位版權管理) ，初始化 DRM 寫入器
- DRM 用戶端擴充 Api，DRM 寫入器
- 用戶端擴充 Api，DRM 寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106965872"
---
# <a name="creating-and-initializing-a-drm-writer"></a>建立和初始化 DRM 寫入器

必須執行下列步驟，才能初始化 ASF 寫入器物件，以便在 Windows Media DRM 中匯入加密的媒體範例。

1.  遵循匯 [入授權和金鑰內容](importing-license-and-key-material.md)的步驟1到4。
2.  使用適當的 Windows Media DRM 金鑰內容，建立及初始化 ASF 寫入器物件。 如需詳細資訊，請參閱 [啟用 DRM 支援](enabling-drm-support.md)。
3.  藉由呼叫 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)來設定下列每個屬性：
    -   DRM \_ HeaderSignPrivKey
    -   DRM \_ V1LicenseAcqURL
    -   DRM \_ KeyID
    -   DRM \_ LicenseAcqURL
4.  如果執行軟體的電腦上未安裝 Windows Media Rights Manager 的授權版本，則也必須設定下列四個屬性：
    -   DRM \_ LASignatureRootCert
    -   DRM \_ LASignatureCert
    -   DRM \_ LASignatureLicSrvCert
    -   DRM \_ LASignaturePrivKey
    -   您可以填寫 [Windows Media 授權合約 (WMLA) ](https://www.microsoft.com/licensing/default) online，來完成必要加密憑證的應用程式。
5.  建立工作階段金鑰，並填寫 WMDRM 匯 [**\_ 入 \_ 會話 \_ 金鑰**](wmdrm-import-session-key.md) 結構。 工作階段金鑰將用來加密內容金鑰。 如需範例，請參閱 [建立工作階段金鑰範例](create-session-key-example.md)。
6.  從隨機 RC4 初始化向量建立內容金鑰，並填寫 [**WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰**](wmdrm-import-content-key.md) 結構。 內容金鑰是用來加密媒體範例。 如需範例，請參閱 [建立內容金鑰範例](create-content-key-example.md)。
7.  使用 RC4 加密，以工作階段金鑰加密內容金鑰。
8.  解壓縮電腦憑證集合金鑰。 如需範例，請參閱 [取得電腦憑證範例](get-machine-certificate-example.md)。
9.  使用從憑證解壓縮的公開金鑰來加密工作階段金鑰。
10. 填寫 WMDRM 匯 [**\_ 入 \_ INIT \_ 結構**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) 結構。
11. 呼叫 [**IWMDRMWriter3：： SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) 方法來通知 SDK，進入寫入器的範例已經受到保護，而且應該直接傳送到 WINDOWS Media DRM 用戶端以進行匯入。
12. 呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)。

您可以在 Windows Media Format SDK 程式設計指南中記載建立受 DRM 保護之檔案的其餘步驟。 如需詳細資訊，請參閱 [建立受保護](creating-protected-files.md)的檔案。

下一步是逐一查看每個媒體範例、將其加密，然後將其傳遞至寫入器物件。 如需詳細資訊，請參閱 [加密和匯入媒體範例](encrypting-and-importing-media-samples.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**屬性**](attributes.md)
</dt> <dt>

[**DRM 匯入**](drm-import.md)
</dt> </dl>

 

 




