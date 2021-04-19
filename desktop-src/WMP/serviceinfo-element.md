---
title: ServiceInfo 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 ServiceInfo 元素是 ServiceInfo.xml 檔的主要元素。
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- ServiceInfo 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989605"
---
# <a name="serviceinfo-element"></a>ServiceInfo 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**ServiceInfo** 元素是 ServiceInfo.xml 檔的主要元素。

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a>屬性



| 詞彙                                                                                                                                             | 描述                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**版本** (選用) <br/> | ServiceInfo.xml 檔的版本。 Windows Media Player 支援1.00 版。<br/>                                                                                                                                                            |
| <span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>需要 (**金鑰**) <br/>                 | 可唯一識別線上商店的服務金鑰字串。<br/>                                                                                                                                                                                   |
| <span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**<br/>                 | 指出線上商店是否為類型1存放區。 值為 "true" 表示存放區為類型1存放區。 值為 "false" 表示存放區不是類型1存放區;也就是說，它是類型2存放區。 預設值為 "false"。<br/> |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 父元素 | 無                                                                                                                                                                               |
| 子元素  | **AlbumInfo**、 **BuyCD**、 **Color**、 **Description**、 **FriendlyName**、 **HTMLView**、 **Image**、 **資訊中心**、 **Install**、 **ServiceTask1**、 **ServiceTask2**、 **ServiceTask3** |



 

## <a name="remarks"></a>備註

下表詳細說明以 URL 要求傳送的參數。 其他可能存在於舊版相容性的用途。 要求也會包含您使用 Windows Media Player 安裝程式的 ServiceExtra 命令列參數指定的任何參數。



| Name         | 值                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *大地 水準面*      | Windows 地理位置識別碼。 在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。 |
| *locale*     | Windows Media Player 地區設定識別碼。                                                                                                                                     |
| *userlocale* | Windows 地區設定識別碼。 地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。        |
| *version*    | 使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





