---
description: 尋找音訊編碼器輸出類型
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: '尋找音訊編碼器輸出類型 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80dd5aa5204887472e08c6ec5ff375a99b8788924ed0848764cde9ba4b5b97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061570"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>尋找音訊編碼器輸出類型 (Microsoft 媒體基礎) 

因為您必須使用音訊編碼器所列舉的音訊編碼器輸出格式，所以您需要尋找最適合您需求的格式。 您所選擇之輸出的通道數目、每個樣本位數，以及所選輸出的取樣率必須符合您壓縮之內容的值。 不過，編碼器可能會支援這些條件約束中的數種類型。

選擇類型的決定因素是編碼資料流程的位元速率。您想要尋找符合輸入的媒體類型，並具有比目標值更接近的位元速率。 如果您要列舉一次執行的 VBR 輸出類型，它是決定您所使用類型的品質值。 如需有關列舉輸出型別中之品質值的詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。

> [!Note]  
>    音訊編碼器以幾乎所有方式列舉其他類型的部分類型。 這些重複的格式存在，其中每秒的封包數不符合在與影片同步時，ASF 檔案中儲存的需求。 在 ASF 檔案中與影片同步處理的音訊，每秒必須有3個或更多的封包，而且位元速率小於32000，每秒5個或更多個封包的位元速率大於或等於32000。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定音訊編碼](configuringaudioencoding.md)
</dt> <dt>

[列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



