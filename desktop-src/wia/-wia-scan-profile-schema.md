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
# <a name="scan-profile-schema"></a><span data-ttu-id="40164-103">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="40164-103">Scan Profile Schema</span></span>

<span data-ttu-id="40164-104">掃描設定檔架構會定義 XML 格式，可用來儲存 Windows 映像取得 (WIA) 專案的屬性，例如掃描器和攝影機。</span><span class="sxs-lookup"><span data-stu-id="40164-104">The Scan Profile Schema defines an XML format that can be used to store the properties of Windows Image Acquisition (WIA) items, such as scanners and cameras.</span></span> <span data-ttu-id="40164-105">這些持續性檔案可讓應用程式提供自動掃描，而不需要使用者記住專案的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="40164-105">These persistent files enable applications to provide automatic scanning without requiring users to remember the property settings of the items.</span></span>

<span data-ttu-id="40164-106">任何 [**IWiaItem2**](-wia-iwiaitem2.md) 裝置都可以有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="40164-106">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="40164-107">不過，  [WIA \_ 類別目錄 \_ 已完成檔案] 和 [wia 類別根目錄] 類型的 IWiaItem2 專案 \_ \_ \_ 不能有設定檔。</span><span class="sxs-lookup"><span data-stu-id="40164-107">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="40164-108">掃描設定檔是透過 [**IScanProfile**](-wia-iscanprofile.md)、 [**IScanProfileMgr**](-wia-iscanprofilemgr.md)和 [**IScanProfileUI**](-wia-iscanprofileui.md) 介面來建立和管理。</span><span class="sxs-lookup"><span data-stu-id="40164-108">Scan profiles are created and managed through the [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md), and [**IScanProfileUI**](-wia-iscanprofileui.md) interfaces.</span></span> <span data-ttu-id="40164-109">您應用程式的使用者可以使用 [**IScanProfileUI：： ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法，以有限的方式修改設定檔。</span><span class="sxs-lookup"><span data-stu-id="40164-109">Users of your application can modify profiles in limited ways using the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="40164-110">所有掃描設定檔都有下列元素： `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` 、和 `<Properties>` 。</span><span class="sxs-lookup"><span data-stu-id="40164-110">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="40164-111">裝置的預設設定檔也有一個 `<Default>` 元素。</span><span class="sxs-lookup"><span data-stu-id="40164-111">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="40164-112">`<ProfileGUID>` `<DeviceID>` 建立掃描設定檔之後，就無法變更元素和元素。</span><span class="sxs-lookup"><span data-stu-id="40164-112">The `<ProfileGUID>` element and the `<DeviceID>` element cannot be changed after the scan profile is created.</span></span> <span data-ttu-id="40164-113">`<ProfileName>`可以修改元素和元素的值 `<WiaItem>` 。</span><span class="sxs-lookup"><span data-stu-id="40164-113">The values of the `<ProfileName>` element and the `<WiaItem>` element can be modified.</span></span> <span data-ttu-id="40164-114">您 `<Default>` 可以新增或刪除元素。</span><span class="sxs-lookup"><span data-stu-id="40164-114">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="40164-115">您可以使用 [**IScanProfile：： SetName**](-wia-iscanprofile-setname.md)、 [**IScanProfile：： SetItem**](-wia-iscanprofile-setitem.md)和 [**IScanProfileMgr：： SetDefault**](-wia-iscanprofilemgr-setdefault.md) 方法以程式設計方式完成此動作。</span><span class="sxs-lookup"><span data-stu-id="40164-115">This can be done programatically using the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="40164-116">使用者也可以透過 [**IScanProfileUI：： ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法變更這些屬性。</span><span class="sxs-lookup"><span data-stu-id="40164-116">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="40164-117">`<Properties>`元素包含 `<Property>` 子系。</span><span class="sxs-lookup"><span data-stu-id="40164-117">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="40164-118">使用這些專案，將任何 WIA 專案或裝置屬性新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="40164-118">Use these to add any WIA item or device property to the profile.</span></span> <span data-ttu-id="40164-119">您也可以開發自己的映射獲取 `<Property>` 子系。</span><span class="sxs-lookup"><span data-stu-id="40164-119">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="40164-120">這可延伸掃描設定檔架構。</span><span class="sxs-lookup"><span data-stu-id="40164-120">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="40164-121"> (如需延伸架構的詳細資訊，請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)、 [**IScanProfile：： GetProperty**](-wia-iscanprofile-getproperty.md)和 [**IScanProfile：： SetProperty**](-wia-iscanprofile-setproperty.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="40164-121">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

<span data-ttu-id="40164-122">以下是完整的掃描設定檔架構。</span><span class="sxs-lookup"><span data-stu-id="40164-122">Here is the complete Scan Profile Schema.</span></span> <span data-ttu-id="40164-123">範例設定檔如下所示。</span><span class="sxs-lookup"><span data-stu-id="40164-123">A sample profile follows.</span></span>


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



<span data-ttu-id="40164-124">按一下 [ **顯示範例** ] 以查看範例設定檔。</span><span class="sxs-lookup"><span data-stu-id="40164-124">Click **Show Example** to see a sample profile.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="40164-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="40164-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="40164-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="40164-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="40164-127">**IScanProfile：： GetProperty**</span><span class="sxs-lookup"><span data-stu-id="40164-127">**IScanProfile::GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[<span data-ttu-id="40164-128">**IScanProfile：： SetProperty**</span><span class="sxs-lookup"><span data-stu-id="40164-128">**IScanProfile::SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)
</dt> <dt>

<span data-ttu-id="40164-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="40164-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="40164-130">WIA 屬性常數</span><span class="sxs-lookup"><span data-stu-id="40164-130">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="40164-131">定義自訂屬性</span><span class="sxs-lookup"><span data-stu-id="40164-131">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



