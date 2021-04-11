---
title: Windows Media Format SDK 程式設計參考
description: Windows Media Format SDK 程式設計參考
ms.assetid: cafb8aa7-6b0a-4bcc-b618-2520a31cd7a6
keywords:
- Windows Media Format SDK，程式設計參考
- 'Windows Media Format SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) ，程式設計參考
- ASF (Advanced Systems Format) ，程式設計參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c316b85e91c31b513fbfcdff003ba37efea93b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383709"
---
# <a name="windows-media-format-sdk-programming-reference"></a><span data-ttu-id="468a4-107">Windows Media Format SDK 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="468a4-107">Windows Media Format SDK Programming Reference</span></span>

<span data-ttu-id="468a4-108">Microsoft® Windows Media® Format 軟體發展工具組 (SDK) 支援一系列的物件、介面、獨立函式、結構、列舉類型、屬性等等。</span><span class="sxs-lookup"><span data-stu-id="468a4-108">The Microsoft® Windows Media® Format Software Development Kit (SDK) supports a range of objects, interfaces, independent functions, structures, enumeration types, attributes, and so on.</span></span> <span data-ttu-id="468a4-109">下列各節將詳細說明這些詳細資料。</span><span class="sxs-lookup"><span data-stu-id="468a4-109">The following sections document these in detail.</span></span>



