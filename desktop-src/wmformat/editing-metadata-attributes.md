---
title: 編輯中繼資料屬性
description: 編輯中繼資料屬性
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media Format SDK，編輯中繼資料屬性
- Advanced Systems Format (ASF) 、編輯中繼資料屬性
- ASF (Advanced Systems Format) 、編輯中繼資料屬性
- 中繼資料，編輯屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374543"
---
# <a name="editing-metadata-attributes"></a>編輯中繼資料屬性

編輯中繼資料屬性與設定新屬性非常類似。 請勿使用 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)，而是使用 [**IWMHeaderInfo3：： ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute)。 **ModifyAttribute** 與 **AddAttribute** 相同，不同之處在于您未指定屬性名稱，而且索引編號是輸入參數，而不是輸出。

您可以使用 stream number 0xFFFF 來指定要使用其全域索引來修改的屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




