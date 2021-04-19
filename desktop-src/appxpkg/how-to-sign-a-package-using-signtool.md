---
title: 如何使用 SignTool 簽署應用程式套件
description: 瞭解如何使用 SignTool 來簽署您的 Windows 應用程式套件，以便部署。
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106969736"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a>如何使用 SignTool 簽署應用程式套件

> [!Note]  
> 如需簽署 Windows 應用程式套件，請參閱 [使用 SignTool 簽署應用程式套件](/windows/msix/package/sign-app-package-using-signtool)。

 

瞭解如何使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 來簽署您的 Windows 應用程式套件，以便部署。 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 是 WINDOWS 軟體開發套件 (SDK) 的一部分。

所有 Windows 應用程式套件都必須經過數位簽署，才能進行部署。 雖然 Microsoft Visual Studio 2012 和更新版本可以在建立應用程式套件時進行簽署，但您使用應用程式封裝工具建立的封裝 [ (MakeAppx.exe) ](make-appx-package--makeappx-exe-.md) Windows SDK 工具不會簽署。

> [!Note]  
> 您只能使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 來簽署 Windows 8 和更新版本或 windows Server 2012 及更新版本上的 Windows 應用程式套件。 您無法使用 **SignTool** 來簽署舊版作業系統（例如 Windows 7 或 windows Server 2008 R2）上的應用程式套件。

 

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [應用程式封裝和部署](/previous-versions/windows/apps/hh464929(v=win.10))
-   [用來簽署檔案和檢查簽章的工具](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>必要條件

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool)，這是 Windows SDK 的一部分
-   有效的程式碼簽署憑證，例如，使用 [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) 和 [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) 工具建立的個人資訊交換 ( .pfx) 檔案

    如需建立有效程式碼簽署憑證的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。

-   封裝的 Windows 應用程式，例如，使用應用程式封裝工具建立的 .appx 檔案 [ (MakeAppx.exe) ](make-appx-package--makeappx-exe-.md) 工具

**其他考量**

您用來簽署應用程式套件的憑證必須符合下列準則：

-   憑證的主體名稱必須符合封裝中儲存之 AppxManifest.xml 檔案的 [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity)元素所包含的 **發行者** 屬性。 發行者名稱是已封裝之 Windows 應用程式身分識別的一部分，因此您必須讓憑證的主體名稱符合應用程式的發行者名稱。 這可讓您根據數位簽章檢查已簽署套件的身分識別。 如需使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool)簽署應用程式套件時可能產生之簽署錯誤的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)的備註一節。
-   憑證必須有效，才能進行程式碼簽署。 這表示這兩個專案都必須為 true：

    -   憑證的 [擴充金鑰使用方法] (EKU) 欄位必須設定為 [未設定]，或包含 [程式碼簽署 (1.3.6.1.5.5.7.3.3) 的 EKU 值。
    -   憑證的金鑰使用方法 (KU) 欄位必須取消設定或包含數位簽章 (0x80) 的使用位。

-   憑證包含私密金鑰。
-   憑證有效。 它是作用中、尚未過期，而且尚未撤銷。

## <a name="instructions"></a>指示

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>步驟1：決定要使用的雜湊演算法

當您簽署應用程式套件時，您必須使用建立應用程式封裝時所使用的相同雜湊演算法。 如果您使用預設設定來建立應用程式套件，則使用的雜湊演算法是 SHA256。

如果您使用具有特定雜湊演算法的應用程式封裝程式來建立應用程式套件，請使用相同的演算法來簽署套件。 若要判斷用於簽署封裝的雜湊演算法，您可以解壓縮封裝內容，並檢查 AppxBlockMap.xml 的檔案。 [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap)專案的 **HashMethod** 屬性工作表示建立應用程式封裝時所使用的雜湊演算法。 例如：

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

上述 [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) 元素指出使用 SHA256 演算法。 下表列出目前可用演算法的對應：

| **HashMethod** 值                            | 要使用的 *hashAlgorithm* |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 ( .appx 預設)  |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>步驟2：執行 SignTool.exe 來簽署套件

**使用 .pfx 檔案中的簽署憑證簽署套件**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

如果未指定，則 [**SignTool**](/windows-hardware/drivers/devtest/signtool)會將/fd *hashAlgorithm* 參數預設為 sha1，而 sha1 對簽署應用程式封裝而言是不正確。 因此，當您簽署應用程式封裝時，必須指定此參數。 若要簽署使用預設 SHA256 雜湊所建立的應用程式套件，您可以將/fd *hashAlgorithm* 參數指定為 SHA256：

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

如果您使用未受密碼保護的 .pfx 檔案，您可以省略/p *password* 參數。 您也可以使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 所支援的其他憑證選取選項來簽署應用程式套件。 如需這些選項的詳細資訊，請參閱 [SignTool](/windows/desktop/SecCrypto/signtool)。

> [!Note]  
> 您無法在已簽署的應用程式套件上使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 時間戳記操作;不支援此操作。

 

如果您想要為應用程式套件進行時間戳記，您必須在簽署作業期間執行此動作。 例如：

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

讓/tr *timestampServerUrl* 參數等於 RFC 3161 時間戳記伺服器的 URL。

## <a name="remarks"></a>備註

本節討論應用程式套件簽署錯誤的疑難排解。

### <a name="troubleshooting-app-package-signing-errors"></a>針對應用程式套件簽署錯誤進行疑難排解

除了 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 可以傳回的簽署錯誤之外， **SignTool** 也會傳回簽署應用程式套件的特定錯誤。 這些錯誤通常會顯示為內部錯誤：

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

如果錯誤碼以0x8008 開頭，例如 0x80080206 APPX 電子損毀 \_ 的 \_ \_ 內容) ，則表示簽署的套件無效。 在此情況下，您必須先重建套件，才能簽署封裝。 如需0x8008 錯誤的完整清單 \* ，請參閱 [**COM 錯誤碼 (安全性和設定)**](/windows/desktop/com/com-error-codes-4)。

