---
description: 應用程式佈建檔是用來控制元件系結的 XML 檔。
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: 應用程式組態檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf4b22d3710c0dd38e83f827a175ad591309f22ab8ac2d81e93438f27d07dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142521"
---
# <a name="application-configuration-files"></a>應用程式組態檔

應用程式佈建檔是用來控制元件系結的 XML 檔。 它可以將應用程式從使用一種並存元件的版本重新導向至相同元件的另一個版本。 這稱為 [每個應用程式](per-application-configuration.md)設定。 應用程式佈建檔只適用于特定的應用程式資訊清單和相依元件。 使用內嵌 ISOLATIONAWARE \_ 資訊清單 \_ 資源識別碼資訊清單編譯的隔離元件 \_ 需要個別的應用程式佈建檔。 使用 [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) 管理的資訊清單需要個別的應用程式佈建檔。

應用程式佈建檔所指定的重新導向可覆寫 [應用程式資訊清單](application-manifests.md) 和 [發行者設定檔](publisher-configuration-files.md)案所指定的元件版本。 例如，如果發行者設定檔指定將元件的所有參考從1.0.0.0 版重新導向至1.1.0.0，則可以使用應用程式佈建檔重新導向特定應用程式以使用1.0.0.0 版。 應用程式佈建檔僅適用于指定的應用程式資訊清單和相依元件。

如需 XML 架構的完整清單，請參閱 [應用程式佈建檔架構](application-configuration-file-schema.md)。

應用程式佈建檔具有下表所示的元素和屬性。



| 項目               | 屬性                | 必要 |
|-----------------------|---------------------------|----------|
| **設定**     |                           | Yes      |
| **windows**           |                           | Yes      |
| **>publisherpolicy**   |                           | Yes      |
|                       | **應用**                 | Yes      |
| **運行**           |                           | No       |
| **assemblyBinding**   |                           | Yes      |
| **探討**           |                           | No       |
|                       | **privatePath**           | Yes      |
| **依賴**        |                           | No       |
| **y** |                           | Yes      |
| **assemblyIdentity**  |                           | Yes      |
|                       | **type**                  | Yes      |
|                       | **name**                  | Yes      |
|                       | **language**              | No       |
|                       | **processorArchitecture** | Yes      |
|                       | **version**               | Yes      |
|                       | **publicKeyToken**        | No       |
| **bindingRedirect**   |                           | Yes      |
|                       | **oldVersion**            | Yes      |
|                       | **newVersion**            | Yes      |



 

## <a name="file-location"></a>檔案位置

應用程式佈建檔必須安裝在與應用程式 [應用程式資訊清單](application-manifests.md)相同的位置。

## <a name="file-name-syntax"></a>檔名語法

應用程式佈建檔的名稱是應用程式可執行檔的名稱，後面接著 .config。

例如，參考 Example.exe 或 Example.dll 的應用程式佈建檔會使用下列範例所示的檔案名語法。 如果將設定檔安裝為個別檔案，或資源識別碼為1，您可以省略 <*資源識別碼*> 的欄位。

**example.exe。 <*資源識別碼* C1.config**

**example.dll。 <*資源識別碼* C1.config**

## <a name="elements"></a>元素

元素和屬性的名稱會區分大小寫。 專案和屬性的值全都不區分大小寫，但 type 屬性的值除外。

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>組態

應用程式佈建檔的 **windows** 與 **運行** 時間專案的容器元素。 必要。

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>windows

包含應用程式佈建檔的元件，該元件會套用至 Win32 元件的重新導向。

> [!Note]  
> 應用程式的作者不應包含具有 **windows** 子項目的設定檔，做為其應用程式的一部分。 如果設定檔的唯一目的是要啟用 **探查** 元素的 **privatePath** 功能，則可能會允許這種情況。 在 Windows Server 2008 R2 和 Windows 7 之前的系統上無法使用 **探查** 元素。

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>>publisherpolicy

指定是否要套用發行者原則。

此元素具有下表所示的屬性。



| 屬性 | 描述                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **應用** | 值為 "yes" 時，會套用發行者原則。 這是預設值。 值為 "no" 時，不會套用發行者原則。 |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>執行階段

包含應用程式佈建檔的部分，適用于 .Net 元件的重新導向。

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>assemblyBinding

包含應用程式的重新導向資訊，以及受此應用程式佈建檔影響的元件。 **AssemblyBinding** 的第一個子項目必須是可識別應用程式的 **assemblyIdentity** 。

從 Windows Server 2008 R2 和 Windows 7 開始， **assemblyBinding** 專案可以包含 **探查** 子項目。

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>探查

