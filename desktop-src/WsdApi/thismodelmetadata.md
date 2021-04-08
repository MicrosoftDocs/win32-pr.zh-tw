---
description: 定義要執行之裝置的製造商和型號中繼資料。 此元素僅用於 (主機) 的裝置執行。
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: thisModelMetadata 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851484"
---
# <a name="thismodelmetadata-element"></a>thisModelMetadata 元素

定義要執行之裝置的製造商和型號中繼資料。 此元素僅用於 (主機) 的裝置執行。

## <a name="usage"></a>使用方式

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                     | 描述                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**製造商**](manufacturer.md)<br/>             | 製造商的名稱。 中繼資料中至少必須有一個 [**製造商**](manufacturer.md) 或 [**manufacturerLS**](manufacturerls.md) 。<br/> <br/> |
| [**manufacturerLS**](manufacturerls.md)<br/>         | 製造商名稱的當地語系化版本。<br/> <br/>                                                                                                                 |
| [**manufacturerURL**](manufacturerurl.md)<br/>       | 製造商 URL 位址。<br/> <br/>                                                                                                                                   |
| [**modelName**](modelname.md)<br/>                   | 裝置的名稱。 中繼資料中至少必須有一個 [**modelName**](modelname.md) 或 [**modelNameLS**](modelnamels.md) 。<br/> <br/>                   |
| [**modelNameLS**](modelnamels.md)<br/>               | 裝置名稱的當地語系化版本。<br/> <br/>                                                                                                                       |
| [**modelNumber**](modelnumber.md)<br/>               | 裝置的型號。<br/> <br/>                                                                                                                                 |
| [**modelURL**](modelurl.md)<br/>                     | 裝置型號的 URL 位址。<br/> <br/>                                                                                                                           |
| [**PnPXDeviceCategory**](pnpxdevicecategory.md)<br/> | 裝置所屬的 PnP-X 類別。 <br/> <br/>                                                                                                                |
| [**presentationURL**](presentationurl.md)<br/>       | 裝置型號呈現資料的 URL 位址。<br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

製造商中繼資料符合裝置設定檔中所述的製造商中繼資料區段 (如需詳細資訊，請參閱裝置設定檔) 。 必須提供製造商名稱或至少一個當地語系化版本的製造商名稱。 必須提供模型名稱或至少一個當地語系化版本的模型名稱。

接著會使用 [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) 元素來產生包含這項資訊的 C 常數。

如果有 [**PnPXDeviceCategory**](pnpxdevicecategory.md) 元素，則 [**至少一個裝載**](hosted.md) 的元素必須同時包含 [**PnPXHardwareId**](pnpxhardwareid.md) 和 [**PnPXCompatibleId**](pnpxcompatibleid.md) 專案。 同樣地，如果 **PnPXHardwareId** 和 **PnPXCompatibleId** 元素 **存在於裝載的元素中**，則 **thisModelMetadata** 元素內必須有 **PnPXDeviceCategory** 元素。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




