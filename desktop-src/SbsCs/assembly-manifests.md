---
description: 組件資訊清單是描述並存元件的 XML 檔。
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: 組件資訊清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254702d5044331fa5d47def815556dbd8edef2f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193293"
---
# <a name="assembly-manifests"></a>組件資訊清單

組件資訊清單是描述並存元件的 XML 檔。 組件資訊清單會描述並存元件的名稱和版本、檔案以及元件的資源，以及元件在其他並存元件上的相依性。 修正並存元件的安裝、啟動及執行，必須將組件資訊清單一律伴隨系統上的元件。

如需 XML 架構的完整清單，請參閱 [資訊清單檔案架構](manifest-file-schema.md)。

元件資訊清單具有下列元素和屬性。



| 項目                           | 屬性                | 必要 |
|-----------------------------------|---------------------------|----------|
| **裝配**                      |                           | Yes      |
|                                   | **manifestVersion**       | Yes      |
| **noInheritable**                 |                           | No       |
| **assemblyIdentity**              |                           | Yes      |
|                                   | **type**                  | Yes      |
|                                   | **name**                  | Yes      |
|                                   | **language**              | No       |
|                                   | **processorArchitecture** | No       |
|                                   | **version**               | Yes      |
|                                   | **publicKeyToken**        | No       |
| **依賴**                    |                           | No       |
| **y**             |                           | No       |
| **file**                          |                           | No       |
|                                   | **name**                  | Yes      |
|                                   | **hashalg**               | No       |
|                                   | **hash**                  | No       |
| **Comclass.zip**                      |                           | No       |
|                                   | **description**           | No       |
|                                   | **Clsid**                 | Yes      |
|                                   | **>threadingmodel**        | No       |
|                                   | **tlbid**                 | No       |
|                                   | **progid**                | No       |
|                                   | **miscStatus**            | No       |
|                                   | **miscStatusIcon**        | No       |
|                                   | **miscStatusContent**     | No       |
|                                   | **miscStatusDocPrint**    | No       |
|                                   | **miscStatusDocPrint**    | No       |
| **類型**                       |                           | No       |
|                                   | **tlbid**                 | Yes      |
|                                   | **version**               | Yes      |
|                                   | **helpdir**               | Yes      |
|                                   | **id**            | No       |
|                                   | **flags**                 | No       |
| **comInterfaceExternalProxyStub** |                           | No       |
|                                   | **Iid**                   | Yes      |
|                                   | **Typeinterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **name**                  | No       |
|                                   | **tlbid**                 | No       |
|                                   | **proxyStubClsid32**      | No       |
| **comInterfaceProxyStub**         |                           | No       |
|                                   | **Iid**                   | Yes      |
|                                   | **name**                  | Yes      |
|                                   | **tlbid**                 | No       |
|                                   | **Typeinterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **proxyStubClsid32**      | No       |
|                                   | **>threadingmodel**        | No       |
| **windowClass**                   |                           | No       |
|                                   | **版本**             | No       |



 

## <a name="file-location"></a>檔案位置

元件資訊清單可以安裝在三個位置：

-   如同 [共用元件](/windows/desktop/Msi/shared-assemblies)的資訊清單一樣，組件資訊清單也應該安裝為並存組件快取中的個別檔案。 這通常是 Windows 目錄中的 WinSxS 資料夾。
-   如同 [私用元件](/windows/desktop/Msi/private-assemblies)伴隨的資訊清單，組件資訊清單應該安裝在應用程式的目錄結構中。 這通常是與應用程式的可執行檔相同的資料夾中的個別檔案。
-   作為 DLL 中的資源，元件可用於 DLL 的私用。 元件資訊清單不能以資源的形式包含在 EXE 中。 EXE 檔案可能會包含 [應用程式資訊清單](application-manifests.md) 做為資源。

## <a name="file-name-syntax"></a>檔名語法

組件資訊清單的名稱是任何有效的檔案名，後面接著. 資訊清單。

例如，參考 myassembly 的組件資訊清單會使用下列檔案名語法。 如果要將組件資訊清單安裝為個別檔案，或是資源識別碼是1，您可以省略 <*資源識別碼*> 欄位。

