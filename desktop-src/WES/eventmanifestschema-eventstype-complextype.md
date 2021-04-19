---
title: EventsType 複雜類型
description: 包含資訊清單中所定義之提供者的清單。 |EventsType 複雜類型
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventsType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991420"
---
# <a name="eventstype-complex-type"></a><span data-ttu-id="d1606-105">EventsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="d1606-105">EventsType Complex Type</span></span>

<span data-ttu-id="d1606-106">包含資訊清單中所定義之提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="d1606-106">Contains a list of providers that are defined in the manifest.</span></span>

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
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

## <a name="child-elements"></a><span data-ttu-id="d1606-107">子元素</span><span class="sxs-lookup"><span data-stu-id="d1606-107">Child elements</span></span>

| <span data-ttu-id="d1606-108">元素</span><span class="sxs-lookup"><span data-stu-id="d1606-108">Element</span></span> | <span data-ttu-id="d1606-109">類型</span><span class="sxs-lookup"><span data-stu-id="d1606-109">Type</span></span> | <span data-ttu-id="d1606-110">Description</span><span class="sxs-lookup"><span data-stu-id="d1606-110">Description</span></span> |
|---------|------|-------------|
| <span data-ttu-id="d1606-111">message</span><span class="sxs-lookup"><span data-stu-id="d1606-111">message</span></span> |      | <span data-ttu-id="d1606-112">定義訊息字串。</span><span class="sxs-lookup"><span data-stu-id="d1606-112">Defines a message string.</span></span> |
| <span data-ttu-id="d1606-113">messageTable</span><span class="sxs-lookup"><span data-stu-id="d1606-113">messageTable</span></span> | | <span data-ttu-id="d1606-114">定義訊息字串的清單。</span><span class="sxs-lookup"><span data-stu-id="d1606-114">Defines a list of message strings.</span></span> <span data-ttu-id="d1606-115">除非在下列情況下，您必須定義訊息資料表以明確地將資源編號指派給訊息字串，否則您不應該使用訊息資料表。</span><span class="sxs-lookup"><span data-stu-id="d1606-115">You should not have to use a message table except in the following cases where you must define a message table to explicitly assign resource numbers to message strings.</span></span> <ul><li><span data-ttu-id="d1606-116">您要從郵件內文 ( 的) 檔案遷移至資訊清單，但仍將事件寫入應用程式和系統通道，以便舊版取用者繼續取用事件。</span><span class="sxs-lookup"><span data-stu-id="d1606-116">You are migrating from a message text (.mc) file to a manifest but are still writing events to the application and system channels, so that legacy consumers to continue consuming the events.</span></span> <span data-ttu-id="d1606-117">若要進行這項工作，資訊清單中所定義之訊息字串的資源識別碼必須與事件識別碼相同。</span><span class="sxs-lookup"><span data-stu-id="d1606-117">To make this work, the resource identifiers for the message strings defined in the manifest must be the same as the event identifiers.</span></span> <span data-ttu-id="d1606-118">但是，訊息編譯器會自動將資源識別碼指派給訊息字串。</span><span class="sxs-lookup"><span data-stu-id="d1606-118">However, the message compiler automatically assigns resource identifiers to the message strings.</span></span> <span data-ttu-id="d1606-119">若要覆寫編譯器，請使用 message 資料表並將 value 屬性設為事件識別碼，並將 message 屬性設定為在資訊清單的當地語系化區段中，參考字串資料表中的字串。</span><span class="sxs-lookup"><span data-stu-id="d1606-119">To override the compiler, use the message table and set the value attribute to the event identifier and the message attribute to refer to a string in the string table in the localization section of the manifest.</span></span></li><li><span data-ttu-id="d1606-120">如果您想要識別16個以上的提供者，則必須包含第十七個和提供者必須用來為其定義的訊息字串指派資源值的訊息資料表。</span><span class="sxs-lookup"><span data-stu-id="d1606-120">If you want to identify more than 16 providers, you must include the message table that the seventeenth and on providers must use to assign resource values for the message strings that they define.</span></span> <span data-ttu-id="d1606-121">如果提供者參考了提供者1到16的訊息字串，則您不會在訊息資料表中包含這些訊息字串。</span><span class="sxs-lookup"><span data-stu-id="d1606-121">If the provider references message strings that providers 1 through 16 defined, you do not include those message strings in the message table.</span></span></li></ul>|
| [<span data-ttu-id="d1606-122">**供應商**</span><span class="sxs-lookup"><span data-stu-id="d1606-122">**provider**</span></span>](eventmanifestschema-provider-eventstype-element.md) | [<span data-ttu-id="d1606-123">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="d1606-123">**ProviderType**</span></span>](eventmanifestschema-providertype-complextype.md) | <span data-ttu-id="d1606-124">您要定義的提供者清單。</span><span class="sxs-lookup"><span data-stu-id="d1606-124">A list of providers that you want to define.</span></span> |

