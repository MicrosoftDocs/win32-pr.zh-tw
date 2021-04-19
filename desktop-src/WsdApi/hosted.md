---
description: 定義服務主機所定義之服務的 ServiceID、類型、PnPXHardwareId 和 PnPXCompatibleId 元素。
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: hosted 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46549898f0a95de362467c759c3d95eb806a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988377"
---
# <a name="hosted-element"></a>hosted 元素

定義服務主機所定義之服務的 [**ServiceID**](serviceid.md)、 [**類型**](types.md)、[**PnPXHardwareId**](pnpxhardwareid.md)和 [**PnPXCompatibleId**](pnpxcompatibleid.md) 元素。

## <a name="usage"></a>使用方式

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                 | 描述                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [**PnPXCompatibleId**](pnpxcompatibleid.md)<br/> | 指定服務的 PnP 相容識別碼。<br/> <br/> |
| [**PnPXHardwareId**](pnpxhardwareid.md)<br/>     | 指定服務的 PnP 硬體識別碼。<br/> <br/>   |
| [**ServiceID**](serviceid.md)<br/>               | 定義服務主機的服務識別碼。<br/> <br/>        |
| [**類型**](types.md)<br/>                       | 定義 XSD 限定名稱的清單。<br/> <br/>                    |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a>父元素



| 元素                                         | 描述                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | 要執行之裝置的裝載中繼資料。<br/> <br/> |



## <a name="remarks"></a>備註

服務主機提供的每個服務都應該有自己的 **託管** 元素資訊，以確保服務在對中繼資料要求的回應中已正確發佈。

[**PnPXHardwareId**](pnpxhardwareid.md)和 [**PnPXCompatibleId**](pnpxcompatibleid.md)元素是選擇性的，但在使用時，必須一起使用。 如果有的話，也必須有另一個。

如果有 [**PnPXDeviceCategory**](pnpxdevicecategory.md) 元素，則 **至少一個裝載** 的元素必須同時包含 [**PnPXHardwareId**](pnpxhardwareid.md) 和 [**PnPXCompatibleId**](pnpxcompatibleid.md) 專案。 同樣地，如果 **PnPXHardwareId** 和 **PnPXCompatibleId** 元素 **存在於裝載的元素中**，則 [**ThisModelMetadata**](thismodelmetadata.md)元素內至少必須有一個 **PnPXDeviceCategory** 元素。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