<dl> myassembly ... <resource ID>清單
</dl>

> [!Note]  
> 由於並存搜尋私用元件的方式，因此封裝 DLL 做為私用元件時，將會套用下列命名限制。 執行這項操作的建議方式是將組件資訊清單放在 DLL 中做為資源。 在此情況下，資源識別碼必須等於1，而且私用元件的名稱可能與 DLL 的名稱相同。 例如，如果 DLL 的名稱是 Microsoft.Windows.mysample.dll，資訊清單之 **assemblyIdentity** 專案中所使用的 name 屬性（attribute）值也可以是 mysample。 另一種方式是將組件資訊清單放在不同的檔案中。 在此情況下，元件的名稱及其資訊清單必須與 DLL 的名稱不同。 例如，mysampleAsm、mysampleAsm，以及 Microsoft.Windows.Mysample.dll 的範例中。 如需如何並存搜尋私用元件的詳細資訊，請參閱 [元件搜尋序列](assembly-searching-sequence.md)。

 

## <a name="elements"></a>元素

元素和屬性的名稱會區分大小寫。 元素和屬性的值不區分大小寫，但 type 屬性的值除外。

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**裝配**
</dt> <dd>

容器元素。 它的第一個子項目必須是 **assemblyIdentity** 或 **noInheritable** 元素。 組件資訊清單可唯一描述 **assemblyIdentity** 所識別的並存元件。 必要。

Assembly 元素必須在命名空間 "urn：架構-microsoft-com： asm" 中。 元件的子專案也必須在這個命名空間中，繼承或標記。

**Assembly** 元素具有下列屬性。



| 屬性           | 描述                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | **ManifestVersion** 屬性必須設定為1.0。 |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**noInheritable**
</dt> <dd>

將此專案包含在組件資訊清單中，以指出該元件會管理 [啟用](activation-contexts.md) 內容及其物件。 **NoInheritable** 元素必須是 **元件** 專案的元素。 **AssemblyIdentity** 元素應位於任何 **noInheritable** 元素之後。 如果包含 **noInherit** 元素的任何 [應用程式資訊清單](application-manifests.md)使用元件，則組件資訊清單中需要 **noInheritable** 元素。 應用程式資訊清單中的 **noInheritable** 元素沒有任何作用。 **NoInheritable** 元素沒有任何子項目。

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

描述和唯一識別並存元件。

作為 **元件** 專案的第一個子項目， **assemblyIdentity** 會描述和唯一識別擁有此組件資訊清單的並存元件。 這稱為組件資訊清單的 DEF 內容 **assemblyIdentity** 。

**AssemblyIdentity** 會以 **y** 專案的第一個子項目，描述和唯一識別 DEF 內容 **assemblyIdentity** 所使用的並存元件。 這稱為組件資訊清單的參考內容 **assemblyIdentity** 。 DEF 內容元件需要 REF 內容元件才能正確運作。 請注意，每個 REF 內容 **assemblyIdentity** 必須完全符合參考元件本身的組件資訊清單中對應的 DEF 內容 **assemblyIdentity** 。

這個元素沒有子項目。 **AssemblyIdentity** 元素具有下列屬性。