更常見的情況是，錯誤的 0x8007000b (錯誤 \_ \_ 格式) 。 在此情況下，您可以在事件記錄檔中找到更明確的錯誤資訊：

**若要搜尋事件記錄檔**

1.  執行 Eventvwr.msc services.msc。
2.  開啟事件記錄檔：事件檢視器 (本機) > 應用程式和服務記錄 > Microsoft > Windows > AppxPackagingOM > Microsoft Windows-AppxPackaging/Operational
3.  尋找最新的錯誤事件。

內部錯誤通常會對應到下列其中一項：

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>事件識別碼</th>
<th>範例事件字串</th>
<th>建議</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>150</td>
<td>錯誤 0x8007000B: 應用程式資訊清單發行者名稱 (CN=Contoso) 必須符合簽署憑證 (CN=Contoso, C=US) 的主體名稱。</td>
<td>應用程式資訊清單發行者名稱必須完全符合簽署的主體名稱。
<blockquote>
[!Note]<br />
這些名稱會以引號指定，且區分大小寫和空白字元。
</blockquote>
<br/> 您可以更新為 AppxManifest.xml 檔中的<a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a>專案定義的<strong>發行者</strong>屬性字串，以符合所需簽署憑證的主體名稱。 或者，選取具有與應用程式資訊清單發行者名稱相符之主體名稱的不同簽署憑證。 資訊清單發行者名稱和憑證主體名稱都會列在事件訊息中。</td>
</tr>
<tr class="even">
<td>151</td>
<td>錯誤 0x8007000B: 指定的簽章雜湊方法 (SHA512) 必須符合應用程式套件區塊對應中使用的雜湊方法 (SHA256)。</td>
<td>在/fd 參數中指定的 hashAlgorithm 不正確 (請參閱步驟1：判斷要使用的雜湊演算法) 。 使用符合應用程式套件區塊對應的 hashAlgorithm 重新執行 <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> 。</td>
</tr>
<tr class="odd">
<td>152</td>
<td>錯誤 0x8007000B: 應用程式套件內容必須通過區塊對應的驗證。</td>
<td>應用程式套件損壞，需要重建產生新區塊對應。 如需建立應用程式套件的詳細資訊，請參閱使用 <a href="make-appx-package--makeappx-exe-.md">應用程式封裝程式</a> 建立應用程式套件或 <a href="/previous-versions/hh975357(v=vs.110)">使用 Visual Studio 2012 建立應用程式套件</a>。</td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a>安全性考量

簽署封裝之後，您用來簽署套件的憑證仍然必須由要部署封裝的電腦所信任。 藉由將認證新增至[本機電腦憑證存放區](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores) (英文)，您會對電腦上所有使用者的憑證信任造成影響。 建議您將任何要用於測試應用程式套件的程式碼簽署憑證，安裝到 [受信任的人] 憑證存放區，並在不再需要時立即移除這些憑證。 如果您建立自己的測試憑證來簽署應用程式套件，我們也建議您限制與測試憑證相關聯的許可權。 如需建立測試憑證以簽署應用程式套件的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。

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

[在 Visual Studio 2012 中簽署套件](/previous-versions/br230260(v=vs.110))
</dt> <dt>

[SignTool](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[應用程式封裝工具 (MakeAppx.exe) ](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

