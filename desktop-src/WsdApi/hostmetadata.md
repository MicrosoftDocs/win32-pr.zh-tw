---
description: 定義要執行之裝置的裝載中繼資料。 此元素僅用於 (主機) 的裝置執行。
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: hostMetadata 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971604"
---
# <a name="hostmetadata-element"></a>hostMetadata 元素

定義要執行之裝置的裝載中繼資料。 此元素僅用於 (主機) 的裝置執行。

## <a name="usage"></a>使用方式

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                             | 描述                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**主機**](host.md)<br/>     | 定義服務主機的 ServiceID 和 [**Types**](types.md) 元素。 如果未明確提供，則 WSDAPI 不會提供任何預設資料來回應中繼資料要求。<br/> <br/>                                                                                                                                          |
| [**託管**](hosted.md)<br/> | 定義此服務主機所提供之服務的 [**ServiceID**](serviceid.md) 和 [**Types**](types.md) 元素。 這項服務主機提供的每個服務都應該有自己的 [**託管**](hosted.md) 元素資訊，以確保服務在對中繼資料要求的回應中已正確發佈。<br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a>父元素



| 元素                                                         | 描述                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | 描述裝置的主機和託管中繼資料。<br/> <br/> |



## <a name="remarks"></a>備註

裝載中繼資料會顯示在此專案中，類似于裝置設定檔中指定的表單。 **hostMetadata** 與裝置設定檔中所述的格式稍有不同，因為它所支援的唯一參考屬性是服務識別碼。

接著會使用 [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) 元素來產生包含這項資訊的 C 常數。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




