---
description: 包含特定媒體模組 (MSM) 設定。
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: MSM (LANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193668"
---
# <a name="msm-lanprofile-element"></a><span data-ttu-id="961f2-103">MSM (LANProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="961f2-103">MSM (LANProfile) Element</span></span>

<span data-ttu-id="961f2-104">MSM (LANProfile) 元素包含媒體專屬模組 (MSM) 設定。</span><span class="sxs-lookup"><span data-stu-id="961f2-104">The MSM (LANProfile) element contains media-specific module (MSM) settings.</span></span>

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="security">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OneXEnforced"
                            type="boolean"
                         />
                        <xs:element name="OneXEnabled"
                            type="boolean"
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

<span data-ttu-id="961f2-105">**MSM** 元素是由 [**LANProfile**](lan-profileschema-lanprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="961f2-105">The **MSM** element is defined by the [**LANProfile**](lan-profileschema-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="961f2-106">子元素</span><span class="sxs-lookup"><span data-stu-id="961f2-106">Child elements</span></span>



| <span data-ttu-id="961f2-107">元素</span><span class="sxs-lookup"><span data-stu-id="961f2-107">Element</span></span>                                                                 | <span data-ttu-id="961f2-108">類型</span><span class="sxs-lookup"><span data-stu-id="961f2-108">Type</span></span>    | <span data-ttu-id="961f2-109">Description</span><span class="sxs-lookup"><span data-stu-id="961f2-109">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="961f2-110">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="961f2-110">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="961f2-111">boolean</span><span class="sxs-lookup"><span data-stu-id="961f2-111">boolean</span></span> | <span data-ttu-id="961f2-112">指定有線網路的自動設定服務是否會嘗試使用 802.1 X 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="961f2-112">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span><br/>       |
| [<span data-ttu-id="961f2-113">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="961f2-113">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="961f2-114">boolean</span><span class="sxs-lookup"><span data-stu-id="961f2-114">boolean</span></span> | <span data-ttu-id="961f2-115">指定有線網路的自動設定服務是否需要使用 802.1 X 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="961f2-115">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="961f2-116">**安全**</span><span class="sxs-lookup"><span data-stu-id="961f2-116">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="961f2-117">包含安全性設定。</span><span class="sxs-lookup"><span data-stu-id="961f2-117">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="961f2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="961f2-118">Requirements</span></span>



| <span data-ttu-id="961f2-119">需求</span><span class="sxs-lookup"><span data-stu-id="961f2-119">Requirement</span></span> | <span data-ttu-id="961f2-120">值</span><span class="sxs-lookup"><span data-stu-id="961f2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="961f2-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="961f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="961f2-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="961f2-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="961f2-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="961f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="961f2-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="961f2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="961f2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="961f2-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="961f2-126">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="961f2-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="961f2-127">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="961f2-127">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="961f2-128">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="961f2-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="961f2-129">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="961f2-129">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