**AssemblyBinding** 專案的選擇性元素，可將元件的搜尋延伸至其他目錄。 其他目錄不需要是元件目錄的子目錄。

> [!Note]  
> 在 Windows Server 2008 R2 和 Windows 7 之前的系統上無法使用此元素，而且只能在 **Windows** 專案內使用。

此元素具有下表所示的屬性。

| 屬性       | 描述                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **privatePath** | 指定可能包含元件的應用程式基底目錄之子目錄的 [相對路徑](/windows/desktop/FileIO/naming-a-file) 。 最多可以指定九個子目錄路徑。 使用分號分隔每個子目錄路徑。 |

您可以在路徑中使用雙點特殊規範，以表示目前的目錄的上層目錄。 您可以使用雙點來指定目前目錄上方的兩個層級。 請勿使用三個點。 例如，使用下列 **探查** 元素的應用程式會檢查元件的其他目錄。

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>相依性
至少一個 **y** 的容器元素。 每個 **y** 都可以只在 **一個相依** 性內。 這個元素沒有屬性。 選擇性。

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

第一個子項目必須是 **assemblyIdentity** 專案，可識別應用程式佈建檔重新導向的並存元件。 **Y** 沒有任何屬性。

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

**AssemblyIdentity** 會以 **assemblyBinding** 專案的第一個子項目來描述和唯一識別應用程式。 應用程式佈建檔會將此應用程式的系結重新導向至並存元件。 例如，下列 **assemblyIdentity** 表示應用程式佈建檔會影響應用程式 >mysampleapp 對並存元件的系結。 重新導向的元件會在 **y** 中識別。

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

**AssemblyIdentity** 會以 **y** 專案的第一個子項目，描述應用程式所相依的並存元件。 應用程式佈建檔會重新設定此必要元件的身分識別。 例如，下列 **assemblyIdentity** 和 **bindingRedirect** 會重新配置 Microsoft 的相依性。Windows。從2.0.0.0 版 SampleAssembly 至版本2.1.0.0。

``` XML
<dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32"
          name="Microsoft.Windows.SampleAssembly"
          processorArchitecture="x86"
          publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.1.0.0"/>
      </dependentAssembly>
</dependency>
```

請注意， **y** 中包含的每個 **assemblyIdentity** 都必須完全符合元件本身的 [組件資訊清單](assembly-manifests.md)中的 **assemblyIdentity** 。

**AssemblyIdentity** 元素具有下列屬性。 它沒有子項目。

| 屬性                 | 描述                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | 值必須是 win32 (小寫) 。 必要。                                                                                                                                                                                                                                                                      |
| **name**                  | Name 屬性會識別受應用程式佈建檔或正在重新導向的元件所影響的應用程式。 針對名稱，請使用下列格式： Organization.Division.Name。 必要。 例如： Microsoft。Windows。>mysampleapp 或 Microsoft。Windows。MysampleAsm.<br/>            |
| **language**              | 識別語言。 選擇性。 對於參考元件的 **assemblyIdentity** ，如果元件是語言特定的，請指定 DHTML 語言代碼。 如果元件適用于全球使用 (中性語言) 將值設定為 " \* "。<br/>                                                            |
| **processorArchitecture** | 指定執行應用程式的處理器。                                                                                                                                                                                                                                                                     |
| **version**               | 指定應用程式或元件的版本。 使用四部分的版本語法： mmmm. oooo. pppp。 必要。                                                                                                                                                                                                   |
| **publicKeyToken**        | 若為參考元件的 **assemblyIdentity** ，則為16字元的十六進位字串，代表簽署元件之公開金鑰的 sha-1 雜湊最後8個位元組。 用來簽署目錄的公開金鑰必須是2048位或更高的版本。 所有共用並存元件的必要項。 |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>bindingRedirect

**BindingRedirect** 元素包含元件系結的重新導向資訊。 每個 **bindingRedirect** 都必須只包含在一個 **y** 中。 新版本和舊版本的四部分版本語法必須指定相同的主要和次要版本。

此元素具有下表所示的屬性。

| 屬性      | 描述                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | 指定要覆寫和重新導向的元件版本。 使用四部分的版本語法 nnnnn。 以沒有空格的虛線來指定版本範圍。 例如，2.14.3.0 或 2.14.3.0 2.16.0.0。 必要。 |
| **newVersion** | 指定取代元件的版本。 使用四部分的版本語法 nnnnn。                                                                                                                                     |

## <a name="remarks"></a>備註

應用程式佈建檔不會指定檔案。

## <a name="example"></a>範例

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