| 屬性                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | 指定元件類型。 此值必須是 win32 且以小寫形式。 必要。                                                                                                                                                                                                                                                                                                                                                         |
| **name**                  | 將元件命名為唯一名稱。 針對元件名稱，請使用下列格式： Organization.Division.Name。 例如，mysampleAsm。 必要。 請注意，如果 DLL 以個別的資訊清單檔封裝為私用元件，則元件的名稱必須與 DLL 和資訊清單的名稱不同。<br/>                                                                              |
| **language**              | 識別元件的語言。 選擇性。 如果元件是語言特定的，請指定 DHTML 語言代碼。 在適用于全球用途 (語言的組件資訊清單的 DEF 內容 **assemblyIdentity** 中) 省略 language 屬性。<br/> 在適用于全球用途 (語言的組件資訊清單之 REF 內容 **assemblyIdentity** 中) 將 language 的值設定為 " \* "。<br/> |
| **processorArchitecture** | 指定處理器。 有效的值為適用于32位 Windows 的 x86 和64位 Windows 的 ia64。 選擇性。                                                                                                                                                                                                                                                                                                                               |
| **version**               | 指定組件版本。 使用四部分版本格式：好吃. ooooo. ppppp。 以句號分隔的每個部分都可以是0-65535 （含）。 如需詳細資訊，請參閱 [元件版本](assembly-versions.md)。 必要。                                                                                                                                                                                               |
| **publicKeyToken**        | 16字元的十六進位字串，代表用來簽署元件之公開金鑰的 SHA-1 雜湊最後8個位元組。 用來簽署目錄的公開金鑰必須是2048位或更高的版本。 共用並存元件的必要項。                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**依賴**
</dt> <dd>

包含至少一個 **y** 的容器元素。 第一個子項目必須是 **y** 專案。 相依 **性沒有任何** 屬性。 選擇性。

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**y**
</dt> <dd>

第一個子項目必須是 **assemblyIdentity** 專案，它會描述和唯一識別由擁有此組件資訊清單之並存元件所使用的並存元件。 每個 **y** 都必須正好在 **一個相依** 性內。 選擇性。

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**檔**
</dt> <dd>

包含並存元件所使用的檔案。 包含 **comclass.zip**、 **typelib**、 **windowClass**、 **comInterfaceProxyStub** 子項目。 選擇性。

**File** 元素具有下列屬性。



| 屬性   | 描述                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | 檔案名，例如 Conctl32.dll。                                                            |
| **hashalg** | 用來建立檔案雜湊的演算法。 此值應為 SHA1。                                 |
| **hash**    | 名稱所參考之檔案的雜湊。 長度的十六進位字串，取決於雜湊演算法。 |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**Comclass.zip**
</dt> <dd>

**File** 元素的子項目。 選擇性。

**Comclass.zip** 元素具有下列屬性。



| 屬性               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **description**         | 類別名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Clsid**               | 可唯一識別類別的 GUID。 必要。 值的格式必須是有效的 GUID。                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **>threadingmodel**      | 同進程 COM 類別所使用的執行緒模型。 如果此屬性為 null，則不會使用任何執行緒模型。 元件是在用戶端的主執行緒上建立，而來自其他執行緒的呼叫會封送處理至此執行緒。 選擇性。 有效的值為：「公寓」、「免費」、「兩者」和「中性」。                                                                                                                                                                                                                         |
| **tlbid**               | 此 COM 元件之類型程式庫的 GUID。 此值必須是 GUID 的格式。 選擇性。                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **progid**              | 與 COM 元件相關聯的版本相依程式設計識別碼。 ProgID 的格式是 <*廠商*>。 <*元件*>. <*版本*>。                                                                                                                                                                                                                                                                                                                                                                      |
| **miscStatus**          | 組件資訊清單中的重複專案是由 MiscStatus 登錄機碼提供的資訊。 如果找不到 **miscStatusIcon**、 **miscStatusContent**、 **miscStatusDocprint** 或 **miscStatusThumbnail** 屬性的值，則會將 **miscStatus** 中列出的對應預設值用於遺漏的屬性。 值可以是下表中的屬性值清單（以逗號分隔）。 如果 COM 類別是需要 Miscstatus 登錄機碼值的 OCX 類別，您可以使用此屬性。 |
| **miscStatusIcon**      | 組件資訊清單中的重複專案，>DVASPECT 圖示提供的資訊 \_ 。 它可以提供物件的圖示。 值可以是下表中的屬性值清單（以逗號分隔）。 如果 COM 類別是需要 Miscstatus 登錄機碼值的 OCX 類別，您可以使用此屬性。                                                                                                                                                                                                                |
| **miscStatusContent**   | 組件資訊清單中的重複專案會 >DVASPECT 內容所提供的資訊 \_ 。 它可以為螢幕或印表機提供可顯示的複合檔案。 值可以是下表中的屬性值清單（以逗號分隔）。 如果 COM 類別是需要 Miscstatus 登錄機碼值的 OCX 類別，您可以使用此屬性。                                                                                                                                                                          |
| **miscStatusDocprint**  | 組件資訊清單中的重複專案 >DVASPECT DOCPRINT 所提供的資訊 \_ 。 它可以提供在螢幕上顯示的物件標記法，就好像列印到印表機一樣。 值可以是下表中的屬性值清單（以逗號分隔）。 如果 COM 類別是需要 Miscstatus 登錄機碼值的 OCX 類別，您可以使用此屬性。                                                                                                                                               |
| **miscStatusThumbnail** | 組件資訊清單中的重複專案，>DVASPECT 縮圖提供的資訊 \_ 。 它可以提供流覽工具中可顯示物件的縮圖。 值可以是下表中的屬性值清單（以逗號分隔）。 如果 COM 類別是需要 Miscstatus 登錄機碼值的 OCX 類別，您可以使用此屬性。                                                                                                                                                                         |



 

