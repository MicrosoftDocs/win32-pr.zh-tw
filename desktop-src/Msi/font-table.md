---
description: 字型表格包含向系統註冊字型檔案的資訊。
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: 字型資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944551"
---
# <a name="font-table"></a><span data-ttu-id="ec6f7-103">字型資料表</span><span class="sxs-lookup"><span data-stu-id="ec6f7-103">Font Table</span></span>

<span data-ttu-id="ec6f7-104">字型表格包含向系統註冊字型檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-104">The Font table contains the information for registering font files with the system.</span></span>

<span data-ttu-id="ec6f7-105">字型資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-105">The Font table has the following columns.</span></span>



| <span data-ttu-id="ec6f7-106">Column</span><span class="sxs-lookup"><span data-stu-id="ec6f7-106">Column</span></span>    | <span data-ttu-id="ec6f7-107">類型</span><span class="sxs-lookup"><span data-stu-id="ec6f7-107">Type</span></span>                         | <span data-ttu-id="ec6f7-108">答案</span><span class="sxs-lookup"><span data-stu-id="ec6f7-108">Key</span></span> | <span data-ttu-id="ec6f7-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ec6f7-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="ec6f7-110">檔案\_</span><span class="sxs-lookup"><span data-stu-id="ec6f7-110">File\_</span></span>    | [<span data-ttu-id="ec6f7-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="ec6f7-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ec6f7-112">Y</span><span class="sxs-lookup"><span data-stu-id="ec6f7-112">Y</span></span>   | <span data-ttu-id="ec6f7-113">N</span><span class="sxs-lookup"><span data-stu-id="ec6f7-113">N</span></span>        |
| <span data-ttu-id="ec6f7-114">FontTitle</span><span class="sxs-lookup"><span data-stu-id="ec6f7-114">FontTitle</span></span> | [<span data-ttu-id="ec6f7-115">Text</span><span class="sxs-lookup"><span data-stu-id="ec6f7-115">Text</span></span>](text.md)             | <span data-ttu-id="ec6f7-116">N</span><span class="sxs-lookup"><span data-stu-id="ec6f7-116">N</span></span>   | <span data-ttu-id="ec6f7-117">Y</span><span class="sxs-lookup"><span data-stu-id="ec6f7-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ec6f7-118">資料行</span><span class="sxs-lookup"><span data-stu-id="ec6f7-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ec6f7-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="ec6f7-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="ec6f7-120">字型檔案的檔案 [資料表](file-table.md) 專案中的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-120">External key into the [File table](file-table.md) entry for the font file.</span></span> <span data-ttu-id="ec6f7-121">建議包含字型檔案的元件在 \_ [component 資料表](component-table.md)的目錄資料行中指定 FontsFolder。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-121">It is recommended that the component containing the font file have the FontsFolder specified in the Directory\_ column of the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec6f7-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span><span class="sxs-lookup"><span data-stu-id="ec6f7-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span></span>
</dt> <dd>

<span data-ttu-id="ec6f7-123">字型名稱。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-123">Font name.</span></span> <span data-ttu-id="ec6f7-124">建議您針對 TrueType 字型和 TrueType 集合將此資料行保留為 null，因為安裝程式可以在從字型檔案讀取正確的字型標題之後註冊字型。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-124">It is recommended that you leave this column null for TrueType Fonts and TrueType Collections because the installer can register the font after reading the correct font title from the font file.</span></span> <span data-ttu-id="ec6f7-125">如果輸入字型名稱，它必須與字型檔案中的字型標題相同。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-125">If the font name is entered, it must be identical to font title from the font file.</span></span> <span data-ttu-id="ec6f7-126">您必須為沒有內嵌名稱的字型指定標題，例如 fon 檔。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-126">You must specify a title for fonts that do not have embedded names, such as .fon files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec6f7-127">備註</span><span class="sxs-lookup"><span data-stu-id="ec6f7-127">Remarks</span></span>

<span data-ttu-id="ec6f7-128">當執行 [RegisterFonts 動作](registerfonts-action.md) 或 [UnregisterFonts 動作](unregisterfonts-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-128">This table is referred to when the [RegisterFonts action](registerfonts-action.md) or the [UnregisterFonts action](unregisterfonts-action.md) is executed.</span></span>

<span data-ttu-id="ec6f7-129">如果 [FontTitle] 欄位是空的，則會直接從指定的字型檔案讀取字型名稱。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-129">If the FontTitle field is left Null, the Font name is read directly from the font file specified.</span></span> <span data-ttu-id="ec6f7-130">如果記錄在 FontTitle 欄位中的字型名稱與字型檔案中記錄的內部字型名稱不同，則會使用 [RegisterFonts 動作](registerfonts-action.md)將字型註冊兩次。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-130">If the font name recorded into the FontTitle field differs from the internal font name recorded in the font file, the font is registered twice by the [RegisterFonts action](registerfonts-action.md).</span></span>

<span data-ttu-id="ec6f7-131">字型檔案不能以語言識別項撰寫，因為字型沒有內嵌的語言識別項資源。因此字型檔案的 [語言] 資料 [行應該保留](file-table.md) null。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-131">Font files should not be authored with a language ID, as fonts do not have an embedded language ID resource.Thus the Language column of the [File table](file-table.md) should be left null for font files.</span></span>

<span data-ttu-id="ec6f7-132">因為安裝程式預設不會 refcount 字型檔案，所以卸載應用程式時，可能會移除預先存在的字型檔案及其元件。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-132">Because the installer does not refcount font files by default, preexisting font files may be removed with their component when uninstalling an application.</span></span> <span data-ttu-id="ec6f7-133">為了確保不會移除字型檔案，作者可以  \_ \_ \_ 針對包含字型檔案的元件，在元件資料表 msi 元件資料表的 [屬性] 資料行中設定 msidbComponentAttributesSharedDllRefCount 或 msidbComponentAttributesPermanent 位旗標。</span><span class="sxs-lookup"><span data-stu-id="ec6f7-133">To ensure that a font file is not removed, authors may set the **msidbComponentAttributesSharedDllRefCount** or **msidbComponentAttributesPermanent** bit flags in the Attributes column of the Component Table\_msi\_Component\_Table for the component containing the font file.</span></span>

## <a name="validation"></a><span data-ttu-id="ec6f7-134">驗證</span><span class="sxs-lookup"><span data-stu-id="ec6f7-134">Validation</span></span>

<dl>

[<span data-ttu-id="ec6f7-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="ec6f7-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ec6f7-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="ec6f7-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ec6f7-137">ICE07</span><span class="sxs-lookup"><span data-stu-id="ec6f7-137">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="ec6f7-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="ec6f7-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ec6f7-139">ICE51</span><span class="sxs-lookup"><span data-stu-id="ec6f7-139">ICE51</span></span>](ice51.md)  
[<span data-ttu-id="ec6f7-140">ICE60</span><span class="sxs-lookup"><span data-stu-id="ec6f7-140">ICE60</span></span>](ice60.md)  
</dl>

 

 



