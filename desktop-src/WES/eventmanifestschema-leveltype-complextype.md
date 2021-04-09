---
title: LevelType 複雜類型
description: 定義嚴重性值，判斷所記錄事件的詳細程度。
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- LevelType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093883"
---
# <a name="leveltype-complex-type"></a>LevelType 複雜類型

定義嚴重性值，判斷所記錄事件的詳細程度。

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
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
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱    | 類型                                                              | Description                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | 層級的當地語系化顯示名稱。 訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。 <br/>                                                                                                    |
| NAME    | **QName**                                                         | 要指派給這個層級的名稱。 這個名稱在提供者的範圍內必須是唯一的。<br/>                                                                                                                                                                                                            |
| 符號  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中之層級的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立層級的常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | 層級值。 您可以指定範圍16到255之間的值。 如需預先定義的層級值，請參閱備註。<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>備註

以下是您可以使用的預先定義層級值。 這些值是在包含于 Windows SDK 的 Winmeta.xml 檔案中定義。



| Name              | 值 | 符號                    | 描述                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | NEW-WINEVENT \_ 層級 \_ 重大 | 識別異常離開或終止事件。<br/>            |
| win:Error         | 2     | NEW-WINEVENT \_ 層級 \_ 錯誤    | 識別嚴重的錯誤事件。<br/>                             |
| win:Warning       | 3     | NEW-WINEVENT \_ 層級 \_ 警告  | 識別如配置失敗的警告事件。<br/>    |
| win:Informational | 4     | NEW-WINEVENT \_ 層級 \_ 資訊     | 識別非錯誤事件，例如進入或離開事件。<br/> |
| win:Verbose       | 5     | NEW-WINEVENT \_ 層級 \_ 詳細資訊  | 識別詳細的追蹤事件。<br/>                           |



 

較高的數位表示您也可以取得較低的層級。 例如，如果您指定「win：警告」，則會收到所有警告、錯誤和重大事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