**Comclass.zip** 元素可以將 <progid>...</progid>元素做為子系，以列出相依于 progid 的版本。

下列範例會顯示包含在 **file** 元素中的 **comclass.zip** 元素。

``` syntax
<file name="sampleu.dll">
        <comClass description="Font Property Page"
    clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"
          threadingModel = "Both"
             tlbid = "{44EC0535-400F-11D0-9DCD-00A0C90391D3}"/>
        <comClass description="Color Property Page"
    clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}" 
    progid="ABC.Registrar"/>
    </file>
```

如果您的 COM 類別是需要 MiscStatus 登錄子機碼來指定如何建立及顯示物件的 OCX 類別，您可以藉由在組件資訊清單中複製這項資訊來啟用物件。 使用 **miscStatusThumbnail** 元素的 **miscStatus**、 **miscStatusIcon**、 **miscStatusContent**、 **miscStatusDocprint** 和 **comclass.zip** 屬性來指定物件的特性。 將這些屬性設定為下表中的屬性值清單（以逗號分隔）。 這些屬性會複製 >DVASPECT 列舉所提供的資訊。 如果找不到 **miscStatusIcon**、 **miscStatusContent**、 **miscStatusDocprint** 或 **MiscStatusThumbnail** 的值，則會使用 **miscStatus** 中指定的預設值。 使用下表中的屬性值。 這些會對應至 [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) 列舉的位旗標。



| 屬性值              | OLEMISC 常數                      |
|------------------------------|---------------------------------------|
| recomposeonresize            | OLEMISC \_ RECOMPOSEONRESIZE            |
| onlyiconic                   | OLEMISC \_ ONLYICONIC                   |
| insertnotreplace             | OLEMISC \_ INSERTNOTREPLACE             |
| static                       | OLEMISC \_ 靜態                       |
| cantlinkinside               | OLEMISC \_ CANTLINKINSIDE               |
| canlinkbyole1                | OLEMISC \_ CANLINKBYOLE1                |
| islinkobject                 | OLEMISC \_ ISLINKOBJECT                 |
| insideout                    | OLEMISC \_ INSIDEOUT                    |
| activatewhenvisible          | OLEMISC \_ ACTI加值稅EWHENVISIBLE          |
| renderingisdeviceindependent | OLEMISC \_ RENDERINGISDEVICEINDEPENDENT |
| invisibleatruntime           | OLEMISC \_ INVISIBLEATRUNTIME           |
| alwaysrun                    | OLEMISC \_ ALWAYSRUN                    |
| actslikebutton               | OLEMISC \_ ACTSLIKEBUTTON               |
| actslikelabel                | OLEMISC \_ ACTSLIKELABEL                |
| nouiactivate                 | OLEMISC \_ NOUIACTI加值稅E                 |
| alignable                    | OLEMISC \_ ALIGNABLE                    |
| simpleframe                  | OLEMISC \_ SIMPLEFRAME                  |
| setclientsitefirst           | OLEMISC \_ SETCLIENTSITEFIRST           |
| imemode                      | TOLEMISC \_ IMEMODE                     |
| ignoreativatewhenvisible     | OLEMISC \_ IGNOREACTI加值稅EWHENVISIBLE    |
| wantstomenumerge             | OLEMISC \_ WANTSTOMENUMERGE             |
| supportsmultilevelundo       | OLEMISC \_ SUPPORTSMULTILEVELUNDO       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**類型**
</dt> <dd>

