---
title: 設定中繼資料屬性
description: 設定中繼資料屬性
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media 格式 SDK，設定中繼資料屬性
- Advanced Systems Format (ASF) ，設定中繼資料屬性
- ASF (Advanced Systems Format) ，設定中繼資料屬性
- 中繼資料，設定屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374526"
---
# <a name="setting-metadata-attributes"></a>設定中繼資料屬性

中繼資料屬性是使用 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) 方法所設定。

所有屬性都是從檔案的語言清單中指派語言。 您可以使用 [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) 介面來存取語言清單。 若要取得 **IWMLanguageList** 介面的指標，請在您取得 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)之物件的任何介面上呼叫 **QueryInterface** 。

您可以使用任何想要的名稱來新增屬性。 不過，使用 Windows Media 格式 SDK 所支援之非標準名稱的屬性名稱，可能會讓使用者難以探索您的中繼資料。 大部分的媒體播放應用程式都會檢查標準值。 如需詳細資訊，請參閱 [自訂中繼資料](custom-metadata.md)。

您無法使用 stream number 0xFFFF 來全域加入屬性。 您必須將每個屬性指派給特定的資料流程號碼，或指派給檔案層級屬性的資料流程0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




