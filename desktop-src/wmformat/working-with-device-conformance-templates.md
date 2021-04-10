---
title: 使用裝置一致性範本
description: 使用裝置一致性範本
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- 設定檔，裝置一致性範本
- 設定檔，一致性範本
- 編解碼器、裝置一致性範本
- 編解碼器，一致性範本
- 裝置一致性範本，關於
- 一致性範本
- 範本、裝置一致性範本
- Advanced Systems Format (ASF) 、裝置一致性範本
- ASF (Advanced Systems Format) 、裝置一致性範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092536"
---
# <a name="working-with-device-conformance-templates"></a>使用裝置一致性範本

由於 ASF 檔案有很大的彈性，因此通常很難判斷檔案是否適合在特定裝置上播放。 例如，在桌上型電腦上針對本機播放所撰寫的檔案，並不適合用於掌上型裝置。 裝置一致性範本可讓應用程式快速識別檔案預定的播放裝置類型。 如果裝置一致性範本與裝置不符，應用程式可以通知使用者該檔案對裝置而言是不正確的。 如此一來，使用者就能獲得更好的播放體驗。

如果您要以獨佔方式寫入個人電腦上的檔案，則在建立設定檔時，裝置一致性範本將不會有許多因素。 這些範本的主要用途是確保為了與特殊硬體一起使用而建立的檔案，與整個裝置（而不只是單一裝置）相容。

裝置一致性範本是一個判斷提示，表示 ASF 檔案包含在特定參數內編碼的資料。 如需個別範本適用設定的詳細資訊，請參閱 [裝置一致性範本參數](device-conformance-template-parameters.md)。

下列編解碼器支援裝置一致性範本：

-   Windows Media 視訊9
-   Windows Media 音訊9和更新版本
-   Windows Media 音訊 9 Professional 和更新版本
-   Windows Media 音訊9語音

您不需要採取任何特殊步驟就能使用裝置一致性範本。 編解碼器會自動為檔案中的每個適當串流寫入範本字串。 編解碼器會根據設定檔中的串流設定，決定要使用的範本。 裝置一致性範本參數中有一些重迭，因此您可能會想要要求特定的範本，而不是讓編解碼器為您指派一個範本。 您可以 \_ 使用適當串流設定物件的 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) 介面方法來設定 g wszDecoderComplexityRequested 屬性，以指定您想要的範本。

寫入 ASF 檔案時，每個資料流程的實際裝置一致性範本會設定為編解碼器傳遞給寫入器的值。 開啟要讀取的檔案時，您可以使用 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面的方法來取出 g \_ wszDeviceConformanceTemplate 資料流程層級屬性，以找出檔案資料流程符合的範本。 如需屬性的詳細資訊，請參閱 [使用中繼資料](working-with-metadata.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設計設定檔**](designing-profiles.md)
</dt> <dt>

[**裝置一致性範本參數**](device-conformance-template-parameters.md)
</dt> </dl>

 

 




