---
title: 自訂中繼資料
description: 自訂中繼資料
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows Media Format SDK，自訂中繼資料
- Advanced Systems Format (ASF) 、自訂中繼資料
- ASF (Advanced Systems Format) ，自訂中繼資料
- Windows Media Format SDK，IWMHeaderInfo3 介面
- Advanced Systems Format (ASF) ，IWMHeaderInfo3 介面
- ASF (Advanced Systems Format) ，IWMHeaderInfo3 介面
- 中繼資料，自訂
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "103681539"
---
# <a name="custom-metadata"></a>自訂中繼資料

除了 Windows Media Format SDK 提供的許多支援屬性之外，您還可以建立自己的規格的中繼資料屬性。 建立自訂中繼資料屬性時，您應該使用容易識別的命名慣例，以避免可能與其他人建立的屬性發生衝突。

建議您使用 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 的方法來建立您的中繼資料，因為它們在 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)的方法上提供額外的彈性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**屬性**](attributes.md)
</dt> <dt>

[**中繼資料功能**](metadata-features.md)
</dt> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




