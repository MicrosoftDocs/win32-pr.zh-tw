---
description: Session 物件的 FormatRecord 方法會從範本傳回格式化的字串，並記錄資料。
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: FormatRecord 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992912"
---
# <a name="sessionformatrecord-method"></a><span data-ttu-id="1c12e-103">FormatRecord 方法</span><span class="sxs-lookup"><span data-stu-id="1c12e-103">Session.FormatRecord method</span></span>

<span data-ttu-id="1c12e-104">[**Session**](session-object.md)物件的 **FormatRecord** 方法會從範本傳回格式化的字串，並記錄資料。</span><span class="sxs-lookup"><span data-stu-id="1c12e-104">The **FormatRecord** method of the [**Session**](session-object.md) object returns a formatted string from a template and record data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c12e-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c12e-105">Syntax</span></span>


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="1c12e-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c12e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c12e-107">*記錄*</span><span class="sxs-lookup"><span data-stu-id="1c12e-107">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="1c12e-108">必要的 **記錄** 物件，其中包含要格式化的範本和資料。</span><span class="sxs-lookup"><span data-stu-id="1c12e-108">Required **Record** object containing a template and data to be formatted.</span></span> <span data-ttu-id="1c12e-109">您必須在欄位0中設定範本字串，後面接著任何參考的資料參數。</span><span class="sxs-lookup"><span data-stu-id="1c12e-109">The template string must be set in field 0 followed by any referenced data parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c12e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c12e-110">Return value</span></span>

<span data-ttu-id="1c12e-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1c12e-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c12e-112">備註</span><span class="sxs-lookup"><span data-stu-id="1c12e-112">Remarks</span></span>

<span data-ttu-id="1c12e-113">**FormatRecord** 方法會使用下列格式進程。</span><span class="sxs-lookup"><span data-stu-id="1c12e-113">The **FormatRecord** method uses the following format process.</span></span>

<span data-ttu-id="1c12e-114">要[格式化](formatted.md)的參數會以方括弧括住 \[ ... \]</span><span class="sxs-lookup"><span data-stu-id="1c12e-114">Parameters to be [formatted](formatted.md) are enclosed in square brackets \[..\].</span></span> <span data-ttu-id="1c12e-115">可以反復執行方括弧，因為會從外部解析出替代。</span><span class="sxs-lookup"><span data-stu-id="1c12e-115">The square brackets can be iterated because the substitutions are resolved from inside out.</span></span>

<span data-ttu-id="1c12e-116">如果字串的一部分是以大括弧 {} 括住，且未包含方括弧，則部分會保持不變，包括大括弧。</span><span class="sxs-lookup"><span data-stu-id="1c12e-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, the part is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="1c12e-117">如果字串的一部分是以大括弧括住，且包含一或多個屬性名稱，而且如果找到所有屬性，則會顯示具有已解析之替代的文字 () 不含大括弧。</span><span class="sxs-lookup"><span data-stu-id="1c12e-117">If a part of the string is enclosed in curly braces and contains one or more property names, and if all the properties are found, the text (with the resolved substitutions) is displayed without the curly braces.</span></span> <span data-ttu-id="1c12e-118">如果找不到任何屬性，則會移除大括弧和大括弧本身中的所有文字。</span><span class="sxs-lookup"><span data-stu-id="1c12e-118">If any of the properties are not found, all the text in the curly braces and the braces themselves are removed.</span></span>

<span data-ttu-id="1c12e-119">**若要使用 FormatRecord 方法將字串格式化**</span><span class="sxs-lookup"><span data-stu-id="1c12e-119">**To format strings using the FormatRecord method**</span></span>