**File** 元素的子項目。 選擇性。

**Typelib** 元素具有下表所示的屬性。



| 屬性      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | 類型程式庫的唯一 ID。 必要。                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | 類型程式庫的兩部分版本號碼。 如果只增加次要版本號碼，則會以相容的方式支援先前類型程式庫的所有功能。 如果主要版本號碼變更，則必須重新編譯針對類型程式庫編譯的程式碼。 類型程式庫的版本號碼可能與應用程式的版本號碼不同。 必要。                                      |
| **helpdir**    | 類型程式庫中類型的說明檔所在的目錄。 如果應用程式支援多種語言的類型程式庫，則程式庫可能會參考說明檔目錄中的不同檔案名。 如果沒有值，則指定 ""。 必要。                                                                                                                                                          |
| **id** | 地區設定識別碼的十六進位字串標記法 (LCID) 。 這是一到四個十六進位數位，沒有0x 前置詞且沒有前置零。 LCID 可能具有中性的子語言識別項。 如需詳細資訊，請參閱 [地區設定識別碼](/windows/desktop/Intl/locale-identifiers)。 選擇性。                                                                                                                                      |
| **flags**      | 此類型程式庫之類型程式庫旗標的字串表示。 具體而言，它應該是「受限」、「控制」、「隱藏」和「HASDISKIMAGE」其中一個。 這些是 [**LIBFLAGS**](/windows/win32/api/oaidl/ne-oaidl-libflags)列舉的值，而且是 [**ICreateTypeLib：： SetLibFlags**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags)方法的 *uLibFlags* 參數中所指定的相同旗標。 選擇性。 |



 

下列範例顯示包含在 **file** 元素中的 **typelib** 元素。

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

**ComInterfaceExternalProxyStub** 是 **元件** 專案的子項目，用於自動化介面。 例如， [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 和其衍生的介面。 選擇性。

預設 proxy 存根實作為大部分的自動化介面，例如衍生自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)的介面。 介面 proxy stub 和所有其他的外部 proxy stub 介面執行都必須列在 **comInterfaceExternalProxyStub** 中。 **ComInterfaceExternalProxyStub** 元素具有下表所示的屬性。



| 屬性         | 描述                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**           | 正在宣告 proxy 之介面的 IID。 必要。 值的格式應為： "{iid}"。                                                                         |
| **Typeinterface** | 由 **iid** 屬性所描述的介面所衍生之介面的 IID。 此屬性是選擇性的。 值的格式應為： "{iid}"。                            |
| **numMethods**    | 介面所執行的方法數目。 此屬性是選擇性的。 值的格式應為： "n"。                                                                       |
| **name**          | 出現在程式碼中的介面名稱。 例如，"IViewObject"。 這不能是描述性字串。 此屬性是選擇性的。 值的格式應為： "name"。 |
| **tlbid**         | 類型程式庫，其中包含 **iid** 屬性所指定之介面的描述。 此屬性是選擇性的。 值的格式應為： "{tlbid}"。                |
| proxyStubClsid32  | 將 IID 對應至32位 proxy Dll 中的 CLSID。                                                                                                                                                |



 

下列範例顯示 **comInterfaceExternalProxyStub** 元素。

``` syntax
<comInterfaceExternalProxyStub 
  name="IAxWinAmbientDispatch" 
    iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" 
    numMethods="35" 
  baseInterface="{00000000-0000-0000-C000-000000000046}"/>
```

</dd> <dt>

<span id="comInterfaceProxyStub"></span><span id="cominterfaceproxystub"></span><span id="COMINTERFACEPROXYSTUB"></span>**comInterfaceProxyStub**
</dt> <dd>

**File** 元素的子項目。 選擇性。