| <span data-ttu-id="468a4-110">區段</span><span class="sxs-lookup"><span data-stu-id="468a4-110">Section</span></span>                                                                              | <span data-ttu-id="468a4-111">描述</span><span class="sxs-lookup"><span data-stu-id="468a4-111">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="468a4-112">物件</span><span class="sxs-lookup"><span data-stu-id="468a4-112">Objects</span></span>](objects.md)                                                               | <span data-ttu-id="468a4-113">描述 Windows Media 格式 SDK 中每個物件所支援的物件和介面。</span><span class="sxs-lookup"><span data-stu-id="468a4-113">Describes the objects and the interfaces supported by each object in the Windows Media Format SDK.</span></span>           |
| [<span data-ttu-id="468a4-114">函數</span><span class="sxs-lookup"><span data-stu-id="468a4-114">Functions</span></span>](functions.md)                                                           | <span data-ttu-id="468a4-115">描述所有的獨立函式，通常是用來建立和初始化各種物件的函式。</span><span class="sxs-lookup"><span data-stu-id="468a4-115">Describes all the independent functions, typically those used to create and initialize various objects.</span></span>      |
| [<span data-ttu-id="468a4-116">介面</span><span class="sxs-lookup"><span data-stu-id="468a4-116">Interfaces</span></span>](interfaces.md)                                                         | <span data-ttu-id="468a4-117">描述此 SDK 中的所有介面和方法。</span><span class="sxs-lookup"><span data-stu-id="468a4-117">Describes all the interfaces and methods in this SDK.</span></span>                                                        |
| [<span data-ttu-id="468a4-118">結構</span><span class="sxs-lookup"><span data-stu-id="468a4-118">Structures</span></span>](structures.md)                                                         | <span data-ttu-id="468a4-119">描述此 SDK 所支援的結構。</span><span class="sxs-lookup"><span data-stu-id="468a4-119">Describes the structures supported by this SDK.</span></span>                                                              |
| [<span data-ttu-id="468a4-120">列舉類型</span><span class="sxs-lookup"><span data-stu-id="468a4-120">Enumeration Types</span></span>](enumeration-types.md)                                           | <span data-ttu-id="468a4-121">描述此 SDK 所支援的列舉類型。</span><span class="sxs-lookup"><span data-stu-id="468a4-121">Describes the enumeration types supported by this SDK.</span></span>                                                       |
| [<span data-ttu-id="468a4-122">屬性</span><span class="sxs-lookup"><span data-stu-id="468a4-122">Attributes</span></span>](attributes.md)                                                         | <span data-ttu-id="468a4-123">描述可在 ASF 檔案的標頭中指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="468a4-123">Describes the attributes that can be specified in the headers of ASF files.</span></span>                                  |
| [<span data-ttu-id="468a4-124">媒體類型</span><span class="sxs-lookup"><span data-stu-id="468a4-124">Media Types</span></span>](media-types.md)                                                       | <span data-ttu-id="468a4-125">描述此 SDK 所使用的媒體類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="468a4-125">Describes the media type identifiers used by this SDK.</span></span>                                                       |
| [<span data-ttu-id="468a4-126">輸出設定</span><span class="sxs-lookup"><span data-stu-id="468a4-126">Output Settings</span></span>](output-settings.md)                                               | <span data-ttu-id="468a4-127">描述用來識別讀取器輸出設定的全域常數。</span><span class="sxs-lookup"><span data-stu-id="468a4-127">Describes the global constants used to identify reader output settings.</span></span>                                      |
| [<span data-ttu-id="468a4-128">語言字串</span><span class="sxs-lookup"><span data-stu-id="468a4-128">Language Strings</span></span>](language-strings.md)                                             | <span data-ttu-id="468a4-129">描述常用於 RFC 1766 相容的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="468a4-129">Describes the commonly used RFC 1766-compliant language identifiers.</span></span>                                         |
| [<span data-ttu-id="468a4-130">裝置一致性範本參數</span><span class="sxs-lookup"><span data-stu-id="468a4-130">Device Conformance Template Parameters</span></span>](device-conformance-template-parameters.md) | <span data-ttu-id="468a4-131">描述裝置一致性範本，其描述適用于各種裝置的值範圍。</span><span class="sxs-lookup"><span data-stu-id="468a4-131">Describes the device conformance templates, which describe ranges of values appropriate for various devices.</span></span> |
| [<span data-ttu-id="468a4-132">系統設定檔</span><span class="sxs-lookup"><span data-stu-id="468a4-132">System Profiles</span></span>](system-profiles.md)                                               | <span data-ttu-id="468a4-133">列出所有支援的系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="468a4-133">Lists all supported system profiles.</span></span>                                                                         |
| [<span data-ttu-id="468a4-134">當地語系化的系統設定檔</span><span class="sxs-lookup"><span data-stu-id="468a4-134">Localized System Profiles</span></span>](localized-system-profiles.md)                           | <span data-ttu-id="468a4-135">列出 SDK 隨附的當地語系化系統設定檔檔案，以及與每個檔案相關聯的語言。</span><span class="sxs-lookup"><span data-stu-id="468a4-135">Lists the localized system profile files included with the SDK and the languages associated with each.</span></span>       |
| [<span data-ttu-id="468a4-136">GUID 值</span><span class="sxs-lookup"><span data-stu-id="468a4-136">GUID Values</span></span>](guid-values.md)                                                       | <span data-ttu-id="468a4-137">描述此 SDK 所使用的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="468a4-137">Describes the GUID values used by this SDK.</span></span>                                                                  |
| [<span data-ttu-id="468a4-138">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="468a4-138">Error Codes</span></span>](error-codes.md)                                                       | <span data-ttu-id="468a4-139">描述 SDK 中方法和函式所傳回的常見錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="468a4-139">Describes common error codes returned by methods and functions in the SDK.</span></span>                                   |
| [<span data-ttu-id="468a4-140">來源外掛程式</span><span class="sxs-lookup"><span data-stu-id="468a4-140">Source Plug-ins</span></span>](source-plug-ins.md)                                               | <span data-ttu-id="468a4-141">描述使用者實作為來源的需求。</span><span class="sxs-lookup"><span data-stu-id="468a4-141">Describes the requirements for user-implemented sources.</span></span>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="468a4-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="468a4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="468a4-143">**關於 Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="468a4-143">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="468a4-144">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="468a4-144">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="468a4-145">**Windows Media Format 11 SDK**</span><span class="sxs-lookup"><span data-stu-id="468a4-145">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




