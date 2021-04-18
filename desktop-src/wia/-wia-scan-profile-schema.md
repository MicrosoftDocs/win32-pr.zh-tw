---
description: 掃描設定檔架構會定義 XML 格式，可用來儲存 Windows 映像取得 (WIA) 專案的屬性，例如掃描器和攝影機。
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: 掃描設定檔架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971223"
---
# <a name="scan-profile-schema"></a>掃描設定檔架構

掃描設定檔架構會定義 XML 格式，可用來儲存 Windows 映像取得 (WIA) 專案的屬性，例如掃描器和攝影機。 這些持續性檔案可讓應用程式提供自動掃描，而不需要使用者記住專案的屬性設定。

任何 [**IWiaItem2**](-wia-iwiaitem2.md) 裝置都可以有掃描設定檔。 不過，  [WIA \_ 類別目錄 \_ 已完成檔案] 和 [wia 類別根目錄] 類型的 IWiaItem2 專案 \_ \_ \_ 不能有設定檔。

掃描設定檔是透過 [**IScanProfile**](-wia-iscanprofile.md)、 [**IScanProfileMgr**](-wia-iscanprofilemgr.md)和 [**IScanProfileUI**](-wia-iscanprofileui.md) 介面來建立和管理。 您應用程式的使用者可以使用 [**IScanProfileUI：： ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法，以有限的方式修改設定檔。

所有掃描設定檔都有下列元素： `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` 、和 `<Properties>` 。 裝置的預設設定檔也有一個 `<Default>` 元素。

`<ProfileGUID>` `<DeviceID>` 建立掃描設定檔之後，就無法變更元素和元素。 `<ProfileName>`可以修改元素和元素的值 `<WiaItem>` 。 您 `<Default>` 可以新增或刪除元素。 您可以使用 [**IScanProfile：： SetName**](-wia-iscanprofile-setname.md)、 [**IScanProfile：： SetItem**](-wia-iscanprofile-setitem.md)和 [**IScanProfileMgr：： SetDefault**](-wia-iscanprofilemgr-setdefault.md) 方法以程式設計方式完成此動作。 使用者也可以透過 [**IScanProfileUI：： ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法變更這些屬性。

`<Properties>`元素包含 `<Property>` 子系。 使用這些專案，將任何 WIA 專案或裝置屬性新增至設定檔。 您也可以開發自己的映射獲取 `<Property>` 子系。 這可延伸掃描設定檔架構。  (如需延伸架構的詳細資訊，請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)、 [**IScanProfile：： GetProperty**](-wia-iscanprofile-getproperty.md)和 [**IScanProfile：： SetProperty**](-wia-iscanprofile-setproperty.md)。 ) 

以下是完整的掃描設定檔架構。 範例設定檔如下所示。


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



按一下 [ **顯示範例** ] 以查看範例設定檔。


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IScanProfile：： GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**IScanProfile：： SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**概念**
</dt> <dt>

[WIA 屬性常數](-wia-wia-property-constants.md)
</dt> <dt>

[定義自訂屬性](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



