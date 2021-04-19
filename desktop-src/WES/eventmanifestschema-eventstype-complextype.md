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
# <a name="eventstype-complex-type"></a>EventsType 複雜類型

包含資訊清單中所定義之提供者的清單。

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

## <a name="child-elements"></a>子元素

| 元素 | 類型 | Description |
|---------|------|-------------|
| message |      | 定義訊息字串。 |
| messageTable | | 定義訊息字串的清單。 除非在下列情況下，您必須定義訊息資料表以明確地將資源編號指派給訊息字串，否則您不應該使用訊息資料表。 <ul><li>您要從郵件內文 ( 的) 檔案遷移至資訊清單，但仍將事件寫入應用程式和系統通道，以便舊版取用者繼續取用事件。 若要進行這項工作，資訊清單中所定義之訊息字串的資源識別碼必須與事件識別碼相同。 但是，訊息編譯器會自動將資源識別碼指派給訊息字串。 若要覆寫編譯器，請使用 message 資料表並將 value 屬性設為事件識別碼，並將 message 屬性設定為在資訊清單的當地語系化區段中，參考字串資料表中的字串。</li><li>如果您想要識別16個以上的提供者，則必須包含第十七個和提供者必須用來為其定義的訊息字串指派資源值的訊息資料表。 如果提供者參考了提供者1到16的訊息字串，則您不會在訊息資料表中包含這些訊息字串。</li></ul>|
| [**供應商**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | 您要定義的提供者清單。 |

## <a name="attributes"></a>屬性

| 名稱    | 類型                                                             | Description                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | 字串資料表中當地語系化字串的參考。                               |
| mid     | xs:string                                                        | 未使用。                                                                              |
| 符號  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 您希望訊息編譯器為此訊息字串建立的符號名稱。|
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | 要用來做為此訊息之訊息識別碼的數位。                          |


## <a name="remarks"></a>備註

您可以在資訊清單中定義之提供者數目的實際限制為16個提供者。 如果您指定16個以上的提供者，則必須使用 message table 明確地將資源編號指派給提供者所參考的訊息字串。 如需詳細資訊，請參閱上述的 message 元素。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|-------------------------------------------|
| 最低支援的用戶端 | \[僅限 Windows Vista 桌面應用程式\]       |
| 最低支援的伺服器 | 僅限 Windows Server 2008 \[ desktop 應用程式\] |
