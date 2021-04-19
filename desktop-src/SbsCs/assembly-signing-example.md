---
description: 下列範例會討論如何產生由組件資訊清單、驗證目錄和元件檔案組成的帶正負號並存元件。
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: 組件簽署範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106986718"
---
# <a name="assembly-signing-example"></a>組件簽署範例

下列範例會討論如何產生由組件資訊清單、驗證目錄和元件檔案組成的帶正負號並存元件。 共用並存元件應該經過簽署。 作業系統會先驗證元件簽章，然後再將共用的元件安裝到全域並存存放區 (WinSxS) 。 這會讓您難以偽造並存元件的發行者。

請注意，在產生元件類別目錄之後變更元件檔或資訊清單內容會使目錄和元件失效。 如果您必須在建立和簽署類別目錄之後更新元件檔或資訊清單，您必須再次簽署該元件，並產生新的目錄。

從元件檔、組件資訊清單和您將用來簽署元件的憑證檔案開始。 憑證檔案必須是2048位或更大。 您不需要使用受信任的憑證。 憑證只能用來驗證元件是否已損毀。

執行 Microsoft Windows 軟體開發套件 (SDK) 所提供的 [Pktextract.exe](pktextract-exe.md) 公用程式，從憑證檔案中解壓縮公開金鑰 token。 若要讓 Pktextract 正常運作，憑證檔案必須存在於與公用程式相同的目錄中。 使用已解壓縮的公開金鑰 token 值，更新資訊清單檔案中 **assemblyIdentity** 元素的 **publicKeyToken** 屬性。

以下是名為 MySampleAssembly 的資訊清單檔案範例。 MySampleAssembly 元件僅包含一個檔案，MYFILE.DLL。 請注意， **assemblyIdentity** 元素的 **publicKeyToken** 屬性值已更新為公開金鑰 token 的值。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

接下來，執行 Windows SDK 所提供的 [Mt.exe](mt-exe.md) 公用程式。 元件檔必須位於與資訊清單相同的目錄中。 在此範例中，這是 MySampleAssembly 目錄。 呼叫範例的 Mt.exe，如下所示：

**c： \\ MySampleAssembly>mt.exe-資訊清單 MySampleAssembly. hashupdate-makecdfs**

以下是執行 Mt.exe 後，範例資訊清單的外觀。 請注意，使用 hashupdate 選項執行 Mt.exe 會新增檔案的 SHA-1 雜湊。 請勿變更此值。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

使用-makecdfs 選項執行 Mt.exe 會產生名為 MySampleAssembly 的檔案，其中描述將用來驗證資訊清單的安全性目錄內容。

下一步是在這個的 Makecat.exe 上執行，以建立元件的安全性目錄。 此範例的 Makecat.exe 呼叫會如下所示：

**c： \\ MySampleAssembly>Makecat MySampleAssembly .manifest**

最後一個步驟是執行 SignTool.exe，以使用憑證簽署類別目錄檔案。 這應該是先前用來產生公開金鑰 token 的相同憑證。 如需 SignTool.exe 的詳細資訊，請參閱 [**SignTool**](../seccrypto/signtool.md) 主題。 範例的 **SignTool** 呼叫會如下所示：

**c： \\ MySampleAssembly>signtool sign/f \<fullpath> mycompany .pfx/du HTTPs： \/ /www.mycompany.com/MySampleAssembly/t HTTPs： \/ /timestamp.digicert.com MySampleAssembly.cat**

如果您有經過驗證的數位憑證，而您的憑證授權單位單位使用 PVK 檔案格式來儲存私密金鑰，您可以使用 PVK 數位憑證檔案匯入工具 (pvkimprt.exe) 將金鑰匯入 (CSP) 的密碼編譯服務提供者中。 此公用程式可讓您匯出至「PFX/P12」的產業標準格式。 如需 PVK 的數位憑證檔案匯入工具的詳細資訊，請參閱 MSDN library 的「部署資源」一節，或洽詢您的憑證授權單位單位。 您可能可以從取得 pvkimprt.exe https://office.microsoft.com/downloads/2000/pvkimprt.aspx 。

另請參閱 [建立已簽署的檔案和目錄](creating-signed-files-and-catalogs.md)。

 

 
