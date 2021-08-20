---
description: 封裝作者可以壓縮原始程式檔並將它們包含在封包檔中，以縮減其安裝套件的大小。 來源檔案映射可以是壓縮、未壓縮或混合兩種類型。
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: 壓縮和未壓縮的來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7d35a5723261ab1c62866d185a8402a9607600cad906c2fb66ddc5dc85ac08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144449"
---
# <a name="compressed-and-uncompressed-sources"></a>壓縮和未壓縮的來源

封裝作者可以壓縮原始程式檔並將它們 [包含在封包檔](cabinet-files.md)中，以縮減其安裝套件的大小。 來源檔案映射可以是壓縮、未壓縮或混合兩種類型。

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> 壓縮的來源
</dt> <dd>

完全由壓縮檔案組成的來源應該在 [ [**字數統計摘要**](word-count-summary.md) ] 屬性中包含壓縮的旗標位。 壓縮的原始程式檔必須儲存在位於 .msi 檔案內之資料流程內的封包檔中，或位於來源樹狀結構根目錄之個別封包檔中的封包檔中。 來源中的所有封包都必須列在 [媒體資料表](media-table.md)中。

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>未壓縮的來源
</dt> <dd>

完全由未壓縮的原始程式檔組成的來源，應該從 [ [**字數統計摘要**](word-count-summary.md) ] 屬性中省略壓縮的旗標位。 來源中的所有未壓縮檔案都必須存在於 [目錄資料表](directory-table.md)所指定的來源樹狀結構中。

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>混合來源 
</dt> <dd>

若要在相同的封裝中混合壓縮和未壓縮的原始程式檔，請在特定檔案上設定 msidbFileAttributesCompressed 或 msidbFileAttributesNoncompressed 位旗標，以覆寫 [ [**字數統計摘要**](word-count-summary.md) ] 屬性預設值。 如果檔案的壓縮狀態不符合 [[**字數統計摘要**](word-count-summary.md)] 屬性所指定的預設值，則會在 [檔案][資料表](file-table.md)的 [屬性] 資料行中設定這些位旗標。

例如，如果 [ [**字數統計**](word-count-summary.md) ] 屬性已設定壓縮的旗標，則所有檔案都會被視為壓縮成封包。 來源中任何未壓縮的檔案都必須在 [File 資料表](file-table.md)的 [屬性] 資料行中包含 msidbFileAttributesNoncompressed。 未壓縮的檔案必須位於來源樹狀結構的根目錄。

如果 [ [**字數統計摘要**](word-count-summary.md) ] 屬性已設定未壓縮的旗標，則預設會將檔案視為未壓縮，而任何壓縮檔案資料表的 [屬性] 資料行中都必須包含 msidbFileAttributesCompressed。 所有壓縮檔案都必須儲存在位於 .msi 檔案內之資料流程內的封包檔中，或位於來源樹狀結構根目錄之個別封包檔中的封包檔中。

如需詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。

</dd> </dl>

 

 



