---
title: instrumentationManifest 元素
description: 資訊清單的根節點。
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- instrumentationManifest 元素 EventLog
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104195831"
---
# <a name="instrumentationmanifest-element"></a><span data-ttu-id="6f4e0-104">instrumentationManifest 元素</span><span class="sxs-lookup"><span data-stu-id="6f4e0-104">instrumentationManifest Element</span></span>

<span data-ttu-id="6f4e0-105">資訊清單的根節點。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-105">The root node of the manifest.</span></span>

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="6f4e0-106">子元素</span><span class="sxs-lookup"><span data-stu-id="6f4e0-106">Child elements</span></span>



| <span data-ttu-id="6f4e0-107">元素</span><span class="sxs-lookup"><span data-stu-id="6f4e0-107">Element</span></span>                                                                                        | <span data-ttu-id="6f4e0-108">類型</span><span class="sxs-lookup"><span data-stu-id="6f4e0-108">Type</span></span>                                                                               | <span data-ttu-id="6f4e0-109">Description</span><span class="sxs-lookup"><span data-stu-id="6f4e0-109">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f4e0-110">**儀錶**</span><span class="sxs-lookup"><span data-stu-id="6f4e0-110">**instrumentation**</span></span>](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [<span data-ttu-id="6f4e0-111">**Instrumentationtype.event**</span><span class="sxs-lookup"><span data-stu-id="6f4e0-111">**InstrumentationType**</span></span>](eventmanifestschema-instrumentationtype-complextype.md) | <span data-ttu-id="6f4e0-112">此區段會定義一或多個事件提供者，以及它們所記錄的事件。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-112">This section defines one or more event providers and the events that they log.</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="6f4e0-113">**定位**</span><span class="sxs-lookup"><span data-stu-id="6f4e0-113">**localization**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [<span data-ttu-id="6f4e0-114">**LocalizationType**</span><span class="sxs-lookup"><span data-stu-id="6f4e0-114">**LocalizationType**</span></span>](eventmanifestschema-localizationtype-complextype.md)       | <span data-ttu-id="6f4e0-115">此區段會定義取用者用來顯示的當地語系化訊息字串。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-115">This section defines the localized message strings that consumers use for display.</span></span> <span data-ttu-id="6f4e0-116">例如，此區段會包含提供者名稱的當地語系化訊息字串、您所定義的事件，以及您定義的任何事件屬性，例如通道、工作和作業碼。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-116">For example, this section would contain the localized message string for the name of your provider, the events that you define, and any event attributes that you define, such as channels, tasks, and opcodes.</span></span><br/> |
| [<span data-ttu-id="6f4e0-117">**元**</span><span class="sxs-lookup"><span data-stu-id="6f4e0-117">**metadata**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [<span data-ttu-id="6f4e0-118">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="6f4e0-118">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)               | <span data-ttu-id="6f4e0-119">此區段會定義其他資訊清單可以使用的元資料類型。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-119">This section defines metadata types that other manifests can use.</span></span> <span data-ttu-id="6f4e0-120">如需範例，請參閱 Windows SDK 的 Include 資料夾中包含的 Winmeta.xml 檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-120">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="6f4e0-121">備註</span><span class="sxs-lookup"><span data-stu-id="6f4e0-121">Remarks</span></span>

<span data-ttu-id="6f4e0-122">**InstrumentationManifest** 元素必須包含下列命名空間：</span><span class="sxs-lookup"><span data-stu-id="6f4e0-122">The **instrumentationManifest** element must contain the following namespaces:</span></span>

<dl> <span data-ttu-id="6f4e0-123">xmlns = " https://schemas.microsoft.com/win/2004/08/events "</span><span class="sxs-lookup"><span data-stu-id="6f4e0-123">xmlns="https://schemas.microsoft.com/win/2004/08/events"</span></span>  
<span data-ttu-id="6f4e0-124">xmlns： win = " https://manifests.microsoft.com/win/2004/08/windows/events "</span><span class="sxs-lookup"><span data-stu-id="6f4e0-124">xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"</span></span>  
<span data-ttu-id="6f4e0-125">xmlns： xs = " https://www.w3.org/2001/XMLSchema "</span><span class="sxs-lookup"><span data-stu-id="6f4e0-125">xmlns:xs="https://www.w3.org/2001/XMLSchema"</span></span>  
</dl>

<span data-ttu-id="6f4e0-126">資訊清單必須包含檢測區段和當地語系化區段。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-126">A manifest must contain an instrumentation section and a localization section.</span></span> <span data-ttu-id="6f4e0-127">檢測區段和中繼資料區段互斥 (您無法在相同的資訊清單) 中定義。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-127">The instrumentation section and metadata section are mutually exclusive (you cannot define both in the same manifest).</span></span> <span data-ttu-id="6f4e0-128">雖然您可以建立包含中繼資料區段的資訊清單，但服務將不會使用它。服務唯一可辨識的中繼資料是 Winmeta.xml 檔案中找到的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-128">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="examples"></a><span data-ttu-id="6f4e0-129">範例</span><span class="sxs-lookup"><span data-stu-id="6f4e0-129">Examples</span></span>

<span data-ttu-id="6f4e0-130">下列範例顯示完整定義之檢測資訊清單的基本架構。</span><span class="sxs-lookup"><span data-stu-id="6f4e0-130">The following example shows the skeleton of a fully defined instrumentation manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a><span data-ttu-id="6f4e0-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f4e0-131">Requirements</span></span>



| <span data-ttu-id="6f4e0-132">需求</span><span class="sxs-lookup"><span data-stu-id="6f4e0-132">Requirement</span></span> | <span data-ttu-id="6f4e0-133">值</span><span class="sxs-lookup"><span data-stu-id="6f4e0-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6f4e0-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f4e0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4e0-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f4e0-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6f4e0-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f4e0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4e0-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f4e0-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





