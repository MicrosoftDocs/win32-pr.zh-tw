---
title: 設定中繼資料屬性
description: 設定中繼資料屬性
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows媒體格式 SDK，設定中繼資料屬性
- Advanced Systems Format (ASF) ，設定中繼資料屬性
- ASF (Advanced Systems Format) ，設定中繼資料屬性
- 中繼資料，設定屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa352a83e758b97bde6088377f8461a62b2d5071314d45f4978035bec219a5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197508"
---
# <a name="setting-metadata-attributes"></a>設定中繼資料屬性

中繼資料屬性是使用 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) 方法所設定。

所有屬性都是從檔案的語言清單中指派語言。 您可以使用 [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) 介面來存取語言清單。 若要取得 **IWMLanguageList** 介面的指標，請在您取得 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)之物件的任何介面上呼叫 **QueryInterface** 。

您可以使用任何想要的名稱來新增屬性。 不過，使用 Windows 媒體格式 SDK 所支援之非標準名稱的屬性名稱，可能會讓使用者難以探索您的中繼資料。 大部分的媒體播放應用程式都會檢查標準值。 如需詳細資訊，請參閱 [自訂中繼資料](custom-metadata.md)。

您無法使用 stream number 0xFFFF 來全域加入屬性。 您必須將每個屬性指派給特定的資料流程號碼，或指派給檔案層級屬性的資料流程0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




