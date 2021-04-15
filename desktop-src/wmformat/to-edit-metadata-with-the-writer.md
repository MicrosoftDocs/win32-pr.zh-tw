---
title: 使用寫入器編輯中繼資料
description: 使用寫入器編輯中繼資料
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media Format SDK，使用寫入器編輯中繼資料
- Windows Media Format SDK，中繼資料編輯
- Advanced Systems Format (ASF) ，使用寫入器編輯中繼資料
- ASF (Advanced Systems Format) ，使用寫入器編輯中繼資料
- Advanced Systems Format (ASF) ，中繼資料編輯
- ASF (Advanced Systems Format) ，中繼資料編輯
- 中繼資料，使用寫入器編輯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374809"
---
# <a name="to-edit-metadata-with-the-writer"></a>使用寫入器編輯中繼資料

您可以直接從寫入器存取將會進入檔案標頭的中繼資料。 呼叫 writer 物件中任何介面的 **QueryInterface** 方法，以取得 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 或 [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) 介面的指標。 當您有適當介面的指標之後，您就可以操控中繼資料，就像您在中繼資料編輯器物件中載入檔案一樣。 如需有關編輯中繼資料的詳細資訊，請參閱 [使用中繼資料](working-with-metadata.md)。

您必須在呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)之前，對中繼資料進行所有變更。

> [!Note]  
> 如果您設定檔案的中繼資料、寫入檔案，然後準備在不釋放寫入器的情況下寫入新檔案，則某些針對第一個檔案設定的中繼資料仍會保持設定，並且會包含在後續的檔案中。 使用相同的寫入器物件實例來撰寫多個檔案時，您有兩個選項：在寫入每個檔案之前檢查所有中繼資料，或只寫入寫入器中繼資料，以套用至您所撰寫的所有檔案。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




