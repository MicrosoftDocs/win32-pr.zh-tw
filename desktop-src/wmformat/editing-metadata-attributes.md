---
title: 編輯中繼資料屬性
description: 編輯中繼資料屬性
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows媒體格式 SDK，編輯中繼資料屬性
- Advanced Systems Format (ASF) 、編輯中繼資料屬性
- ASF (Advanced Systems Format) 、編輯中繼資料屬性
- 中繼資料，編輯屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973b787b37bbf9333a0adb218ab5db0e6f677521f1bfc9a0cdc1d5c37200e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586058"
---
# <a name="editing-metadata-attributes"></a>編輯中繼資料屬性

編輯中繼資料屬性與設定新屬性非常類似。 請勿使用 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)，而是使用 [**IWMHeaderInfo3：： ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute)。 **ModifyAttribute** 與 **AddAttribute** 相同，不同之處在于您未指定屬性名稱，而且索引編號是輸入參數，而不是輸出。

您可以使用 stream number 0xFFFF 來指定要使用其全域索引來修改的屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




