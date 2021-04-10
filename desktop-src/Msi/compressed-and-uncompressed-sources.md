---
description: 封裝作者可以壓縮原始程式檔並將它們包含在封包檔中，以縮減其安裝套件的大小。 來源檔案映射可以是壓縮、未壓縮或混合兩種類型。
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: 壓縮和未壓縮的來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dc706a73d52f1dac35c917bd6c178a543ab300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943672"
---
# <a name="compressed-and-uncompressed-sources"></a><span data-ttu-id="11dfd-104">壓縮和未壓縮的來源</span><span class="sxs-lookup"><span data-stu-id="11dfd-104">Compressed and Uncompressed Sources</span></span>

<span data-ttu-id="11dfd-105">封裝作者可以壓縮原始程式檔並將它們 [包含在封包檔](cabinet-files.md)中，以縮減其安裝套件的大小。</span><span class="sxs-lookup"><span data-stu-id="11dfd-105">Package authors can reduce the size of their installation packages by compressing the source files and including them in [cabinet files](cabinet-files.md).</span></span> <span data-ttu-id="11dfd-106">來源檔案映射可以是壓縮、未壓縮或混合兩種類型。</span><span class="sxs-lookup"><span data-stu-id="11dfd-106">The source file image can be compressed, uncompressed, or a mixture of both types.</span></span>

<dl> <dt>

<span data-ttu-id="11dfd-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> 壓縮的來源</span><span class="sxs-lookup"><span data-stu-id="11dfd-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Compressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="11dfd-108">完全由壓縮檔案組成的來源應該在 [ [**字數統計摘要**](word-count-summary.md) ] 屬性中包含壓縮的旗標位。</span><span class="sxs-lookup"><span data-stu-id="11dfd-108">A source consisting entirely of compressed files should include the compressed flag bit in the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="11dfd-109">壓縮的原始程式檔必須儲存在位於 .msi 檔案的資料流程內的封包檔中，或儲存在來源樹狀結構根目錄中的另一個封包檔中。</span><span class="sxs-lookup"><span data-stu-id="11dfd-109">The compressed source files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span> <span data-ttu-id="11dfd-110">來源中的所有封包都必須列在 [媒體資料表](media-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="11dfd-110">All of the cabinets in the source must be listed in the [Media table](media-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="11dfd-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>未壓縮的來源</span><span class="sxs-lookup"><span data-stu-id="11dfd-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Uncompressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="11dfd-112">完全由未壓縮的原始程式檔組成的來源，應該從 [ [**字數統計摘要**](word-count-summary.md) ] 屬性中省略壓縮的旗標位。</span><span class="sxs-lookup"><span data-stu-id="11dfd-112">A source consisting entirely of uncompressed source files should omit the compressed flag bit from the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="11dfd-113">來源中的所有未壓縮檔案都必須存在於 [目錄資料表](directory-table.md)所指定的來源樹狀結構中。</span><span class="sxs-lookup"><span data-stu-id="11dfd-113">All of the uncompressed files in the source must exist in the source tree specified by the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="11dfd-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>混合來源</span><span class="sxs-lookup"><span data-stu-id="11dfd-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Mixed Sources</span></span> 
</dt> <dd>

<span data-ttu-id="11dfd-115">若要在相同的封裝中混合壓縮和未壓縮的原始程式檔，請在特定檔案上設定 msidbFileAttributesCompressed 或 msidbFileAttributesNoncompressed 位旗標，以覆寫 [ [**字數統計摘要**](word-count-summary.md) ] 屬性預設值。</span><span class="sxs-lookup"><span data-stu-id="11dfd-115">To mix compressed and uncompressed source files in the same package, override the [**Word Count Summary**](word-count-summary.md) property default by setting the msidbFileAttributesCompressed or msidbFileAttributesNoncompressed bit flags on particular files.</span></span> <span data-ttu-id="11dfd-116">如果檔案的壓縮狀態不符合 [[**字數統計摘要**](word-count-summary.md)] 屬性所指定的預設值，則會在 [檔案][資料表](file-table.md)的 [屬性] 資料行中設定這些位旗標。</span><span class="sxs-lookup"><span data-stu-id="11dfd-116">These bit flags are set in the Attributes column of the [File table](file-table.md) if the compression state of the file does not match the default specified by the [**Word Count Summary**](word-count-summary.md) property.</span></span>

<span data-ttu-id="11dfd-117">例如，如果 [ [**字數統計**](word-count-summary.md) ] 屬性已設定壓縮的旗標，則所有檔案都會被視為壓縮成封包。</span><span class="sxs-lookup"><span data-stu-id="11dfd-117">For example, if the [**Word Count Summary**](word-count-summary.md) property has the compressed flag bit set, all files are treated as compressed into a cabinet.</span></span> <span data-ttu-id="11dfd-118">來源中任何未壓縮的檔案都必須在 [File 資料表](file-table.md)的 [屬性] 資料行中包含 msidbFileAttributesNoncompressed。</span><span class="sxs-lookup"><span data-stu-id="11dfd-118">Any uncompressed files in the source must include msidbFileAttributesNoncompressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="11dfd-119">未壓縮的檔案必須位於來源樹狀結構的根目錄。</span><span class="sxs-lookup"><span data-stu-id="11dfd-119">The uncompressed files must be located at the root of the source tree.</span></span>

<span data-ttu-id="11dfd-120">如果 [ [**字數統計摘要**](word-count-summary.md) ] 屬性已設定未壓縮的旗標，則預設會將檔案視為未壓縮，而任何壓縮檔案資料表的 [屬性] 資料行中都必須包含 msidbFileAttributesCompressed。</span><span class="sxs-lookup"><span data-stu-id="11dfd-120">If the [**Word Count Summary**](word-count-summary.md) property has the uncompressed flag set, files are treated as uncompressed by default and any compressed files must include msidbFileAttributesCompressed in the Attributes column of the File table.</span></span> <span data-ttu-id="11dfd-121">所有的壓縮檔案都必須儲存在位於 .msi 檔案的資料流程內的封包檔中，或位於來源樹狀結構根目錄之個別的封包檔中。</span><span class="sxs-lookup"><span data-stu-id="11dfd-121">All of the compressed files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span>

<span data-ttu-id="11dfd-122">如需詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="11dfd-122">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

</dd> </dl>

 

 



