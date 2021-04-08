---
description: 發行者設定檔是一種 XML 檔案，可將應用程式和元件從使用一種並存元件版本，重新導向至相同元件的另一個版本。
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: 發行者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851772"
---
# <a name="publisher-configuration-files"></a>發行者設定檔

發行者設定檔是一種 XML 檔案，可將應用程式和元件從使用一種並存元件版本，重新導向至相同元件的另一個版本。 一般來說，元件的發行者會發出發行者設定檔案，以與 service pack 更新一起安裝，以針對每個元件發出相容的更新或安全性修正程式。 這稱為「 [發行者](publisher-configuration.md)設定」。 如需此類型設定的詳細資訊 [，請參閱](configuration.md) 發行者設定。

發行者設定檔具有下列元素和屬性。 如需 XML 架構的完整清單，請參閱 [發行者設定檔架構](publisher-configuration-file-schema.md)。



| 項目               | 屬性                | 必要 |
|-----------------------|---------------------------|----------|
| **裝配**          |                           | Yes      |
|                       | **manifestVersion**       | Yes      |
| **assemblyIdentity**  |                           | Yes      |
|                       | **type**                  | Yes      |
|                       | **name**                  | Yes      |
|                       | **language**              | No       |
|                       | **processorArchitecture** | No       |
|                       | **version**               | Yes      |
|                       | **publicKeyToken**        | No       |
| **依賴**        |                           | No       |
| **y** |                           | No       |
| **bindingRedirect**   |                           | Yes      |
|                       | **oldVersion**            | Yes      |
|                       | **newVersion**            | Yes      |



 

## <a name="file-location"></a>檔案位置

發行者設定檔必須安裝在 WinSxS 資料夾中。 它們通常會安裝為個別的檔案，但發行者設定檔也可以包含為 DLL 中的資源。 發行者設定檔無法以資源的形式包含在 EXE 檔案中。 EXE 檔案可能會包含 [應用程式資訊清單](application-manifests.md) 做為資源。

## <a name="file-name-syntax"></a>檔名語法

發行者設定檔案的檔案名具有表單 *原則*。*主要*。*次要*。*assemblyname* ，其中 *主要* 和 *次要* 會參考受影響之 [元件版本](assembly-versions.md) 的主要和次要部分。 *Assemblyname* 指的是元件的名稱。

例如，Microsoft 的6.0 版發行者設定檔會有下列名稱： < 組解碼：

<dl> policy. Windows. 一般控制項  
</dl>

請勿使用原則設定檔來遞增元件的主要或次要版本。 例如，請勿將 version 6.0.0.0 重新導向至7.0.0.0 或6.1.0.0。 當應用程式參考元件版本（例如6.0.0.0）時，並存檢查是否有任何具有指定主要和次要版本的原則設定檔，例如6.0。 然後，應用程式會重新導向至另一個版本的元件，例如6.0.1.0。 如果發行者設定檔遞增元件的主要或次要版本，則元件的後續重新導向可能需要發出多個原則設定檔案。

## <a name="elements"></a>元素

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**裝配**
</dt> <dd>

容器元素。 它的第一個子項目必須是 **assemblyIdentity**。 必要。

Assembly 元素必須位於命名空間 **urn：架構-microsoft-com： .asm** 中。 元件的子專案也必須在這個命名空間中，繼承或標記。

**Assembly** 元素具有下列屬性。



| 屬性           | 描述                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | **ManifestVersion** 屬性必須設定為1.0。 |



 

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

描述和唯一識別並存元件。

作為 **元件** 專案的第一個子項目， **assemblyIdentity** 會描述有一或多個元件相依性變更的並存元件。 發行者設定檔會重新導向所識別元件的相依性。 例如，下列 **assemblyIdentity** 表示發行者設定檔會影響 x86 6.0.0.0 元件的相依性。

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

**AssemblyIdentity** 是 **y** 專案的第一個子項目，描述並存元件相依性。 發行者設定檔會重新設定此必要並存元件的身分識別。 變更會在 **bindingRedirect** 中指定。 例如，下列 **assemblyIdentity** 會將 SampleAssembly 2.0.0.0 版的相依性變更為 SampleAssembly version 2.0.1.0 的相依性。

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

**AssemblyIdentity** 元素具有下列屬性。 它沒有子項目。



| 屬性                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | 指定元件類型。 必要。 在受影響之元件的 **assemblyIdentity** 中， **type** 屬性的值必須設定為 win32 原則。 Win32 原則的值必須全部都是小寫字母。<br/> 在變更元件相依性的 **assemblyIdentity** 中， **類型** 屬性的值必須設定為 [win32]。 Win32 的值必須全部都是小寫字母。<br/>                                                                                                                                                                                                             |
| **name**                  | 唯一命名元件。 必要。 在受影響之元件的 **assemblyIdentity** 中，名稱具有表單 *原則*。*主要*。*次要*。*assemblyname* ，其中 *主要* 和 *次要* 指的是 [元件版本](assembly-versions.md)的主要和次要部分。<br/> 在變更元件相依性的 **assemblyIdentity** 中，名稱的格式為 Organization.Division.Name。 例如，>mysampleapp。<br/>                                                                                                                                                                                 |
| **language**              | 識別元件的語言。 選擇性。 在受影響之元件的 **assemblyIdentity** 中，如果元件是語言特定的，請指定 DHTML 語言代碼。 如果元件適用于全球使用 (語言中性) ，請省略此屬性。<br/> 在變更元件相依性的 **assemblyIdentity** 中，如果元件是語言特定的，請指定 DHTML 語言代碼。 如果元件適用于全球使用 (中性語言) 將值設定為 " \* "。<br/>                                                                                                                            |
| **processorArchitecture** | 指定執行應用程式的處理器。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **version**               | 指定組件版本。 使用四部分版本語法： mmmm. oooo. pppp 只有在 DEF-coNtext **assemblyIdentity** 中才需要。 請勿在 REF 內容 **assemblyIdentity** 中指定 version 屬性。                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **publicKeyToken**        | 16字元的十六進位字串，代表用來簽署元件之公開金鑰的 SHA-1 雜湊最後8個位元組。 用來簽署目錄的公開金鑰必須是2048位或更高的版本。 所有共用並存元件都需要 publicKeyToken。 用於發行者設定檔的 publicKeyToken 應與簽署的元件使用的金鑰相同。 發行者設定檔可以使用與元件搭配使用的相同工具來簽署，請參閱 [元件簽署範例](assembly-signing-example.md) 和 [建立簽署的檔案和目錄](creating-signed-files-and-catalogs.md)。 |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**依賴**
</dt> <dd>

至少一個 **y** 的選擇性容器元素。 它沒有任何屬性。

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**y**
</dt> <dd>

每個 **y** 都必須正好在 **一個相依** 性內。 **Y** 沒有任何屬性。 **Y** 的第一個子項目必須是由發行者設定重新設定之並存元件的 **assemblyIdentity** 。

</dd> <dt>

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**
</dt> <dd>

**BindingRedirect** 元素包含元件系結的重新導向資訊。

此元素具有下表所示的屬性。



| 屬性      | 描述                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | 指定要覆寫和重新導向的元件版本。 使用四部分的版本語法 nnnnn。 以沒有空格的虛線來指定版本範圍。 例如，2.14.3.0 或 2.14.3.0 2.16.0.0。 必要。 |
| **newVersion** | 指定取代元件的版本。 使用四部分的版本語法 nnnnn。                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a>備註

發行者設定檔不會指定檔案。 請注意，特定語言的原則檔案與發行者設定檔不同。

## <a name="example"></a>範例

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




