---
title: OpcodeType 複雜類型
description: 定義應用程式元件內的作業。
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- OpcodeType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106025"
---
# <a name="opcodetype-complex-type"></a>OpcodeType 複雜類型

定義應用程式元件內的作業。 搭配工作使用，以識別正在記錄事件的應用程式區段。

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱     | 類型                                                              | Description                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Opcode 的當地語系化顯示名稱。 訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。 <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | 已保留供內部使用。<br/>                                                                                                                                                                                                                                                                           |
| NAME     | **QName**                                                         | Opcode 的名稱。 這個名稱在此提供者的範圍內必須是唯一的。 <br/>                                                                                                                                                                                                                      |
| 符號   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中之 opcode 的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，為編譯器產生的標頭檔中的 opcode 建立常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |
| value    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Opcode 值。 您可以指定範圍10和239的值。 如需預先定義之 opcode 值的清單，請參閱備註。<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>備註

以下是您可以使用的預先定義 opcode 值。 這些值是在包含于 Windows SDK 的 Winmeta.xml 檔案中定義。



| Name          | 值 | 符號                      | 描述                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| win： Info      | 0     | NEW-WINEVENT \_ OPCODE \_ 資訊      | 資訊事件。                                                                                |
| win：開始     | 1     | NEW-WINEVENT \_ OPCODE \_ 開始     | 表示啟動活動的事件。                                                         |
| win：停止      | 2     | NEW-WINEVENT 作業 \_ 碼 \_ 停止      | 表示停止活動的事件。 事件對應到最後一個不成對的開始事件。 |
| win： DC \_ 啟動 | 3     | NEW-WINEVENT \_ OPCODE \_ DC \_ 啟動 | 表示開始之資料收集的事件。 這些是取消事件種類。                      |
| win： DC \_ 停止  | 4     | NEW-WINEVENT 作業 \_ 碼 \_ DC \_ 停止  | 表示資料收集停止的事件。 這些是取消事件種類。                      |
| win：擴充功能 | 5     | NEW-WINEVENT \_ OPCODE \_ 延伸模組 | 擴充事件。                                                                                    |
| win：回復     | 6     | NEW-WINEVENT \_ OPCODE \_ 回復     | 回復事件。                                                                                         |
| win： Resume    | 7     | NEW-WINEVENT \_ OPCODE \_ RESUME    | 表示在暫止後繼續之活動的事件。                                   |
| win：暫停   | 8     | NEW-WINEVENT \_ OPCODE \_ 暫止   | 表示暫止的活動暫止另一個活動完成的事件。           |
| win：傳送      | 9     | NEW-WINEVENT \_ OPCODE \_ 傳送      | 表示將活動傳送至另一個元件的事件。                                   |
| win：接收   | 240   | NEW-WINEVENT \_ OPCODE \_ 接收   | 表示接收來自另一個元件之活動傳送的事件。                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





