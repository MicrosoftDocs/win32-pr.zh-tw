---
description: 指定服務的 PnP 硬體識別碼。
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: PnPXHardwareId 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996525"
---
# <a name="pnpxhardwareid-element"></a>PnPXHardwareId 元素

指定服務的 PnP 硬體識別碼。 PnP 符合此元素，並在裝置的 INF 檔案的 PnpxDevice 區段中提供硬體描述 (s) \[ \] 。 根據此資訊，PnP 服務會選取並載入最適當的設備磁碟機。

## <a name="usage"></a>使用方式

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                             | 描述                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [**託管**](hosted.md)<br/> | 定義服務主機所定義之服務的元素。 <br/> <br/> |



## <a name="remarks"></a>備註

若要指定一個以上的硬體識別碼，請以空白字元分隔識別碼，例如 "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3"。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




