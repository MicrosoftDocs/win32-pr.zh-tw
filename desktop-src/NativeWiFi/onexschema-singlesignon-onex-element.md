---
description: 指定單一登入 (SSO) 網路設定資訊。
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: singleSignOn (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993118"
---
# <a name="singlesignon-onex-element"></a><span data-ttu-id="32404-103">singleSignOn (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="32404-103">singleSignOn (OneX) Element</span></span>

<span data-ttu-id="32404-104">SingleSignOn (OneX) 元素會指定單一登入 (SSO) 網路設定資訊。</span><span class="sxs-lookup"><span data-stu-id="32404-104">The singleSignOn (OneX) element specifies single sign-on (SSO) network configuration information.</span></span>

<span data-ttu-id="32404-105">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="32404-105">This element is optional.</span></span> <span data-ttu-id="32404-106">如果網路不需要，請不要在設定檔中使用 singleSignOn 元素。</span><span class="sxs-lookup"><span data-stu-id="32404-106">Do not use the singleSignOn element in a profile if the network does not require it.</span></span>

<span data-ttu-id="32404-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="32404-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="singleSignOn">
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
```

<span data-ttu-id="32404-108">**SingleSignOn** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="32404-108">The **singleSignOn** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="32404-109">子元素</span><span class="sxs-lookup"><span data-stu-id="32404-109">Child elements</span></span>



| <span data-ttu-id="32404-110">元素</span><span class="sxs-lookup"><span data-stu-id="32404-110">Element</span></span>                                                                            | <span data-ttu-id="32404-111">類型</span><span class="sxs-lookup"><span data-stu-id="32404-111">Type</span></span>    | <span data-ttu-id="32404-112">Description</span><span class="sxs-lookup"><span data-stu-id="32404-112">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32404-113">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="32404-113">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="32404-114">指定單一登入連線嘗試失敗之前的延遲上限（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="32404-114">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="32404-115">**類型**</span><span class="sxs-lookup"><span data-stu-id="32404-115">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="32404-116">指定何時執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="32404-116">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="32404-117">當設定為時 `preLogon` ，會在使用者登入之前執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="32404-117">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="32404-118">當設定為時 `postLogon` ，會在使用者登入後立即執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="32404-118">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="32404-119">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="32404-119">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="32404-120">boolean</span><span class="sxs-lookup"><span data-stu-id="32404-120">boolean</span></span> | <span data-ttu-id="32404-121">指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。</span><span class="sxs-lookup"><span data-stu-id="32404-121">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="32404-122">備註</span><span class="sxs-lookup"><span data-stu-id="32404-122">Remarks</span></span>

<span data-ttu-id="32404-123">您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。</span><span class="sxs-lookup"><span data-stu-id="32404-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="32404-124">如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="32404-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="32404-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="32404-125">Requirements</span></span>



| <span data-ttu-id="32404-126">需求</span><span class="sxs-lookup"><span data-stu-id="32404-126">Requirement</span></span> | <span data-ttu-id="32404-127">值</span><span class="sxs-lookup"><span data-stu-id="32404-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32404-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32404-128">Minimum supported client</span></span><br/> | <span data-ttu-id="32404-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32404-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="32404-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32404-130">Minimum supported server</span></span><br/> | <span data-ttu-id="32404-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32404-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32404-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32404-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="32404-133">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="32404-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="32404-134">**OneX**</span><span class="sxs-lookup"><span data-stu-id="32404-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="32404-135">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="32404-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="32404-136">**OneX**</span><span class="sxs-lookup"><span data-stu-id="32404-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
