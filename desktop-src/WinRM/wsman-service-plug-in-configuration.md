---
title: WinRM 服務外掛程式設定
description: Windows 遠端管理 (WinRM) 外掛程式必須在 WinRM 類別目錄中註冊，才能讓基礎結構動態地判斷可用的外掛程式集合，以及它們所支援的資源 Uri。
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316735"
---
# <a name="winrm-service-plug-in-configuration"></a>WinRM 服務外掛程式設定

Windows 遠端管理 (WinRM) 外掛程式必須在 WinRM 類別目錄中註冊，才能讓基礎結構動態地判斷可用的外掛程式集合，以及它們所支援的 [*資源 uri*](windows-remote-management-glossary.md) 。 WinRM 外掛程式的所有 [*資源 uri*](windows-remote-management-glossary.md) 都應符合 RFC 3986 () 中所定義的格式 [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) 。 設定是透過主要 WinRM 服務完成。

下列命令會向 WinRM 服務註冊外掛程式設定：

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> WinRM 服務需要重新開機才能公開新註冊的外掛程式。

外掛程式設定是以 XML 指定的。 以下是一個範例。

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



下列清單會更詳細地描述 XML 元素，後面接著指定為 XSD 的設定架構。

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** /**OperationsConfiguration**
</dt> <dd>

指定作業外掛程式的檔案名。 當要求進入時，會在使用者的內容中展開任何放置於此專案中的環境變數。 每個使用者可能會有相同環境變數的不同版本，因此每個使用者最後可能會有不同的外掛程式。 這個專案不能空白，且必須指向有效的外掛程式。

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** /**名稱**
</dt> <dd>

指定要用於外掛程式的顯示名稱。 如果從外掛程式傳回錯誤，則會將此名稱放入傳回給用戶端應用程式的錯誤 XML。 名稱不是地區設定特定名稱。

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** /**架構**
</dt> <dd>

指定作業外掛程式是否為32位或64位。 如果未指定這個元素，則在 x86 系統上的值會預設為 "32"，在64位系統上則會預設為 "64"。 若是 x86 系統，唯一有效的值是 "32"。 如果在64位系統上的值是 "32"，則在輸入 **檔案名** 資訊時必須將 wow64 重新導向列入考慮。 基礎檔案系統會使用 wow64 重新導向，將 system32 轉譯為 syswow64。 例如，如果 **Filename** 是 "% windir% \\ system32 \\myplugin.dll" 且 **架構** 為 "32"，則實際的外掛程式檔案位於 "% windir% \\ syswow64 \\myplugin.dll"。

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** /**XmlRenderingType**
</dt> <dd>

設定 XML 透過 [**WSMAN \_ 資料**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) 物件傳遞至外掛程式的格式。 目前有下列類型可供使用：

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本
</dt> <dd>

傳入的 XML 資料會包含在 WSMAN \_ 資料 \_ 類型 \_ 文字結構中，這表示 xml 為 **PCWSTR** 記憶體緩衝區。

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader
</dt> <dd>

傳入的 XML 資料會包含在 WSMAN \_ 資料 \_ 類型 \_ WS \_ XML \_ 讀取器結構中，它會將 XML 表示為 **XmlReader** 物件，該物件是定義于 WebServices .h 標頭檔中。

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** /**InitializationXml**
</dt> <dd>

這個節點是選擇性的，可讓外掛程式設定將傳遞給 [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)方法的額外 XML。 大部分的外掛程式都不需要這項額外的資訊，但如果外掛程式需要在需要不同執行時間語義的多個案例下使用，則此 XML 將會賦予外掛程式彈性來執行這項作業。

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** /**資源**
</dt> <dd>

指定此外掛程式支援的 [*資源 uri*](windows-remote-management-glossary.md)清單。 至少必須指定一個 **ResourceUri** 專案;否則，XML 將會遭到拒絕。

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** /**資源** /**資源**
</dt> <dd>

代表單一 [*資源 URI*](windows-remote-management-glossary.md)設定。

> [!Note]  
> **SupportsOptions** 屬性可以設定為 false。 如果 **SupportsOptions** 設定為 false，則列舉資源時，不會列出此屬性。

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** /**資源** /**資源** /**ResourceUri**
</dt> <dd>

以 full 或 **ExactMatch** 屬性為基礎的部分相符字串，指定單一 [*資源 URI*](windows-remote-management-glossary.md) 。 如果 **ExactMatch** 不存在，則會預設為 **False**，這表示 WinRM SOAP 處理器會對 *資源 URI* 的開頭進行部分相符，如果有相符的值，請將它傳遞給外掛程式。 如果允許此 *資源 URI* 傳入任何選項，則可以指定 **SupportsOptions** 屬性。 根據預設，不支援任何選項，如果用戶端要求中有任何選項，則會傳回錯誤。 如果外掛程式支援選項，則如果有外掛程式無法理解當 **mustUnderstand** 旗標設為 **True** 的選項時，外掛程式就會傳回正確的錯誤，這是很重要的。

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** /**資源** /**資源** /**功能**
</dt> <dd>

指定可在此 [*資源 URI*](windows-remote-management-glossary.md)上使用的功能。 它支援的每一種作業類型都會有一個專案。 可用選項如下：

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>獲取
</dt> <dd>

[*資源 URI*](windows-remote-management-glossary.md)支援 Get 作業。 如果 get 作業支援這個概念，就會使用 **SupportFragment** 屬性。 **SupportFiltering** 屬性無效，應設定為 false。 如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>把
</dt> <dd>

[*資源 URI*](windows-remote-management-glossary.md)支援 Put 作業。 如果 put 作業支援這個概念，就會使用 **SupportFragment** 屬性。 **SupportFiltering** 屬性無效，應設定為 **False**。 如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>創建
</dt> <dd>

[*資源 URI*](windows-remote-management-glossary.md)支援建立作業。 如果建立作業支援這個概念，就會使用 **SupportFragment** 屬性。 **SupportFiltering** 屬性無效，應設定為 **False**。 如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>刪除
</dt> <dd>

[*資源 URI*](windows-remote-management-glossary.md)支援刪除作業。 如果刪除作業支援這個概念，就會使用 **SupportFragment** 屬性。 **SupportFiltering** 屬性無效，應設定為 **False**。 如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>調用
</dt> <dd>

[*資源 URI*](windows-remote-management-glossary.md)支援 Invoke 作業。 Invoke 作業不支援 **SupportFragment** 屬性，應設定為 false。 **SupportFiltering** 屬性無效，應設定為 **False**。 如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>枚舉
</dt> <dd>

[*資源 URI*](windows-remote-management-glossary.md)支援列舉作業。 列舉作業不支援 **SupportFragment** 屬性，應設定為 **False**。 **SupportFiltering** 屬性是有效的，而且如果外掛程式支援篩選，則應該將此屬性設定為 **True**。 如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>訂閱
</dt> <dd>

[*資源 URI*](windows-remote-management-glossary.md)支援訂閱作業。 訂閱作業不支援 **SupportFragment** 屬性，應設定為 **False**。 **SupportFiltering** 屬性無效，應設定為 **False**。 如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>殼
</dt> <dd>

[*資源 URI*](windows-remote-management-glossary.md)支援 Shell 作業。 Shell 作業不支援 **SupportFragment** 屬性，應設定為 **False**。 **SupportFiltering** 屬性無效，應設定為 **False**。 如果也支援任何其他作業功能，這項功能對 *資源 URI* 而言是不正確。 如果 shell 作業功能設定為 *資源 URI*，則 get、put、create、delete、invoke 和列舉作業會在 WinRm 服務內部處理，以管理 shell。 因此，外掛程式無法處理作業本身。

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** /**資源** /**資源** /**安全性**
</dt> <dd>

這個元素會透過 **Sddl** 屬性定義安全描述項 (，) 應該套用此屬性，以透過 **URI** 屬性) 來判斷特定 [*資源 URI*](windows-remote-management-glossary.md) (的存取權。 如果 **ExactMatch** 不存在，**安全性** 元素就會預設為 **False**，這表示 **Sddl** 會套用至共用 **Uri** 做為前置詞的所有 *資源 uri* 。 如果 **ExactMatch** 設定為 true，則 **Sddl** 只適用于指定的確切 **Uri** 。 如果有多個可套用至特定 *資源 uri* 的 **安全性** 專案，則會使用最長的前置詞比對來判斷適當的 **Sddl**。 由於有最長的前置詞相符專案，因此，如果有完全相符的 **Uri** 專案存在，一律會將其選擇為適當的安全性元素。

</dd> </dl>

以下是指定為 XSD 的外掛程式設定架構。

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




