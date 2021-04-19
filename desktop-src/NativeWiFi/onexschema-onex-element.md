---
description: 指定有線或無線局域網路設定檔的 802.1 X 設定資訊。
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: OneX 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998497"
---
# <a name="onex-element"></a><span data-ttu-id="d0bc0-103">OneX 元素</span><span class="sxs-lookup"><span data-stu-id="d0bc0-103">OneX Element</span></span>

<span data-ttu-id="d0bc0-104">OneX 元素會指定有線或無線局域網路設定檔的 802.1 X 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-104">The OneX element specifies 802.1X configuration information for a wired or wireless LAN profile.</span></span> <span data-ttu-id="d0bc0-105">這個元素是 802.1 X 設定檔的唯一根項目。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-105">This element is the unique root element for an 802.1X profile.</span></span>

<span data-ttu-id="d0bc0-106">OneX 元素的目標命名空間為 `https://www.microsoft.com/networking/OneX/v1` 。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-106">The target namespace for the OneX element is `https://www.microsoft.com/networking/OneX/v1`.</span></span> <span data-ttu-id="d0bc0-107">所有的 OneX 元素子項目都在 `OneX` 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-107">Most child elements of the OneX element are in the `OneX` namespace.</span></span> <span data-ttu-id="d0bc0-108">有一個例外狀況： [**EAPConfig**](onexschema-eapconfig-onex-element.md) 元素位於 `https://www.microsoft.com/provisioning/EapHostConfig` 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-108">There is one exception: the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span>

<span data-ttu-id="d0bc0-109">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 只支援 [**EAPConfig**](onexschema-eapconfig-onex-element.md)元素。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported.</span></span> <span data-ttu-id="d0bc0-110">如果設定檔中有其他專案，則會忽略這些元素。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-110">Other elements, if present in a profile, will be ignored.</span></span>

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="type"
                            minOccurs="1"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="preLogon"
                                     />
                                    <xs:enumeration
                                        value="postLogon"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="maxDelay"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:enumeration
                                        value="0"
                                     />
                                    <xs:enumeration
                                        value="120"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="userBasedVirtualLan"
                            type="boolean"
                            minOccurs="0"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
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

## <a name="child-elements"></a><span data-ttu-id="d0bc0-111">子元素</span><span class="sxs-lookup"><span data-stu-id="d0bc0-111">Child elements</span></span>



| <span data-ttu-id="d0bc0-112">元素</span><span class="sxs-lookup"><span data-stu-id="d0bc0-112">Element</span></span>                                                                            | <span data-ttu-id="d0bc0-113">類型</span><span class="sxs-lookup"><span data-stu-id="d0bc0-113">Type</span></span>    | <span data-ttu-id="d0bc0-114">Description</span><span class="sxs-lookup"><span data-stu-id="d0bc0-114">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0bc0-115">**authMode**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-115">**authMode**</span></span>](onexschema-authmode-onex-element.md)                               |         | <span data-ttu-id="d0bc0-116">指定用於驗證的認證類型。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-116">Specifies the type of credentials used for authentication.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="d0bc0-117">**authPeriod**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-117">**authPeriod**</span></span>](onexschema-authperiod-onex-element.md)                           |         | <span data-ttu-id="d0bc0-118">指定用戶端等候驗證器回應的最大時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-118">Specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="d0bc0-119">**cacheUserData**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-119">**cacheUserData**</span></span>](onexschema-cacheuserdata-onex-element.md)                     | <span data-ttu-id="d0bc0-120">boolean</span><span class="sxs-lookup"><span data-stu-id="d0bc0-120">boolean</span></span> | <span data-ttu-id="d0bc0-121">指定是否快取使用者認證以進行後續連接。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-121">Specifies whether the user credentials are cached for subsequent connections.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="d0bc0-122">**EAPConfig**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-122">**EAPConfig**</span></span>](onexschema-eapconfig-onex-element.md)                             |         | <span data-ttu-id="d0bc0-123">指定 EAPHost 設定。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-123">Specifies the EAPHost configuration.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="d0bc0-124">**heldPeriod**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-124">**heldPeriod**</span></span>](onexschema-heldperiod-onex-element.md)                           |         | <span data-ttu-id="d0bc0-125">指定在驗證嘗試失敗之後，用戶端不會重新嘗試驗證的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-125">Specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span><br/>                                                                             |
| [<span data-ttu-id="d0bc0-126">**maxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-126">**maxAuthFailures**</span></span>](onexschema-maxauthfailures-onex-element.md)                 |         | <span data-ttu-id="d0bc0-127">指定一組認證允許的驗證失敗次數上限。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-127">Specifies the maximum number of authentication failures allowed for a set of credentials.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="d0bc0-128">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-128">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="d0bc0-129">指定單一登入連線嘗試失敗之前的延遲上限（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-129">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d0bc0-130">**maxStart**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-130">**maxStart**</span></span>](onexschema-maxstart-onex-element.md)                               |         | <span data-ttu-id="d0bc0-131">指定傳送 EAPOL-Start 訊息的數目上限。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-131">Specifies the maximum number of EAPOL-Start messages sent.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="d0bc0-132">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-132">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)                       |         | <span data-ttu-id="d0bc0-133">指定單一登入網路設定資訊。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-133">Specifies single sign-on network configuration information.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="d0bc0-134">**startPeriod**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-134">**startPeriod**</span></span>](onexschema-startperiod-onex-element.md)                         |         | <span data-ttu-id="d0bc0-135">指定傳送 EAPOL-Start 之前等候的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-135">Specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="d0bc0-136">**supplicantMode**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-136">**supplicantMode**</span></span>](onexschema-supplicantmode-onex-element.md)                   |         | <span data-ttu-id="d0bc0-137">指定用於 EAPOL 封包的傳輸方法。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-137">Specifies the method of transmission used for EAPOL packets.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="d0bc0-138">**類型**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-138">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="d0bc0-139">指定何時執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-139">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="d0bc0-140">當設定為時 `preLogon` ，會在使用者登入之前執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-140">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="d0bc0-141">當設定為時 `postLogon` ，會在使用者登入後立即執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-141">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="d0bc0-142">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="d0bc0-142">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="d0bc0-143">boolean</span><span class="sxs-lookup"><span data-stu-id="d0bc0-143">boolean</span></span> | <span data-ttu-id="d0bc0-144">指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-144">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="d0bc0-145">備註</span><span class="sxs-lookup"><span data-stu-id="d0bc0-145">Remarks</span></span>

<span data-ttu-id="d0bc0-146">若要查看類似樹狀結構中子專案的清單，請參閱 [OneX 架構元素](onexschema-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="d0bc0-146">To view the list of child elements in a tree-like structure, see [OneX Schema Elements](onexschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0bc0-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0bc0-147">Requirements</span></span>



| <span data-ttu-id="d0bc0-148">需求</span><span class="sxs-lookup"><span data-stu-id="d0bc0-148">Requirement</span></span> | <span data-ttu-id="d0bc0-149">值</span><span class="sxs-lookup"><span data-stu-id="d0bc0-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d0bc0-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0bc0-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d0bc0-151">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0bc0-151">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d0bc0-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0bc0-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d0bc0-153">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0bc0-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d0bc0-154">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d0bc0-154">Redistributable</span></span><br/>          | <span data-ttu-id="d0bc0-155">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="d0bc0-155">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




