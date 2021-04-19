---
description: 指定裝置所屬的 PnP X 分類。 您可以指定一個以上的類別。
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: PnPXDeviceCategory 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001375"
---
# <a name="pnpxdevicecategory-element"></a>PnPXDeviceCategory 元素

指定裝置所屬的 PnP X 分類。 您可以指定一個以上的類別。

## <a name="usage"></a>使用方式

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                   | 描述                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | 定義要執行之裝置的製造商和型號中繼資料。<br/> <br/> |



## <a name="remarks"></a>備註

裝置也可以指定裝置子類別，以取得更具描述性的裝置類別。 例如，「Microsoft.windowsmobile.forms 攝影機. DigitalStillCamera MediaDevices. MusicPlayer」識別的裝置是具有相機和音樂播放機的 Microsoft Windows Mobile 裝置。 此裝置的主要裝置類別會是「電話」。

若要指定一個以上的裝置類別，請以空格分隔類別。 例如，「印表機存放裝置」會識別主要類別為「印表機」和「儲存體」次要類別的裝置。

如果有 **PnPXDeviceCategory** 元素，則 [**至少一個裝載**](hosted.md) 的元素應該同時包含 [**PnPXHardwareId**](pnpxhardwareid.md) 和 [**PnPXCompatibleId**](pnpxcompatibleid.md) 專案。 同樣地，如果 **PnPXHardwareId** 和 **PnPXCompatibleId** 元素 **存在於裝載的元素中**，則 [**ThisModelMetadata**](thismodelmetadata.md)元素內至少應該有一個 **PnPXDeviceCategory** 元素。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




