---
description: 包含有線網路設定檔。
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: LANProfile 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193670"
---
# <a name="lanprofile-element"></a><span data-ttu-id="6409a-103">LANProfile 元素</span><span class="sxs-lookup"><span data-stu-id="6409a-103">LANProfile Element</span></span>

<span data-ttu-id="6409a-104">LANProfile 元素包含有線網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="6409a-104">The LANProfile element contains a wired network profile.</span></span> <span data-ttu-id="6409a-105">此元素是有線網路設定檔的唯一根項目。</span><span class="sxs-lookup"><span data-stu-id="6409a-105">This element is the unique root element for a wired network profile.</span></span>

<span data-ttu-id="6409a-106">LANProfile 元素的目標命名空間為 `https://www.microsoft.com/networking/LAN/profile/v1` 。</span><span class="sxs-lookup"><span data-stu-id="6409a-106">The target namespace for the LANProfile element is `https://www.microsoft.com/networking/LAN/profile/v1`.</span></span>

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
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

## <a name="child-elements"></a><span data-ttu-id="6409a-107">子元素</span><span class="sxs-lookup"><span data-stu-id="6409a-107">Child elements</span></span>



| <span data-ttu-id="6409a-108">元素</span><span class="sxs-lookup"><span data-stu-id="6409a-108">Element</span></span>                                                                 | <span data-ttu-id="6409a-109">類型</span><span class="sxs-lookup"><span data-stu-id="6409a-109">Type</span></span>    | <span data-ttu-id="6409a-110">Description</span><span class="sxs-lookup"><span data-stu-id="6409a-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6409a-111">**MSM**</span><span class="sxs-lookup"><span data-stu-id="6409a-111">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)                 |         | <span data-ttu-id="6409a-112">包含特定媒體模組 (MSM) 設定。</span><span class="sxs-lookup"><span data-stu-id="6409a-112">Contains media-specific module (MSM) settings.</span></span> <br/>                                                                               |
| [<span data-ttu-id="6409a-113">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="6409a-113">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="6409a-114">boolean</span><span class="sxs-lookup"><span data-stu-id="6409a-114">boolean</span></span> | <span data-ttu-id="6409a-115">指定有線網路的自動設定服務是否會嘗試使用 802.1 X 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="6409a-115">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="6409a-116">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="6409a-116">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="6409a-117">boolean</span><span class="sxs-lookup"><span data-stu-id="6409a-117">boolean</span></span> | <span data-ttu-id="6409a-118">指定有線網路的自動設定服務是否需要使用 802.1 X 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="6409a-118">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="6409a-119">**安全**</span><span class="sxs-lookup"><span data-stu-id="6409a-119">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="6409a-120">包含安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6409a-120">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="6409a-121">備註</span><span class="sxs-lookup"><span data-stu-id="6409a-121">Remarks</span></span>

<span data-ttu-id="6409a-122">若要查看樹狀結構中子專案的清單，請參閱 [LAN \_ 設定檔架構元素](lan-profileschema-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="6409a-122">To view the list of child elements in a tree-like structure, see [LAN\_profile Schema Elements](lan-profileschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6409a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6409a-123">Requirements</span></span>



| <span data-ttu-id="6409a-124">需求</span><span class="sxs-lookup"><span data-stu-id="6409a-124">Requirement</span></span> | <span data-ttu-id="6409a-125">值</span><span class="sxs-lookup"><span data-stu-id="6409a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6409a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6409a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6409a-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6409a-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6409a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6409a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6409a-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6409a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




