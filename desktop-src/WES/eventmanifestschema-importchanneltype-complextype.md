---
title: ImportChannelType 複雜類型
description: 識別已由另一個提供者定義或包含中繼資料區段之資訊清單中的通道。
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- ImportChannelType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094536"
---
# <a name="importchanneltype-complex-type"></a><span data-ttu-id="b15b9-104">ImportChannelType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="b15b9-104">ImportChannelType Complex Type</span></span>

<span data-ttu-id="b15b9-105">識別已由另一個提供者定義或包含中繼資料區段之資訊清單中的通道。</span><span class="sxs-lookup"><span data-stu-id="b15b9-105">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span>

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b15b9-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b15b9-106">Attributes</span></span>



| <span data-ttu-id="b15b9-107">名稱</span><span class="sxs-lookup"><span data-stu-id="b15b9-107">Name</span></span>   | <span data-ttu-id="b15b9-108">類型</span><span class="sxs-lookup"><span data-stu-id="b15b9-108">Type</span></span>                                                              | <span data-ttu-id="b15b9-109">Description</span><span class="sxs-lookup"><span data-stu-id="b15b9-109">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b15b9-110">子</span><span class="sxs-lookup"><span data-stu-id="b15b9-110">chid</span></span>   | <span data-ttu-id="b15b9-111">token</span><span class="sxs-lookup"><span data-stu-id="b15b9-111">token</span></span>                                                             | <span data-ttu-id="b15b9-112">此識別碼可唯一識別提供者所定義或匯入通道清單中的通道。</span><span class="sxs-lookup"><span data-stu-id="b15b9-112">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="b15b9-113">在事件定義中參考此通道時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="b15b9-113">Use this value when referencing this channel in an event definition.</span></span> <span data-ttu-id="b15b9-114">如果您未指定通道識別碼，請使用通道的名稱在事件定義中參考這個通道。</span><span class="sxs-lookup"><span data-stu-id="b15b9-114">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/>  |
| <span data-ttu-id="b15b9-115">NAME</span><span class="sxs-lookup"><span data-stu-id="b15b9-115">name</span></span>   | <span data-ttu-id="b15b9-116">anyURI</span><span class="sxs-lookup"><span data-stu-id="b15b9-116">anyURI</span></span>                                                            | <span data-ttu-id="b15b9-117">要匯入的通道名稱。</span><span class="sxs-lookup"><span data-stu-id="b15b9-117">The name of the channel to import.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b15b9-118">符號</span><span class="sxs-lookup"><span data-stu-id="b15b9-118">symbol</span></span> | [<span data-ttu-id="b15b9-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="b15b9-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="b15b9-120">用來參考應用程式中通道的符號。</span><span class="sxs-lookup"><span data-stu-id="b15b9-120">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="b15b9-121">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立通道的常數。</span><span class="sxs-lookup"><span data-stu-id="b15b9-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="b15b9-122">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="b15b9-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b15b9-123">備註</span><span class="sxs-lookup"><span data-stu-id="b15b9-123">Remarks</span></span>

<span data-ttu-id="b15b9-124">您必須先安裝定義匯入通道的資訊清單，才能讓您的提供者寫入事件;否則，無法將事件寫入至通道， (寫入作業成功時，事件就不會寫入通道) 。</span><span class="sxs-lookup"><span data-stu-id="b15b9-124">The manifest that defined the imported channel must be installed before your provider writes events; otherwise, the events cannot be written to the channel (the write operation succeeds, the events are simply not written to the channel).</span></span>

## <a name="requirements"></a><span data-ttu-id="b15b9-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b15b9-125">Requirements</span></span>



| <span data-ttu-id="b15b9-126">需求</span><span class="sxs-lookup"><span data-stu-id="b15b9-126">Requirement</span></span> | <span data-ttu-id="b15b9-127">值</span><span class="sxs-lookup"><span data-stu-id="b15b9-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b15b9-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b15b9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b15b9-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b15b9-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b15b9-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b15b9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b15b9-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b15b9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