如果元件中的檔案採用 proxy 存根，則對應的檔案標記必須包含具有與 **comInterfaceProxyStub** 專案相同之屬性的 **comInterfaceProxyStub** 子項目。 如果您省略元件的部分 **comInterfaceProxyStub** 相依性，則在進程和執行緒之間封送處理介面可能無法如預期般運作。

**ComInterfaceProxyStub** 元素具有下列屬性。



| 屬性            | 描述                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**              | ，.宣告 proxy 之介面的 IID。 必要。 值的格式應為： "{iid}"。                                                                                                                                                                                        |
| **name**             | 出現在程式碼中的介面名稱。 例如，"IViewObject"。 這不能是描述性字串。 此屬性是選擇性的。 值的格式應為： "name"。                                                                                                                 |
| **tlbid**            | 類型程式庫，其中包含 **iid** 屬性所指定之介面的描述。 此屬性是選擇性的。 值的格式應為： "{tlbid}"。                                                                                                                                 |
| **Typeinterface**    | 由 **iid** 屬性所描述的介面所衍生之介面的 IID。 此屬性是選擇性的。 值的格式應為： "{iid}"。                                                                                                                                            |
| **numMethods**       | 介面所執行的方法數目。 此屬性是選擇性的。 值的格式應為： "n"。                                                                                                                                                                                       |
| **proxyStubClsid32** | 將 IID 對應至32位 proxy Dll 中的 CLSID。                                                                                                                                                                                                                                                                |
| **>threadingmodel**   | 同進程 COM 類別所使用的執行緒模型。 如果此屬性為 null，則不會使用任何執行緒模型。 元件是在用戶端的主執行緒上建立，而來自其他執行緒的呼叫會封送處理至此執行緒。 選擇性。 有效的值為：「公寓」、「免費」、「兩者」和「中性」。 |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**windowclass**
</dt> <dd>

要建立版本的 windows 類別名稱。 **Windowclass** 元素具有下列屬性。



| 屬性     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **版本** | 這個屬性會控制註冊中使用的內部視窗類別名稱是否包含含有視窗類別的元件版本。 這個屬性的值可以是 "yes" 或 "no"。 預設值為 [是]。 只有當並存元件和相等的非並存元件定義了相同的視窗類別，且您想要將它們視為相同的視窗類別時，才應該使用值 "no"。 請注意，有關視窗類別註冊的一般規則只會套用第一個註冊視窗類別的元件，因為它不會建立版本。 |



 

下列範例會顯示包含在 **file** 元素中的 **windowclass** 元素。

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>範例

以下是組件資訊清單的範例。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" 
manifestVersion="1.0">
    <assemblyIdentity type="win32" name="Microsoft.Tools.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="0000000000000000"/>
    <file name="sampleu.dll" hash="3eab067f82504bf271ed38112a4ccdf46094eb5a" hashalg="SHA1">
        <comClass description="Font Property Page" clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Color Property Page" clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Picture Property Page" clsid="{0BE35202-8F91-11CE-9DE3-00AA004BB851}"/>
    </file>
    <file name="bar.dll" hash="ac72753e5bb20446d88a48c8f0aaae769a962338" hashalg="SHA1"/>
    <file name="foo.dll" hash="a7312a1f6cfb46433001e0540458de60adcd5ec5" hashalg="SHA1">
        <comClass description="Registrar Class" clsid="{44EC053A-400F-11D0-9DCD-00A0C90391D3}" progid="ATL.Registrar"/>
    <comInterfaceProxyStub iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" name=" IAxWinAmbientDispatch " tlbid="{34EC053A-400F-11D0-9DCD-00A0C90391D3}"/>
        <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}" version="1.0" helpdir=""/>
    </file>
    <file name="sampledll.dll" hash="ba62960ceb15073d2598379307aad84f3a73dfcb" hashalg="SHA1"/>
<windowClass>ToolbarWindow32</windowClass>
        <windowClass>ComboBoxEx32</windowClass>
        <windowClass>sample_trackbar32</windowClass>
        <windowClass>sample_updown32</windowClass>
</assembly>
```

 

