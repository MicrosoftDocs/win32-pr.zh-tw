---
title: 使用 DRM 7 版或更新版本保護檔案
description: 使用 DRM 7 版或更新版本保護檔案
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows Media Format SDK，建立受保護的檔案
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，建立受保護的檔案
- ASF (Advanced Systems Format) ，建立受保護的檔案
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- Advanced Systems Format (ASF) ，WMStubDRM .lib
- ASF (Advanced Systems Format) ，WMStubDRM .lib
- WMStubDRM .lib，建立受保護的檔案
- WMStubDRM .lib，受保護的檔案
- 數位版權管理 (DRM) ，WMStubDRM .lib
- DRM (數位版權管理) ，WMStubDRM .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee809ea73401f22e4554e74c2ecb8855a0384e0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106999792"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>使用 DRM 7 版或更新版本保護檔案

若要使用 Windows Media DRM 7 版或更新版本保護檔案，請使用寫入器物件的 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 方法來設定 DRM 屬性。 由於 DRM 7 版和更新版本為每個受保護的檔案或一組檔案啟用了唯一的授權，因此 **IWMDRMWriter** 介面也有建立金鑰的方法。 只為了方便起見，提供這些方法。

若要使用 DRM 7 版或更新版本來保護 ASF 檔案，請執行下列步驟：

1.  連結至 WMStubDRM .lib，如有必要，請將 wmvcore 取消連結。
2.  呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數來建立 DRM 寫入器。 第一個引數是保留的，而且必須設定為 **Null**。
3.  藉由呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 或 [**IWMWriter：： SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)，設定要使用之寫入器的設定檔。 設定任何 DRM 屬性之前，您必須先在寫入器中設定設定檔。 只有使用 Windows Media 音訊或 Windows Media 視訊編解碼器的設定檔支援 DRM
4.  取得寫入器物件的 [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) 介面。
5.  呼叫 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) ，並將 [ [**使用 \_ Advanced \_ DRM**](use-advanced-drm.md) ] 設定為 [ **TRUE**]。
6.  如果您需要產生新的金鑰種子，請呼叫 [**IWMDRMWriter：： GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed)。 在大多數情況下，您將會重複使用先前產生的金鑰種子。 此值必須保持秘密;它不會寫入檔案中。
7.  呼叫 [**IWMDRMWriter：： GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) 來建立金鑰識別碼，這是用來建立實際金鑰的第二個值。 與金鑰種子不同的是，金鑰識別碼是公用的，而且會以純文字方式寫入 DRM 標頭中的檔案。 為您建立的每個新檔案建立新的金鑰識別碼。
8.  如有需要，請呼叫 **IWMDRMWriter：： GenerateSigningKeyPair** ，以產生將用來簽署 ADVANCED DRM ASF 標頭物件的公開和私密金鑰。 如需這些金鑰的詳細資訊，請參閱 [**IWMDRMWriter：： GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair)。
9.  如有必要，請取得值以填入 DRM 標頭的數位簽章物件。 如果您的系統上沒有安裝 Windows Media Rights Manager 的工作版本，您必須指定下列四個屬性（全部都必須從 Microsoft 取得）來設定 ASF 檔案標頭的數位簽章物件：

    -   [**DRM \_ LASignatureRootCert**](drm-lasignaturerootcert.md)
    -   [**DRM \_ LASignatureCert**](drm-lasignaturecert.md)
    -   [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)
    -   [**DRM \_ LASignaturePrivKey**](drm-lasignatureprivkey.md)

    如果您已安裝 Windows Media Rights Manager，就不需要在應用程式中設定這些屬性。 DRM 元件會取得這些屬性，並使用它們來自動簽署標頭。 如果您在另一部電腦上有 Windows Media Rights Manager 的啟用版本，而且想要重複使用這些數位簽章物件值，您可以在登錄中找到它們。 授權伺服器憑證會儲存在 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ microsoft \\ wm rights manager \\ 授權伺服器憑證 \\ ： cert1，並將根憑證儲存在 HKEY \_ Local \_ machine \\ software \\ microsoft \\ wm rights manager \\ 授權伺服器 \\ 證書： cert2。 使用 DRM 版本7保護檔案時，您必須使用這些登錄機碼中的值。 針對 **DRM \_ LASignaturePrivKey 屬性**，請使用 **GenerateSigningKeysEx** (透過 Windows media rights manager SDK) 或重複使用 WINDOWS media rights manager 在 HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ WM Rights manager \\ 授權伺服器： Info \_ Cert0 中所安裝的值。 針對 **DRM \_ LASignatureCert** 屬性，請使用 **GenerateSigningKeysEx** (透過 Windows media Rights manager SDK) ，或使用 WINDOWS media rights manager 在 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ WM Rights manager \\ 授權伺服器憑證 \\ ： cert0 下安裝的值。

10. 視需要呼叫 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) ，以設定寫入器物件，此物件會視需要設定必要的 DRM 標頭屬性。 這些屬性會保存在寫入器物件的存留期內，或直到以新值重設為止。 您所建立的每個新檔案都不需要重設它們。

    寫入器物件需要下列屬性：

    -   [**DRM \_ HeaderSignPrivKey**](drm-headersignprivkey.md)
    -   [**DRM \_ KeySeed**](drm-keyseed.md)
    -   [**DRM \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)
    -   [**DRM \_ KeyID**](drm-keyid.md)
    -   [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md)

    以下是選擇性屬性：

    -   [**DRM \_ ContentID**](drm-contentid.md)
    -   [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md)

    此外，您也可以使用 [**DRM \_ DRMHeader**](drm-drmheader.md) 基底屬性，直接指定使用者定義的 DRM 檔案屬性。 您可以新增任何您想要的其他屬性，例如 "DRMHeader. RequireSAP"，以傳達授權伺服器將在建立授權時使用的其他資訊。 授權伺服器必須事先知道您新增的任何其他屬性。 無法以程式設計方式探索未知的屬性。

11. 使用 [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) 介面方法來寫入檔案，如本檔中的其他位置所述。 若要建立即時 DRM 串流，只要寫入網路接收即可。 您也可以寫入至推送接收器。
12. 如有必要，請使用 Windows Media Rights Manager 建立檔案的授權。 這項工作也可以由協力廠商授權伺服器執行。 針對即時 DRM 案例，終端使用者必須在串流開始之前，或在第一次嘗試連接時取得授權。

**注意** 此 SDK 的 x64 版本不支援 DRM。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**屬性**](attributes.md)
</dt> <dt>

[**DRM 屬性清單**](drm-attribute-list.md)
</dt> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> <dt>

[**IWMDRMWriter 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**IWMWriter 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**讀取受保護的檔案**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