1.  <span data-ttu-id="1c12e-120">藉由將標記取代為對應的 [記錄] 欄位的值，並在不產生任何文字的情況下，使用遺漏或 Null 值來取代數值參數。</span><span class="sxs-lookup"><span data-stu-id="1c12e-120">The numeric parameters are substituted by replacing the marker with the value of the corresponding record field, with missing or Null values producing no text.</span></span>
2.  <span data-ttu-id="1c12e-121">藉由以對應的值取代非記錄參數來處理結果的字串，如下列描述所述。</span><span class="sxs-lookup"><span data-stu-id="1c12e-121">The string that results is processed by replacing the non-record parameters with the corresponding values, as noted in the following descriptions.</span></span>
    -   <span data-ttu-id="1c12e-122">如果遇到 "propertyname" 格式的子字串，則會 \[ \] 由屬性的值取代。</span><span class="sxs-lookup"><span data-stu-id="1c12e-122">If a substring of the form "\[propertyname\]" is encountered, it is replaced by the value of the property.</span></span>
    -   <span data-ttu-id="1c12e-123">如果找到 "% environmentvariable" 格式的子字串 \[ \] ，則會取代環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="1c12e-123">If a substring of the form "\[%environmentvariable\]" is found, the value of the environment variable is substituted.</span></span>
    -   <span data-ttu-id="1c12e-124">如果找到 filekey 格式的子字串，則會以檔案的 \[ \#  \] 完整路徑來取代它，而值 *filekey* 會用來做為檔案 [資料表](file-table.md)中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1c12e-124">If a substring of the form \[\#*filekey*\] is found, it is replaced by the full path of the file, with the value *filekey* used as a key into the [File table](file-table.md).</span></span> <span data-ttu-id="1c12e-125">Filekey 的值 \[ \#  \] 會保持空白，而且在安裝程式執行[CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和[CostFinalize 動作](costfinalize-action.md)之前，不會由路徑取代。</span><span class="sxs-lookup"><span data-stu-id="1c12e-125">The value of \[\#*filekey*\] remains blank and is not replaced by a path until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="1c12e-126">Filekey 的值 \[ \#  \] 取決於檔案所屬元件的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="1c12e-126">The value of \[\#*filekey*\] depends upon the installation state of the component to which the file belongs.</span></span> <span data-ttu-id="1c12e-127">如果元件是從來源執行，則此值為檔案來源位置的路徑。</span><span class="sxs-lookup"><span data-stu-id="1c12e-127">If the component is being run from source, the value is the path to the source location of the file.</span></span> <span data-ttu-id="1c12e-128">如果元件是在本機執行，則此值是安裝之後檔案目標位置的路徑。</span><span class="sxs-lookup"><span data-stu-id="1c12e-128">If the component is being run locally, the value is the path to the target location of the file after installation.</span></span> <span data-ttu-id="1c12e-129">如果元件不存在，則路徑是空白的。</span><span class="sxs-lookup"><span data-stu-id="1c12e-129">If the component is absent, the path is blank.</span></span> <span data-ttu-id="1c12e-130">如需有關檢查元件安裝狀態的詳細資訊，請參閱 [檢查功能、元件、](checking-the-installation-of-features-components-files.md)檔案的安裝。</span><span class="sxs-lookup"><span data-stu-id="1c12e-130">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="1c12e-131">如果找到 $componentkey 格式的子字串 \[  \] ，就會由元件的安裝目錄取代，並在 [元件資料表](component-table.md)中將值 *componentkey* 當做索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="1c12e-131">If a substring of the form \[*$componentkey*\] is found, it is replaced by the install directory of the component, with the value *componentkey* used as a key into the [Component table](component-table.md).</span></span> <span data-ttu-id="1c12e-132">Componentkey 的值 \[ $  \] 會保持空白，而且在安裝程式執行[CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和[CostFinalize 動作](costfinalize-action.md)之前，不會以目錄取代。</span><span class="sxs-lookup"><span data-stu-id="1c12e-132">The value of \[$*componentkey*\] remains blank and is not replaced by a directory until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="1c12e-133">Componentkey 的值 \[ $  \] 取決於元件的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="1c12e-133">The value of \[$*componentkey*\] depends upon the installation state of the component.</span></span> <span data-ttu-id="1c12e-134">如果元件是從來源執行，則此值為檔案的來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="1c12e-134">If the component is being run from source, the value is the source directory of the file.</span></span> <span data-ttu-id="1c12e-135">如果元件是在本機執行，則在安裝之後，此值會是目標目錄。</span><span class="sxs-lookup"><span data-stu-id="1c12e-135">If the component is being run locally, the value is the target directory after installation.</span></span> <span data-ttu-id="1c12e-136">如果元件不存在，此值會保留空白。</span><span class="sxs-lookup"><span data-stu-id="1c12e-136">If the component is absent, the value is left blank.</span></span> <span data-ttu-id="1c12e-137">如需有關檢查元件安裝狀態的詳細資訊，請參閱 [檢查功能、元件、](checking-the-installation-of-features-components-files.md)檔案的安裝。</span><span class="sxs-lookup"><span data-stu-id="1c12e-137">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="1c12e-138">如果找到 "c" 格式的子字串，則會 \[ \\ \] 由字元取代，而不需要進一步處理。</span><span class="sxs-lookup"><span data-stu-id="1c12e-138">If a substring of the form "\[\\c\]" is found, it is replaced by the character without any further processing.</span></span> <span data-ttu-id="1c12e-139">只保留反斜線之後的第一個字元;所有其他專案都已移除。</span><span class="sxs-lookup"><span data-stu-id="1c12e-139">Only the first character after the backslash is kept; everything else is removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c12e-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c12e-140">Requirements</span></span>



| <span data-ttu-id="1c12e-141">需求</span><span class="sxs-lookup"><span data-stu-id="1c12e-141">Requirement</span></span> | <span data-ttu-id="1c12e-142">值</span><span class="sxs-lookup"><span data-stu-id="1c12e-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c12e-143">版本</span><span class="sxs-lookup"><span data-stu-id="1c12e-143">Version</span></span><br/> | <span data-ttu-id="1c12e-144">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="1c12e-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1c12e-145">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="1c12e-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1c12e-146">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1c12e-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1c12e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="1c12e-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="1c12e-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c12e-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1c12e-149">IID</span><span class="sxs-lookup"><span data-stu-id="1c12e-149">IID</span></span><br/>     | <span data-ttu-id="1c12e-150">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1c12e-150">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="1c12e-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c12e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c12e-152">格式 化</span><span class="sxs-lookup"><span data-stu-id="1c12e-152">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="1c12e-153">資料行資料類型</span><span class="sxs-lookup"><span data-stu-id="1c12e-153">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




