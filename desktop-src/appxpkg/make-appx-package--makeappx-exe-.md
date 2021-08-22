---
title: App 封裝工具 (MakeAppx.exe)
description: 應用程式封裝工具 (MakeAppx.exe) 會從磁片上的檔案建立應用程式套件，或將檔案從應用程式封裝解壓縮至磁片。
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a75f2eede20ac21fb3b2c1f03a583f31b2e05f69363e5a21c37b1215d3ebf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410748"
---
# <a name="app-packager-makeappxexe"></a>App 封裝工具 (MakeAppx.exe)

> [!Note]  
> 如需使用此工具的 UWP 指引，請參閱使用 [MakeAppx.exe 工具建立應用程式套件](/windows/msix/package/create-app-package-with-makeappx-tool)。

 

應用程式封裝工具 (MakeAppx.exe) 會從磁片上的檔案建立應用程式套件，或將檔案從應用程式封裝解壓縮至磁片。 從 Windows 8.1 開始，應用程式封裝程式也會從磁片上的應用程式套件建立應用程式套件套件組合，或將應用程式套件套件組合中的應用程式套件解壓縮至磁片。 它包含在 Microsoft Visual Studio 和 Windows 軟體開發套件 (sdk) ，適用于 Windows 8 Windows 軟體開發套件或 () sdk Windows 8.1。 造訪 [下載以供開發人員]( https://msdn.microsoft.com/windows/apps/br229516.aspx) 取得。

MakeAppx.exe 工具通常會在下列位置找到：

-   在 x86： C： \\ program files (x86) \\ Windows 套件 \\ 8.0 \\ bin \\ x86 \\makeappx.exe 或 C： \\ Program Files (x86) \\ Windows 套件 \\ 8.1 \\ bin \\ x86 \\makeappx.exe
-   在 x64 上的兩個位置：
    -   C： \\ program files (x86) \\ Windows 套件 \\ 8.0 \\ bin \\ x86 \\makeappx.exe 或 C： \\ program files (x86) \\ Windows 套件 \\ 8.1 \\ bin \\ x86 \\makeappx.exe
    -   C： \\ program files (x86) \\ Windows 套件 \\ 8.0 \\ bin \\ x64 \\makeappx.exe 或 C： \\ program files (x86) \\ Windows 套件 \\ 8.1 \\ bin \\ x64 \\makeappx.exe

沒有 ARM 版本的工具。

-   [使用目錄結構建立封裝](#to-create-a-package-using-a-directory-structure)
-   [使用對應檔建立封裝](#to-create-a-package-using-a-mapping-file)
-   [若要使用 SignTool 簽署封裝](#to-sign-the-package-using-signtool)
-   [從封裝解壓縮檔案](#to-extract-files-from-a-package)
-   [使用目錄結構建立封裝套件組合](#to-create-a-package-bundle-using-a-directory-structure)
-   [使用對應檔建立封裝套件組合](#to-create-a-package-bundle-using-a-mapping-file)
-   [從套件組合解壓縮套件](#to-extract-packages-from-a-bundle)
-   [使用金鑰檔加密封裝](#to-encrypt-a-package-with-a-key-file)
-   [使用全域測試金鑰加密封裝](#to-encrypt-a-package-with-a-global-test-key)
-   [使用金鑰檔解密封裝](#to-decrypt-a-package-with-a-key-file)
-   [使用全域測試金鑰解密封裝](#to-decrypt-a-package-with-a-global-test-key)
-   [使用量](#usage)

## <a name="using-app-packager"></a>使用應用程式封裝工具

> [!Note]  
> 整個工具都支援相對路徑。

 

### <a name="to-create-a-package-using-a-directory-structure"></a>使用目錄結構建立封裝

將 AppxManifest.xml 放在包含應用程式的所有承載檔的目錄根目錄中。 系統會為應用程式套件建立相同的目錄結構，並在部署期間解壓縮封裝時可供使用。

1.  將所有檔案都放在單一目錄結構中，視需要建立子目錄。

2.  建立有效的套件資訊清單，AppxManifest.xml，並將它放在根目錄中。

3.  請執行這個命令：

    **MakeAppx pack/d** *input \_ directorypath* **/p** _filepath_**. appx**

### <a name="to-create-a-package-using-a-mapping-file"></a>使用對應檔建立封裝

1.  建立有效的套件資訊清單，AppxManifest.xml。

2.  建立對應檔。 第一行包含 **\[ \] 字串檔案**，接下來的幾行則會指定來源 (磁片) 和目的地 (封裝在加上引號的字串中) 路徑。

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  請執行這個命令：

    **MakeAppx pack/f** *對應 \_ filepath* **/p** _filepath_**. appx**

### <a name="to-sign-the-package-using-signtool"></a>若要使用 SignTool 簽署封裝

1.  建立憑證。 資訊清單中列出的發行者必須符合簽署憑證的發行者主體資訊。 如需建立簽署憑證的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。

2.  執行 SignTool.exe 以簽署套件：

    **SignTool sign/a/v/Fd** *hashAlgorithm* **/f** *certFileName* _filepath_**. appx**

    *HashAlgorithm* 必須符合在封裝應用程式時用來建立 blockmap 的雜湊演算法。 使用 MakeAppx 封裝公用程式時，預設 Appx blockmap 雜湊演算法是 **SHA256**。 執行 SignTool.exe 指定 **SHA256** 作為檔案摘要 (/fd) 演算法：

    **SignTool sign/a/v/FD SHA256/F** *certFileName* _filepath_**. appx**

    如需如何簽署套件的詳細資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。

### <a name="to-extract-files-from-a-package"></a>從封裝解壓縮檔案

1.  請執行這個命令：

    **MakeAppx 解壓縮/p** __ **. .appx/d** *輸出 \_ 目錄*

2.  解除封裝的套件與安裝的套件具有相同的結構。

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a>使用目錄結構建立封裝套件組合

我們會使用套件 **組合命令，** 在 <output bundle name> 藉由從 (加入所有封裝， <content directory> 包括) 的子資料夾。 如果 <content directory> 包含套件組合資訊清單，AppxBundleManifest.xml，則會予以忽略。

1.  將所有套件都放在單一目錄結構中，視需要建立子目錄。

2.  請執行這個命令：

    **MakeAppx 組合/d** *輸入 \_ directorypath* **/p** _filepath_**. .appxbundle**

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a>使用對應檔建立封裝套件組合

我們會使用套件 **組合命令，** 在 <output bundle name> 藉由在中從套件清單加入所有套件 <mapping file> 。 如果 <mapping file> 包含套件組合資訊清單，AppxBundleManifest.xml，則會予以忽略。

1.  建立 <mapping file>。 第一行包含 **\[ \] 字串檔案**，接下來的幾行指定要加入套件組合的封裝。 每個套件都是由引號中的一組路徑所描述，並以空格或定位字元分隔。 成對的路徑代表磁片) 上的套件來源 (以及套件組合) 中的目的地 (。 所有目的地封裝名稱的副檔名都必須是 .appx。

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  請執行這個命令：

    **MakeAppx 組合/f** *對應 \_ filepath* **/p** _filepath_ ****

### <a name="to-extract-packages-from-a-bundle"></a>從套件組合解壓縮套件

1.  請執行這個命令：

    **MakeAppx 解除配套/p** _組合 \_ 名稱_**.appxbundle/d** *輸出 \_ 目錄*

2.  解除封裝的組合具有與已安裝套件配套相同的結構。

### <a name="to-encrypt-a-package-with-a-key-file"></a>使用金鑰檔加密封裝

1.  建立金鑰檔。 金鑰檔必須以包含字串「機碼」的行開頭， \[ \] 後面接著描述用來加密封裝之金鑰的行。 每個索引鍵都是由引號中的一組字串所描述，並以空格或定位字元分隔。 第一個字串代表金鑰識別碼，而第二個字串表示以十六進位形式表示的加密金鑰。

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  請執行這個命令：

    **MakeAppx.exe 加密/p** _封裝 \_ 名稱_**.appx/ep** _加密的 \_ 封裝 \_ 名稱_**. eappx/kf** _keyfile \_ 名稱_**.txt**

3.  輸入封裝會使用提供的金鑰檔加密為指定的加密封裝。

### <a name="to-encrypt-a-package-with-a-global-test-key"></a>使用全域測試金鑰加密封裝

1.  請執行這個命令：

    **MakeAppx.exe 加密/p** _封裝 \_ 名稱_**.appx/ep** _加密的 \_ 封裝 \_ 名稱_**. eappx/kt**

2.  輸入封裝將會使用全域測試金鑰加密為指定的加密封裝。

### <a name="to-decrypt-a-package-with-a-key-file"></a>使用金鑰檔解密封裝

1.  建立金鑰檔。 金鑰檔必須以包含字串「機碼」的行開頭， \[ \] 後面接著描述用來加密封裝之金鑰的行。 每個索引鍵都是由引號中的一組字串所描述，並以空格或定位字元分隔。 第一個字串代表 base64 編碼的32位元組金鑰識別碼，而第二個字串代表 base64 編碼的32位元組加密金鑰。

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  請執行這個命令：

    **MakeAppx.exe 解密/p** _封裝 \_ 名稱_**. appx/ep** _未加密的 \_ 封裝 \_ 名稱_**. eappx/kf** _keyfile \_ 名稱_**.txt**

3.  輸入封裝會使用提供的金鑰檔解密為指定的未加密封裝。

### <a name="to-decrypt-a-package-with-a-global-test-key"></a>使用全域測試金鑰解密封裝

1.  請執行這個命令：

    **MakeAppx.exe 解密/p** _封裝 \_ 名稱_**. appx/ep** _未加密的 \_ 封裝 \_ 名稱_**。 eappx/kt**

2.  輸入封裝將會使用全域測試金鑰解密至指定的未加密封裝中。

## <a name="usage"></a>使用量

命令列引數 **/p** 一律是必要的，其中包含 **/d**、 **/f** 或 **/ep**。 請注意， **/d**、 **/f** 和 **/ep** 互斥。

**MakeAppx pack \[ 選項 \]** **/p** *\<output package name\>* **/d***\<content directory\>*

**MakeAppx pack \[ 選項 \]** **/p** *\<output package name\>* **/f***\<mapping file\>*

**MakeAppx 解壓縮 \[ 選項 \]** **/p** *\<input package name\>* **/d***\<output directory\>*

**MakeAppx 套件 \[ 組合 \] 選項** **/p** *\<output bundle name\>* **/d***\<content directory\>*

**MakeAppx 套件 \[ 組合 \] 選項** **/p** *\<output bundle name\>* **/f***\<mapping file\>*

**MakeAppx 解除配套 \[ options \]** **/p** *\<input bundle name\>* **/d***\<output directory\>*

**MakeAppx encrypt \[ 選項 \]** **/p** *\<input package name\>* **/ep***\<output package name\>*

**MakeAppx 解密 \[ 選項 \]** **/p** *\<input package name\>* **/ep***\<output package name\>*

## <a name="command-line-syntax"></a>命令列語法

以下是 MakeAppx 的命令列常見使用語法。

**MakeAppx \[ pack \| 解壓縮套件組合 \| \| 解除配套 \| 加密 encrypt \| \]** \[ **/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/？**\]

**MakeAppx** 會封裝或解壓縮套件中的檔案、配套或 unbundles 套件組合中的套件，或加密或解密指定輸入目錄或對應檔中的應用程式套件或套件組合。 以下是適用于 **MakeAppx pack**、 **MakeAppx 解壓縮**、 **MakeAppx** 配套、 **MakeAppx 解除配套**、 **MakeAppx 加密** 或 **MakeAppx 解密** 的參數清單。

<dl> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

此選項用於當地語系化的封裝。 預設驗證是針對當地語系化的套件進行。 此選項只會停用該特定驗證，而不需要停用所有驗證。

</dd> <dt>

<span id="_o"></span><span id="_O"></span>**/o**
</dt> <dd>

如果輸出檔案存在，請予以覆寫。 如果您未指定此選項或 **/no** 選項，則會詢問使用者是否要覆寫檔案。

您無法將此選項與 **/no** 搭配使用。

</dd> <dt>

<span id="_no"></span><span id="_NO"></span>**/no**
</dt> <dd>

如果有，可以避免覆寫輸出檔案。 如果您未指定此選項或 **/o** 選項，系統會詢問使用者是否要覆寫檔案。

您無法搭配使用此選項與 **/o**。

</dd> <dt>

<span id="_nv"></span><span id="_NV"></span>**/nv**
</dt> <dd>

略過語意驗證。 如果您沒有指定此選項，工具會對套件執行完整驗證。

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

啟用主控台的詳細資訊記錄輸出。

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

顯示解說文字。

</dd> </dl>

**MakeAppx pack** 、 **MakeAppx 解壓縮** 、 **MakeAppx** 配套、 **MakeAppx 解除配套**、 **MakeAppx 加密** 和 **MakeAppx 解密** 都是互斥的命令。 以下是特別適用于每個命令的命令列參數：

**MakeAppx 套件** \[**h**\]

建立套件。

<dl> <dt>

<span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *演算法*
</dt> <dd>

指定建立區塊對應時要使用的雜湊演算法。 以下是有效的 *演算法* 值：

<dl> <dd>SHA256 (預設)</dd> <dd>SHA384</dd> <dd>SHA512</dd> </dl>

您無法使用此選項搭配 **解壓縮** 命令。

</dd> </dl>

**MakeAppx 解壓縮** \[**pfn**\]

將指定套件中的所有檔案解壓縮到指定的輸出目錄。 輸出的目錄結構與封裝相同。

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

使用封裝的完整名稱指定名稱為的目錄。 此目錄會建立在所提供的輸出位置下。 您無法使用此選項搭配 **pack** 命令。

</dd> </dl>

**MakeAppx 解除配套** \[**pfn**\]

將所有套件解壓縮至指定的輸出路徑底下的子目錄，並以配套的完整名稱命名。 輸出具有與已安裝套件配套相同的目錄結構。

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

使用封裝套件組合的完整名稱指定名為的目錄。 此目錄會建立在所提供的輸出位置下。 您無法使用此選項搭配套件 **組合命令。**

</dd> </dl>

**MakeAppx 加密** \[**kf**、 **kt**\]

從指定之輸出封裝的指定輸入應用程式封裝建立加密應用程式封裝。

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf***<key file>*
</dt> <dd>

使用指定金鑰檔中的金鑰來加密封裝或套件組合。 您無法將此選項與 **kt** 搭配使用。

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

使用全域測試金鑰來加密封裝或套件組合。 您無法將此選項與 **kf** 搭配使用。

</dd> </dl>

**MakeAppx 解密** \[**kf**、 **kt**\]

從指定之輸出封裝的指定輸入應用程式封裝，建立未加密的應用程式套件。

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf***<key file>*
</dt> <dd>

使用指定金鑰檔中的金鑰來解密封裝或套件組合。 您無法將此選項與 **kt** 搭配使用。

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

使用全域測試金鑰來解密封裝或組合。 您無法將此選項與 **kf** 搭配使用。

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a>MakeAppx 執行的語意驗證

MakeAppx 會執行有限的語意驗證，其設計目的是要攔截最常見的部署錯誤，並協助確保應用程式封裝有效。

此驗證可確保︰

-   在套件資訊清單中參考的所有檔案都包含在應用程式套件中。
-   應用程式不會有兩個相同的金鑰。
-   應用程式不會從這份清單註冊禁止的通訊協定： SMB、檔案、MS-WWA-WEB、WWA。

此語意驗證未完成，而且 MakeAppx 所建立的套件不保證可供安裝。

 

 