## <a name="attributes"></a><span data-ttu-id="d1606-125">屬性</span><span class="sxs-lookup"><span data-stu-id="d1606-125">Attributes</span></span>

| <span data-ttu-id="d1606-126">名稱</span><span class="sxs-lookup"><span data-stu-id="d1606-126">Name</span></span>    | <span data-ttu-id="d1606-127">類型</span><span class="sxs-lookup"><span data-stu-id="d1606-127">Type</span></span>                                                             | <span data-ttu-id="d1606-128">Description</span><span class="sxs-lookup"><span data-stu-id="d1606-128">Description</span></span>                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1606-129">message</span><span class="sxs-lookup"><span data-stu-id="d1606-129">message</span></span> | [<span data-ttu-id="d1606-130">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="d1606-130">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="d1606-131">字串資料表中當地語系化字串的參考。</span><span class="sxs-lookup"><span data-stu-id="d1606-131">A reference to the localized string in the string table.</span></span>                               |
| <span data-ttu-id="d1606-132">mid</span><span class="sxs-lookup"><span data-stu-id="d1606-132">mid</span></span>     | <span data-ttu-id="d1606-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1606-133">xs:string</span></span>                                                        | <span data-ttu-id="d1606-134">未使用。</span><span class="sxs-lookup"><span data-stu-id="d1606-134">Not used.</span></span>                                                                              |
| <span data-ttu-id="d1606-135">符號</span><span class="sxs-lookup"><span data-stu-id="d1606-135">symbol</span></span>  | [<span data-ttu-id="d1606-136">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="d1606-136">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="d1606-137">您希望訊息編譯器為此訊息字串建立的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="d1606-137">The symbolic name that you want the message compiler to create for this message string.</span></span>|
| <span data-ttu-id="d1606-138">value</span><span class="sxs-lookup"><span data-stu-id="d1606-138">value</span></span>   | [<span data-ttu-id="d1606-139">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="d1606-139">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="d1606-140">要用來做為此訊息之訊息識別碼的數位。</span><span class="sxs-lookup"><span data-stu-id="d1606-140">The number to use as the message identifier for this message.</span></span>                          |


## <a name="remarks"></a><span data-ttu-id="d1606-141">備註</span><span class="sxs-lookup"><span data-stu-id="d1606-141">Remarks</span></span>

<span data-ttu-id="d1606-142">您可以在資訊清單中定義之提供者數目的實際限制為16個提供者。</span><span class="sxs-lookup"><span data-stu-id="d1606-142">The practical limit of the number of providers that you can define in a manifest is 16 providers.</span></span> <span data-ttu-id="d1606-143">如果您指定16個以上的提供者，則必須使用 message table 明確地將資源編號指派給提供者所參考的訊息字串。</span><span class="sxs-lookup"><span data-stu-id="d1606-143">If you specify more than 16 providers, you must use a message table to explicitly assign resource numbers to the message strings that the provider references.</span></span> <span data-ttu-id="d1606-144">如需詳細資訊，請參閱上述的 message 元素。</span><span class="sxs-lookup"><span data-stu-id="d1606-144">For more details, see the message element above.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1606-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1606-145">Requirements</span></span>

| <span data-ttu-id="d1606-146">需求</span><span class="sxs-lookup"><span data-stu-id="d1606-146">Requirement</span></span> | <span data-ttu-id="d1606-147">值</span><span class="sxs-lookup"><span data-stu-id="d1606-147">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="d1606-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1606-148">Minimum supported client</span></span> | <span data-ttu-id="d1606-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1606-149">Windows Vista \[desktop apps only\]</span></span>       |
| <span data-ttu-id="d1606-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1606-150">Minimum supported server</span></span> | <span data-ttu-id="d1606-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1606-151">Windows Server 2008 \[desktop apps only\]</span></span> |
