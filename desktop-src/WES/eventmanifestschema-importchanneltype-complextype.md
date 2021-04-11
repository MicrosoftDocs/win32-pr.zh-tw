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
# <a name="importchanneltype-complex-type"></a>ImportChannelType 複雜類型

識別已由另一個提供者定義或包含中繼資料區段之資訊清單中的通道。

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

## <a name="attributes"></a>屬性



| 名稱   | 類型                                                              | Description                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 子   | token                                                             | 此識別碼可唯一識別提供者所定義或匯入通道清單中的通道。 在事件定義中參考此通道時，請使用此值。 如果您未指定通道識別碼，請使用通道的名稱在事件定義中參考這個通道。<br/>  |
| NAME   | anyURI                                                            | 要匯入的通道名稱。<br/>                                                                                                                                                                                                                                                                          |
| 符號 | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中通道的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立通道的常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |



## <a name="remarks"></a>備註

您必須先安裝定義匯入通道的資訊清單，才能讓您的提供者寫入事件;否則，無法將事件寫入至通道， (寫入作業成功時，事件就不會寫入通道) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





