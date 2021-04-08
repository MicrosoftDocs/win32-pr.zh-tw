---
title: 如何建立應用程式套件簽署憑證
description: 瞭解如何使用 MakeCert.exe 和 Pvk2Pfx.exe 來建立測試程式碼簽署憑證，讓您可以簽署 Windows 應用程式套件。
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023300"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>如何建立應用程式套件簽署憑證

> [!IMPORTANT]
> MakeCert.exe 已被取代。 如需建立憑證的目前指導方針，請參閱 [建立封裝簽署的憑證](/windows/msix/package/create-certificate-package-signing)。

 

瞭解如何使用 [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) 和 [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) 來建立測試程式碼簽署憑證，讓您可以簽署 Windows 應用程式套件。

您必須在部署封裝的 Windows 應用程式之前，先對其進行數位簽署。 如果您未使用 Microsoft Visual Studio 2012 來建立和簽署應用程式套件，則需要建立及管理您自己的程式碼簽署憑證。 您可以使用 [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) 建立憑證，並 [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) Windows 驅動程式套件 (WDK) 。 然後，您可以使用憑證來簽署應用程式套件，以便在本機部署以進行測試。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [應用程式封裝和部署](/previous-versions/windows/apps/hh464929(v=win.10))
-   [簽署驅動程式的工具](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>必要條件

-   從 WDK [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert)和 [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)工具

## <a name="instructions"></a>指示

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>步驟1：決定封裝的發行者名稱

若要讓您建立的簽署憑證可與您要簽署的應用程式套件搭配使用，簽署憑證的主體名稱必須符合該應用程式之 AppxManifest.xml 中 [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity)元素的 **發行者** 屬性。 例如，假設 AppxManifest.xml 包含：

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

針對您在下一個步驟中使用 [**MakeCert**](/windows-hardware/drivers/devtest/makecert)公用程式指定的 *publisherName* 參數，請使用 "CN = contoso Software，O = contoso CORPORATION，C = US"。

> [!Note]  
> 此參數字串以引號指定，且區分大小寫和空白字元。

 

針對 AppxManifest.xml 中的 [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity)專案定義的發行者屬性字串，必須與您使用 [憑證主體名稱 **]** 的 [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n 參數指定的字串相同。 盡可能複製並貼上字串。

### <a name="step-2-create-a-private-key-using-makecertexe"></a>步驟2：使用 MakeCert.exe 建立私密金鑰

使用 [**MakeCert**](/windows-hardware/drivers/devtest/makecert) 公用程式來建立自我簽署的測試憑證和私密金鑰：

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

此命令會提示您提供 pvk 檔案的密碼。 建議您選擇 [強式密碼](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) ，並將您的私密金鑰放在安全的位置。

基於下列原因，我們建議您在上述範例中使用建議的參數：

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

建立自我簽署的根憑證。 這可簡化您的測試憑證管理。

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

將憑證的基本條件約束標示為終端實體。 這可防止憑證用來作為憑證授權單位單位， (可發出其他憑證的 CA) 。

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

設定憑證 (EKU) 值的增強金鑰使用方法。

> [!Note]  
> 請勿在兩個逗號分隔值之間加上空格。

 

-   1.3.6.1.5.5.7.3.3 表示憑證對程式碼簽署有效。 一律指定此值以限制憑證的預期用途。
-   1.3.6.1.4.1.311.10.3.13 指出憑證遵循存留期簽署。 一般來說，如果簽章是時間戳記，只要憑證在時間戳記的時間點有效，簽章仍會保持有效，即使憑證過期也一樣。 無論簽章是否已加上時間戳記，這個 EKU 都會強制簽章過期。

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

設定憑證的到期日。 以 mm/dd/yyyy 格式提供 *expirationDate* 參數的值。 建議您只針對測試用途（通常不到一年），選擇只需一段時間的到期日。 此到期日與存留期簽署 EKU 結合，有助於限制憑證可能遭到入侵和誤用的時間範圍。

</dd> </dl>

如需其他選項的詳細資訊，請參閱 [**MakeCert**](/windows-hardware/drivers/devtest/makecert)。

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>步驟3：使用 Pvk2Pfx.exe 建立個人資訊交換 ( .pfx) 檔案

使用 [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) 公用程式，將 [**MakeCert**](/windows-hardware/drivers/devtest/makecert) 建立的 pvk 和 .cer 檔案轉換成可搭配 [SignTool](/windows/desktop/SecCrypto/signtool) 使用的 .pfx 檔案來簽署應用程式套件：

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

*MyKey. pvk* 和 *MyKey .cer* 檔案是在上一個步驟中建立的 [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert)相同檔案。 您可以使用選擇性的/po 參數，為產生的 .pfx 指定不同的密碼;否則，.pfx 的密碼會與 *MyKey. pvk* 相同。

如需其他選項的詳細資訊，請參閱 [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx)。

## <a name="remarks"></a>備註

建立 .pfx 檔案之後，您可以使用 [SignTool](/windows/desktop/SecCrypto/signtool) 檔案來簽署應用程式套件。 如需詳細資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。 但是，除非您將憑證安裝到本機電腦的信任憑證存放區，否則本機電腦仍不會信任憑證來部署應用程式套件。 您可以使用 Windows 隨附的 [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))。

**使用 WindowsCertutil.exe安裝憑證**

1.  以系統管理員身分執行 **Cmd.exe** 。
2.  請執行這個命令：

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

如果不再使用憑證，建議您移除這些憑證。 在相同的系統管理員命令提示字元中，執行此命令：

``` syntax
Certutil -delStore TrustedPeople certID
```

**CertID** 是憑證的序號。 執行此命令以判斷憑證序號：

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>安全性考量

藉由將認證新增至[本機電腦憑證存放區](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores) (英文)，您會對電腦上所有使用者的憑證信任造成影響。 建議您將任何要用於測試應用程式套件的程式碼簽署憑證，安裝到 [受信任的人] 憑證存放區。 當不再需要時，請立即移除這些憑證，以防止它們被用來危害系統信任。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**範例**
</dt> <dt>

[建立應用程式套件範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**概念**
</dt> <dt>

[程式碼簽署最佳作法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md) \(英文\)
</dt> <dt>

[簽署應用程式套件](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 