---
description: 修補具有變數內容的檔案時，可能需要保留目標檔案的選取區域，以避免遺失重要資訊。
ms.assetid: 4a610588-556e-489f-ac14-73e5e6b776fe
title: 修補選取的檔案區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778df4b0cc98eeacd1106929b18c7461c6fa9e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974109"
---
# <a name="patching-selected-regions-of-a-file"></a>修補選取的檔案區域

修補具有變數內容的檔案時，可能需要保留目標檔案的選取區域，以避免遺失重要資訊。 例如，有些應用程式會將使用者資訊標記為可執行檔。 由於目標檔案的內容可能取決於安裝應用程式的電腦，因此很難判斷特定檔案是否為修補程式的有效目標。 寫入至目標檔案的使用者資訊也可以透過修補程式來覆寫。

當您產生 patch 建立屬性 (使用 [Msimsp.exe](msimsp-exe.md) 和 [PATCHWIZ.DLL](patchwiz-dll.md)PCP) 檔案時，可以指定在修補期間忽略目標檔案特定區域中的資訊。 您也可以指定目標檔案的其他區域中的資訊保留並複製到已更新檔案中的位移位置。 您可以指定要忽略的目標檔案區域，以及撰寫 [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md)、 [ExternalFiles](externalfiles-table-patchwiz-dll-.md)和 [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) 資料表時要保留的區域。

使用 [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) 資料表的 RetainOffsets 資料行以及 [RetainLengths](familyfileranges-table-patchwiz-dll-.md) 資料表的 RetainOffsets 和 FamilyFileRanges 資料行，將目標檔案中的資訊範圍複製到已更新檔案中的位移範圍。 此範圍中的資訊會保留下來。 使用 FamilyFileRanges 資料表的 RetainLengths 資料行，指定範圍的長度。 保留範圍的長度在目標和更新的檔案中是相同的。 使用 TargetFiles OptionalData 資料表的 RetainOffsets 資料行，在目標檔案中指定範圍的位移。 使用 FamilyFileRanges 資料表的 RetainOffsets 資料行，在更新的檔案中指定範圍的位移。 因此，保留的目標檔案範圍是 TargetFiles OptionalData 資料表中 RetainOffsets 的值加上 RetainLengths。 這項資訊會複製到 FamilyFileRanges 資料表中 RetainOffsets 值所提供之範圍內的更新檔案，加上 RetainLengths。 您可以指定多個範圍，但是長度的順序必須符合位移的順序。

使用 [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) 資料表來忽略目標檔案的範圍。 修補程式仍可覆寫這個目標檔範圍內的資訊。 在 [IgnoreOffsets] 資料行中指定範圍的位移，並在 [IgnoreLengths] 資料行中指定其長度。 您可以指定多個範圍，但是長度的順序必須符合位移的順序。

[長度] 和 [位移] 資料行中的值可以是十進位或十六進位。 [PATCHWIZ.DLL](patchwiz-dll.md) 將值視為十六進位（如果前面加上 "0x"）。 這些資料行是字串資料行，所以 PATCHWIZ.DLL 將值轉換為 Ulong。 Length 資料行指定長度（以位元組為單位）。

 

 



