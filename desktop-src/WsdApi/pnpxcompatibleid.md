---
description: 指定服務的 PnP 相容識別碼。 裝置可能會有一個以上的相容識別碼。
ms.assetid: 25f3d06e-460c-4338-b05d-a6d2c10c2a12
title: PnPXCompatibleId 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4a02191e2186926e5f26e5609aec82ff87f851f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996635"
---
# <a name="pnpxcompatibleid-element"></a>PnPXCompatibleId 元素

指定服務的 PnP 相容識別碼。 裝置可能會有一個以上的相容識別碼。

## <a name="usage"></a>使用方式

``` syntax
<PnPXCompatibleId/>
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

若要指定一個以上的 CompatibleID，請使用空白字元分隔識別碼，例如 "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX SampleService1 \_ \_ HWID \_ 3"。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




