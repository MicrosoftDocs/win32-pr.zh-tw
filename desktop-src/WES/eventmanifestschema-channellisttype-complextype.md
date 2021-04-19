---
title: ChannelListType 複雜類型
description: 定義提供者可以記錄事件的通道清單。 |ChannelListType 複雜類型
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- ChannelListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106975643"
---
# <a name="channellisttype-complex-type"></a><span data-ttu-id="a3583-105">ChannelListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="a3583-105">ChannelListType Complex Type</span></span>

<span data-ttu-id="a3583-106">定義提供者可以記錄事件的通道清單。</span><span class="sxs-lookup"><span data-stu-id="a3583-106">Defines a list of channels to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a3583-107">子元素</span><span class="sxs-lookup"><span data-stu-id="a3583-107">Child elements</span></span>



| <span data-ttu-id="a3583-108">元素</span><span class="sxs-lookup"><span data-stu-id="a3583-108">Element</span></span>                                                                            | <span data-ttu-id="a3583-109">類型</span><span class="sxs-lookup"><span data-stu-id="a3583-109">Type</span></span>                                                                           | <span data-ttu-id="a3583-110">Description</span><span class="sxs-lookup"><span data-stu-id="a3583-110">Description</span></span>                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3583-111">**通道**</span><span class="sxs-lookup"><span data-stu-id="a3583-111">**channel**</span></span>](eventmanifestschema-channel-channellisttype-element.md)             | [<span data-ttu-id="a3583-112">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="a3583-112">**ChannelType**</span></span>](eventmanifestschema-channeltype-complextype.md)             | <span data-ttu-id="a3583-113">定義可以記錄事件的通道。</span><span class="sxs-lookup"><span data-stu-id="a3583-113">Defines a channel to which events can be logged.</span></span><br/>                                                                  |
| [<span data-ttu-id="a3583-114">**importChannel**</span><span class="sxs-lookup"><span data-stu-id="a3583-114">**importChannel**</span></span>](eventmanifestschema-importchannel-channellisttype-element.md) | [<span data-ttu-id="a3583-115">**ImportChannelType**</span><span class="sxs-lookup"><span data-stu-id="a3583-115">**ImportChannelType**</span></span>](eventmanifestschema-importchanneltype-complextype.md) | <span data-ttu-id="a3583-116">識別已由另一個提供者定義或包含中繼資料區段之資訊清單中的通道。</span><span class="sxs-lookup"><span data-stu-id="a3583-116">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a3583-117">備註</span><span class="sxs-lookup"><span data-stu-id="a3583-117">Remarks</span></span>

<span data-ttu-id="a3583-118">您可以指定最多8個通道 (您定義) 的任何匯入通道或通道組合。</span><span class="sxs-lookup"><span data-stu-id="a3583-118">You can specify up to eight channels (any combination of imported channels or channels that you define).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3583-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3583-119">Requirements</span></span>



| <span data-ttu-id="a3583-120">需求</span><span class="sxs-lookup"><span data-stu-id="a3583-120">Requirement</span></span> | <span data-ttu-id="a3583-121">值</span><span class="sxs-lookup"><span data-stu-id="a3583-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a3583-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3583-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a3583-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3583-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a3583-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3583-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a3583-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3583-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





