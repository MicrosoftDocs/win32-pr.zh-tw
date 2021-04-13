---
title: 通道 (MetadataType) 元素
description: 定義提供者可以記錄事件的通道清單。 |通道 (MetadataType) 元素
ms.assetid: ead7317f-29ec-43d2-a588-7915c8e74dc1
keywords:
- 通道元素 EventLog
topic_type:
- apiref
api_name:
- channels
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9511972faf279917057d522872ecbd72710e42d6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322363"
---
# <a name="channels-metadatatype-element"></a><span data-ttu-id="6c509-105">通道 (MetadataType) 元素</span><span class="sxs-lookup"><span data-stu-id="6c509-105">channels (MetadataType) Element</span></span>

<span data-ttu-id="6c509-106">定義提供者可以記錄事件的通道清單。</span><span class="sxs-lookup"><span data-stu-id="6c509-106">Defines a list of channels to which providers can log events.</span></span>

``` syntax
<xs:element name="channels"
    type="ChannelListType"
 />
```

<span data-ttu-id="6c509-107">**通道** 元素是由 [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="6c509-107">The **channels** element is defined by the [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c509-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c509-108">Requirements</span></span>



| <span data-ttu-id="6c509-109">需求</span><span class="sxs-lookup"><span data-stu-id="6c509-109">Requirement</span></span> | <span data-ttu-id="6c509-110">值</span><span class="sxs-lookup"><span data-stu-id="6c509-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c509-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c509-111">Minimum supported client</span></span><br/> | <span data-ttu-id="6c509-112">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c509-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c509-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c509-113">Minimum supported server</span></span><br/> | <span data-ttu-id="6c509-114">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c509-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c509-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c509-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c509-116">**父元素**</span><span class="sxs-lookup"><span data-stu-id="6c509-116">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="6c509-117">**中繼資料 (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="6c509-117">**metadata (instrumentationManifest)**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





