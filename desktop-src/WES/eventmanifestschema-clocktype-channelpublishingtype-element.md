---
title: clockType (ChannelPublishingType) 元素
description: 記錄每個事件的時間戳記時，所要使用的時鐘解析。
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- clockType 元素 EventLog
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384029"
---
# <a name="clocktype-channelpublishingtype-element"></a><span data-ttu-id="09ea0-104">clockType (ChannelPublishingType) 元素</span><span class="sxs-lookup"><span data-stu-id="09ea0-104">clockType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="09ea0-105">記錄每個事件的時間戳記時，所要使用的時鐘解析。</span><span class="sxs-lookup"><span data-stu-id="09ea0-105">The clock resolution to use when logging the time stamp for each event.</span></span>

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="09ea0-106">**ClockType** 元素是由 [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="09ea0-106">The **clockType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ea0-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="09ea0-107">Requirements</span></span>



| <span data-ttu-id="09ea0-108">需求</span><span class="sxs-lookup"><span data-stu-id="09ea0-108">Requirement</span></span> | <span data-ttu-id="09ea0-109">值</span><span class="sxs-lookup"><span data-stu-id="09ea0-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09ea0-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09ea0-110">Minimum supported client</span></span><br/> | <span data-ttu-id="09ea0-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09ea0-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09ea0-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09ea0-112">Minimum supported server</span></span><br/> | <span data-ttu-id="09ea0-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09ea0-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09ea0-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09ea0-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="09ea0-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="09ea0-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="09ea0-116">**發行 (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="09ea0-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





