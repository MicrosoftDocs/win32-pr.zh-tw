---
description: 本節包含描述 Windows 影像處理元件 (WIC) 中繼資料系統的概念主題。
ms.assetid: 68f08f5a-eec6-4484-b901-dbe96c443a0d
title: 處理影像中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475294acb6c5f6836409938fbaedf22306181f08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027108"
---
# <a name="processing-image-metadata"></a><span data-ttu-id="1e7f7-103">處理影像中繼資料</span><span class="sxs-lookup"><span data-stu-id="1e7f7-103">Processing Image Metadata</span></span>

<span data-ttu-id="1e7f7-104">本節包含描述 Windows 影像處理元件 (WIC) 中繼資料系統的概念主題。</span><span class="sxs-lookup"><span data-stu-id="1e7f7-104">This section contains conceptual topics that describe the Windows Imaging Component (WIC) metadata system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1e7f7-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="1e7f7-105">In this section</span></span>



| <span data-ttu-id="1e7f7-106">主題</span><span class="sxs-lookup"><span data-stu-id="1e7f7-106">Topic</span></span>                                                                                              | <span data-ttu-id="1e7f7-107">描述</span><span class="sxs-lookup"><span data-stu-id="1e7f7-107">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e7f7-108">WIC 中繼資料總覽</span><span class="sxs-lookup"><span data-stu-id="1e7f7-108">WIC Metadata Overview</span></span>](-wic-about-metadata.md)<br/>                                        | <span data-ttu-id="1e7f7-109">本主題介紹 WIC 提供的映射中繼資料支援。</span><span class="sxs-lookup"><span data-stu-id="1e7f7-109">This topic introduces the imaging metadata support provided by the WIC.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="1e7f7-110">中繼資料查詢語言總覽</span><span class="sxs-lookup"><span data-stu-id="1e7f7-110">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)<br/>                | <span data-ttu-id="1e7f7-111">本主題介紹 WIC 的中繼資料查詢語言。</span><span class="sxs-lookup"><span data-stu-id="1e7f7-111">This topic introduces the metadata query language for WIC.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="1e7f7-112">原生影像格式中繼資料查詢</span><span class="sxs-lookup"><span data-stu-id="1e7f7-112">Native Image Format Metadata Queries</span></span>](-wic-native-image-format-metadata-queries.md)<br/>   | <span data-ttu-id="1e7f7-113">本主題概要說明用來讀取和寫入 GIF、PNG、TIFF 和 JPEG 影像所支援中繼資料的 [中繼資料查詢語言](-wic-codec-metadataquerylanguage.md) 查詢。</span><span class="sxs-lookup"><span data-stu-id="1e7f7-113">This topic provides an overview of the [metadata query language](-wic-codec-metadataquerylanguage.md) queries for reading and writing metadata supported by GIF, PNG, TIFF and JPEG images.</span></span><br/>                                                                  |
| [<span data-ttu-id="1e7f7-114">讀取和寫入影像中繼資料的總覽</span><span class="sxs-lookup"><span data-stu-id="1e7f7-114">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)<br/> | <span data-ttu-id="1e7f7-115">本主題概要說明如何使用 WIC Api 來讀取和寫入內嵌于影像檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1e7f7-115">This topic provides an overview of how you can use the WIC APIs to read and write metadata that is embedded in image files.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="1e7f7-116">中繼資料擴充性總覽</span><span class="sxs-lookup"><span data-stu-id="1e7f7-116">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)<br/>                      | <span data-ttu-id="1e7f7-117">本主題將介紹為 WIC 建立自訂元資料處理程式的需求，包括中繼資料讀取器和寫入器。</span><span class="sxs-lookup"><span data-stu-id="1e7f7-117">This topic introduces the requirements for creating custom metadata handlers for the WIC, including both metadata readers and writers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1e7f7-118">人員標記總覽</span><span class="sxs-lookup"><span data-stu-id="1e7f7-118">People Tagging Overview</span></span>](-wic-people-tagging.md)<br/>                                      | <span data-ttu-id="1e7f7-119">本主題將介紹新的可延伸中繼資料平臺 (XMP) 架構和 Windows 7 相片屬性 [PeopleNames](../properties/props-system-photo-peoplenames.md) ，可讓您在數位相片中標記個人。</span><span class="sxs-lookup"><span data-stu-id="1e7f7-119">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1e7f7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e7f7-120">See Also</span></span>

[<span data-ttu-id="1e7f7-121">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="1e7f7-121">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="1e7f7-122">參考</span><span class="sxs-lookup"><span data-stu-id="1e7f7-122">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="1e7f7-123">範例</span><span class="sxs-lookup"><span data-stu-id="1e7f7-123">Samples</span></span>](-wic-samples.md)


 

 
