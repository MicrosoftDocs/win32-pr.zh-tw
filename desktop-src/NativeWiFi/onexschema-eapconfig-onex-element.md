---
description: 指定 EAPHost 設定。
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: EAPConfig (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979132"
---
# <a name="eapconfig-onex-element"></a><span data-ttu-id="36c1b-103">EAPConfig (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="36c1b-103">EAPConfig (OneX) Element</span></span>

<span data-ttu-id="36c1b-104">**EAPConfig** (OneX) 元素會指定 EAPHost 設定。</span><span class="sxs-lookup"><span data-stu-id="36c1b-104">The **EAPConfig** (OneX) element specifies the EAPHost configuration.</span></span>

<span data-ttu-id="36c1b-105">不同于 802.1 X 設定檔架構中的大部分元素，此專案位於 `https://www.microsoft.com/provisioning/EapHostConfig` 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="36c1b-105">Unlike most elements in the 802.1X profile schema, this element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span> <span data-ttu-id="36c1b-106">其子項目是在 [eaphostconfig 架構](../eaphost/eaphostconfigschema-schema.md)中定義。</span><span class="sxs-lookup"><span data-stu-id="36c1b-106">Its child elements are defined in the [eaphostconfig schema](../eaphost/eaphostconfigschema-schema.md).</span></span> <span data-ttu-id="36c1b-107">[**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md)元素是 **EAPConfig** 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="36c1b-107">The [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) element is a child of the **EAPConfig** element.</span></span>

``` syntax
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
```

<span data-ttu-id="36c1b-108">**EAPConfig** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="36c1b-108">The **EAPConfig** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="36c1b-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="36c1b-109">Requirements</span></span>



| <span data-ttu-id="36c1b-110">需求</span><span class="sxs-lookup"><span data-stu-id="36c1b-110">Requirement</span></span> | <span data-ttu-id="36c1b-111">值</span><span class="sxs-lookup"><span data-stu-id="36c1b-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="36c1b-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36c1b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="36c1b-113">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36c1b-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="36c1b-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36c1b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="36c1b-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36c1b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="36c1b-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="36c1b-116">Redistributable</span></span><br/>          | <span data-ttu-id="36c1b-117">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="36c1b-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="36c1b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36c1b-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="36c1b-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="36c1b-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="36c1b-120">**OneX**</span><span class="sxs-lookup"><span data-stu-id="36c1b-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="36c1b-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="36c1b-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="36c1b-122">**OneX**</span><span class="sxs-lookup"><span data-stu-id="36c1b-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
