---
title: sidType (ChannelPublishingType) 元素
description: 決定是否要包含主體的安全識別碼 (SID) ，並將每個事件寫入通道。
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- sidType 元素 EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968174"
---
# <a name="sidtype-channelpublishingtype-element"></a><span data-ttu-id="45f37-104">sidType (ChannelPublishingType) 元素</span><span class="sxs-lookup"><span data-stu-id="45f37-104">sidType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="45f37-105">決定是否要包含主體的安全識別碼 (SID) ，並將每個事件寫入通道。</span><span class="sxs-lookup"><span data-stu-id="45f37-105">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span>

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="45f37-106">**SidType** 元素是由 [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="45f37-106">The **sidType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f37-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="45f37-107">Requirements</span></span>



| <span data-ttu-id="45f37-108">需求</span><span class="sxs-lookup"><span data-stu-id="45f37-108">Requirement</span></span> | <span data-ttu-id="45f37-109">值</span><span class="sxs-lookup"><span data-stu-id="45f37-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45f37-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45f37-110">Minimum supported client</span></span><br/> | <span data-ttu-id="45f37-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45f37-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="45f37-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45f37-112">Minimum supported server</span></span><br/> | <span data-ttu-id="45f37-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45f37-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45f37-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45f37-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="45f37-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="45f37-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="45f37-116">**發行 (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="45f37-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





