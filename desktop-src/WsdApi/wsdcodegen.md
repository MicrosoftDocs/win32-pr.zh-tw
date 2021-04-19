---
description: 這是 WSDAPI 程式碼產生器 XML 腳本檔案的根項目。
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdCodeGen 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999872"
---
# <a name="wsdcodegen-element"></a>wsdCodeGen 元素

這是 WSDAPI 程式碼產生器 XML 腳本檔案的根項目。

## <a name="usage"></a>使用方式

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a>屬性



| 屬性                        | 類型                             | 必要       | 描述                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| **ConfigFileVersion**<br/> | 任何字元字串。<br/> | Yes<br/> | 設定檔案的版本。 唯一有效的值是 "1.0"。<br/> <br/> |



## <a name="child-elements"></a>子元素



| 元素                                                         | 描述                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**autoStatic**](autostatic.md)<br/>                     | 指出 WsdCodeGen 是否應該嘗試自動將某些產生的欄位標記為靜態。 此選項預設為啟用狀態。<br/> <br/>                                                                 |
| [**檔**](file.md)<br/>                                 | 指示程式碼產生器產生檔案。<br/> <br/>                                                                                                                                                       |
| [**hostMetadata**](hostmetadata.md)<br/>                 | 要執行之裝置的裝載中繼資料。 此元素僅用於 (主機) 的裝置執行。<br/> <br/>                                                                                 |
| [**layerNumber**](layernumber.md)<br/>                   | 要產生的程式碼層數目。 在執行時間資料表中，會使用圖層編號來區分另一層程式碼。 WSDAPI 本身會使用產生的程式碼，其層號為0。<br/> <br/> |
| [**layerPrefix**](layerprefix.md)<br/>                   | 要在產生的程式碼中使用的前置詞，以確保產生的符號唯一性。 WSDAPI 使用 "WSD" 前置詞。<br/> <br/>                                                                                     |
| [**宏觀**](macro.md)<br/>                               | 定義 [**include**](include.md) 元素要重複使用的 TEXT 或 CDATA。<br/> <br/>                                                                                                                        |
| [**命名 空間**](namespace.md)<br/>                       | 描述要用於產生程式碼的命名空間。<br/> <br/>                                                                                                                                                |
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | 描述裝置的主機和託管中繼資料。<br/> <br/>                                                                                                                                               |
| [**thisModelMetadata**](thismodelmetadata.md)<br/>       | 要執行之裝置的製造商和型號中繼資料。 此元素僅用於 (主機) 的裝置執行。<br/> <br/>                                                                  |
| [**Wsdl**](wsdl.md)<br/>                                 | 指定要針對合約資訊處理的 WSDL 檔案。<br/> <br/>                                                                                                                                           |
| [**Xsd**](xsd.md)<br/>                                   | 指定要針對合約資訊處理的 XSD 檔案。<br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a>父元素

沒有父元素。

## <a name="remarks"></a>備註

一般情況下 [**，檔案**](file.md) 元素應該會在最後產生，因為它們會產生使用其他元素所指定之資料的程式碼。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




