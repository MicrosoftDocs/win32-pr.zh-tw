---
description: 這是識別行動寬頻設定檔的根項目。
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: MBNProfile 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 7016d492a70192a7d6accdcb3aaa57a9c564960e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970443"
---
# <a name="mbnprofile-element"></a><span data-ttu-id="731ca-103">MBNProfile 元素</span><span class="sxs-lookup"><span data-stu-id="731ca-103">MBNProfile Element</span></span>

<span data-ttu-id="731ca-104">**MBNProfile** 元素是識別 Mobile 寬頻設定檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="731ca-104">The **MBNProfile** element is the root element that identifies a Mobile Broadband profile.</span></span>

<span data-ttu-id="731ca-105">每份檔只能有一個此類型的元素。</span><span class="sxs-lookup"><span data-stu-id="731ca-105">There can only be one element of this type per document.</span></span>

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="731ca-106">子元素</span><span class="sxs-lookup"><span data-stu-id="731ca-106">Child elements</span></span>



| <span data-ttu-id="731ca-107">元素</span><span class="sxs-lookup"><span data-stu-id="731ca-107">Element</span></span>                                                                          | <span data-ttu-id="731ca-108">類型</span><span class="sxs-lookup"><span data-stu-id="731ca-108">Type</span></span>                                                           | <span data-ttu-id="731ca-109">Description</span><span class="sxs-lookup"><span data-stu-id="731ca-109">Description</span></span>                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="731ca-110">**AutoConnectOnInternet**</span><span class="sxs-lookup"><span data-stu-id="731ca-110">**AutoConnectOnInternet**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md) | <span data-ttu-id="731ca-111">boolean</span><span class="sxs-lookup"><span data-stu-id="731ca-111">boolean</span></span>                                                        | <span data-ttu-id="731ca-112">裝置是否會自動連接。</span><span class="sxs-lookup"><span data-stu-id="731ca-112">Whether the device will automatically connect.</span></span><br/> |
| [<span data-ttu-id="731ca-113">**ConnectionMode**</span><span class="sxs-lookup"><span data-stu-id="731ca-113">**ConnectionMode**</span></span>](schema-connectionmode-mbnprofile-element.md)               |                                                                | <span data-ttu-id="731ca-114">裝置自動連線設定。</span><span class="sxs-lookup"><span data-stu-id="731ca-114">The device auto connection settings.</span></span><br/>           |
| [<span data-ttu-id="731ca-115">**Context**</span><span class="sxs-lookup"><span data-stu-id="731ca-115">**Context**</span></span>](schema-context-mbnprofile-element.md)                             | [<span data-ttu-id="731ca-116">**coNtextType**</span><span class="sxs-lookup"><span data-stu-id="731ca-116">**contextType**</span></span>](schema-contexttype-complextype.md)          | <span data-ttu-id="731ca-117">資料連線設定參數。</span><span class="sxs-lookup"><span data-stu-id="731ca-117">Data connection setup parameters.</span></span><br/>              |
| [<span data-ttu-id="731ca-118">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="731ca-118">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | <span data-ttu-id="731ca-119">慣用的漫遊網路提供者。</span><span class="sxs-lookup"><span data-stu-id="731ca-119">Preferred network providers for roaming.</span></span><br/>       |
| [<span data-ttu-id="731ca-120">**描述**</span><span class="sxs-lookup"><span data-stu-id="731ca-120">**Description**</span></span>](schema-description-mbnprofile-element.md)                     | [<span data-ttu-id="731ca-121">**nameType**</span><span class="sxs-lookup"><span data-stu-id="731ca-121">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="731ca-122">設定檔的描述。</span><span class="sxs-lookup"><span data-stu-id="731ca-122">Description of the profile.</span></span><br/>                    |
| [<span data-ttu-id="731ca-123">**HomeProviderName**</span><span class="sxs-lookup"><span data-stu-id="731ca-123">**HomeProviderName**</span></span>](schema-homeprovidername-mbnprofile-element.md)           | [<span data-ttu-id="731ca-124">**providerNameType**</span><span class="sxs-lookup"><span data-stu-id="731ca-124">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="731ca-125">首頁提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="731ca-125">Name of the home provider.</span></span><br/>                     |
| [<span data-ttu-id="731ca-126">**ICONFilePath**</span><span class="sxs-lookup"><span data-stu-id="731ca-126">**ICONFilePath**</span></span>](schema-iconfilepath-mbnprofile-element.md)                   | [<span data-ttu-id="731ca-127">**iconFileType**</span><span class="sxs-lookup"><span data-stu-id="731ca-127">**iconFileType**</span></span>](schema-iconfiletype-simpletype.md)         | <span data-ttu-id="731ca-128">圖示檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="731ca-128">Path to the icon file.</span></span><br/>                         |
| [<span data-ttu-id="731ca-129">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="731ca-129">**IsDefault**</span></span>](schema-isdefault-mbnprofile-element.md)                         | <span data-ttu-id="731ca-130">boolean</span><span class="sxs-lookup"><span data-stu-id="731ca-130">boolean</span></span>                                                        | <span data-ttu-id="731ca-131">設定檔是否為預設值。</span><span class="sxs-lookup"><span data-stu-id="731ca-131">Whether the profile is the default.</span></span><br/>            |
| [<span data-ttu-id="731ca-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="731ca-132">**Name**</span></span>](schema-name-mbnprofile-element.md)                                   | [<span data-ttu-id="731ca-133">**nameType**</span><span class="sxs-lookup"><span data-stu-id="731ca-133">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="731ca-134">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="731ca-134">Name of the profile.</span></span><br/>                           |
| [<span data-ttu-id="731ca-135">**ProfileCreationType**</span><span class="sxs-lookup"><span data-stu-id="731ca-135">**ProfileCreationType**</span></span>](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | <span data-ttu-id="731ca-136">設定檔建立者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="731ca-136">Information about the profile creator.</span></span><br/>         |
| [<span data-ttu-id="731ca-137">**SimIccID**</span><span class="sxs-lookup"><span data-stu-id="731ca-137">**SimIccID**</span></span>](schema-simiccid-mbnprofile-element.md)                           | [<span data-ttu-id="731ca-138">**simIccIDType**</span><span class="sxs-lookup"><span data-stu-id="731ca-138">**simIccIDType**</span></span>](schema-simiccidtype-simpletype.md)         | <span data-ttu-id="731ca-139">GSM 裝置的 SIM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="731ca-139">SIM identification number for GSM devices.</span></span><br/>     |
| [<span data-ttu-id="731ca-140">**SubscriberID**</span><span class="sxs-lookup"><span data-stu-id="731ca-140">**SubscriberID**</span></span>](schema-subscriberid-mbnprofile-element.md)                   | [<span data-ttu-id="731ca-141">**subscriberIdType**</span><span class="sxs-lookup"><span data-stu-id="731ca-141">**subscriberIdType**</span></span>](schema-subscriberidtype-simpletype.md) | <span data-ttu-id="731ca-142">設定檔的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="731ca-142">Unique identifier of the profile.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="731ca-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="731ca-143">Requirements</span></span>



| <span data-ttu-id="731ca-144">需求</span><span class="sxs-lookup"><span data-stu-id="731ca-144">Requirement</span></span> | <span data-ttu-id="731ca-145">值</span><span class="sxs-lookup"><span data-stu-id="731ca-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="731ca-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="731ca-146">Minimum supported client</span></span><br/> | <span data-ttu-id="731ca-147">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="731ca-147">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="731ca-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="731ca-148">Minimum supported server</span></span><br/> | <span data-ttu-id="731ca-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="731ca-149">None supported</span></span><br/>                         |



 

 




