---
title: VERSIONINFO 資源
description: 定義版本資訊資源。 資源包含檔案的相關資訊，例如其版本號碼、其預定的作業系統，以及其原始檔案名。 此資源適用于版本資訊功能。
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- VERSIONINFO 資源功能表與其他資源
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "104316717"
---
# <a name="versioninfo-resource"></a><span data-ttu-id="3de0f-106">VERSIONINFO 資源</span><span class="sxs-lookup"><span data-stu-id="3de0f-106">VERSIONINFO resource</span></span>

<span data-ttu-id="3de0f-107">定義版本資訊資源。</span><span class="sxs-lookup"><span data-stu-id="3de0f-107">Defines a version-information resource.</span></span> <span data-ttu-id="3de0f-108">資源包含檔案的相關資訊，例如其版本號碼、其預定的作業系統，以及其原始檔案名。</span><span class="sxs-lookup"><span data-stu-id="3de0f-108">The resource contains such information about the file as its version number, its intended operating system, and its original filename.</span></span> <span data-ttu-id="3de0f-109">此資源適用于 [版本資訊](./version-information.md) 功能。</span><span class="sxs-lookup"><span data-stu-id="3de0f-109">The resource is intended to be used with the [Version Information](./version-information.md) functions.</span></span>

<span data-ttu-id="3de0f-110">有兩種方式可將 **VERSIONINFO** 語句格式化：</span><span class="sxs-lookup"><span data-stu-id="3de0f-110">There are two ways to format a **VERSIONINFO** statement:</span></span>

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

<span data-ttu-id="3de0f-111">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="3de0f-111">\- or -</span></span>

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="3de0f-112">參數</span><span class="sxs-lookup"><span data-stu-id="3de0f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de0f-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span><span class="sxs-lookup"><span data-stu-id="3de0f-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-114">版本資訊資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3de0f-114">Version-information resource identifier.</span></span> <span data-ttu-id="3de0f-115">此值必須是1。</span><span class="sxs-lookup"><span data-stu-id="3de0f-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="3de0f-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*固定資訊*</span><span class="sxs-lookup"><span data-stu-id="3de0f-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-117">版本資訊，例如檔案版本和預定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="3de0f-117">Version information, such as the file version and the intended operating system.</span></span> <span data-ttu-id="3de0f-118">這個參數是由下列語句所組成。</span><span class="sxs-lookup"><span data-stu-id="3de0f-118">This parameter consists of the following statements.</span></span>



| <span data-ttu-id="3de0f-119">陳述式</span><span class="sxs-lookup"><span data-stu-id="3de0f-119">Statement</span></span>                         | <span data-ttu-id="3de0f-120">描述</span><span class="sxs-lookup"><span data-stu-id="3de0f-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de0f-121">**FILEVERSION** *版本*</span><span class="sxs-lookup"><span data-stu-id="3de0f-121">**FILEVERSION** *version*</span></span>         | <span data-ttu-id="3de0f-122">檔案的二進位版本號碼。</span><span class="sxs-lookup"><span data-stu-id="3de0f-122">Binary version number for the file.</span></span> <span data-ttu-id="3de0f-123">*版本* 是由 4 16 位整數所定義的 2 32 位整數所組成。</span><span class="sxs-lookup"><span data-stu-id="3de0f-123">The *version* consists of two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="3de0f-124">例如，"FILEVERSION 3，10，0，61" 會以該順序轉譯成兩個雙字：0x0003000a 和0x0000003d。</span><span class="sxs-lookup"><span data-stu-id="3de0f-124">For example, "FILEVERSION 3,10,0,61" is translated into two doublewords: 0x0003000a and 0x0000003d, in that order.</span></span> <span data-ttu-id="3de0f-125">因此，如果 *version* 是由 **DWORD** 值 *dw1* 和 *dw2* 所定義，則它們必須出現在 **FILEVERSION** 語句中，如下所示：、 `HIWORD(dw1)` `LOWORD(dw1)` 、 `HIWORD(dw2)` 、 `LOWORD(dw2)` 。</span><span class="sxs-lookup"><span data-stu-id="3de0f-125">Therefore, if *version* is defined by the **DWORD** values *dw1* and *dw2*, they need to appear in the **FILEVERSION** statement as follows: `HIWORD(dw1)`, `LOWORD(dw1)`, `HIWORD(dw2)`, `LOWORD(dw2)`.</span></span> |
| <span data-ttu-id="3de0f-126">**PRODUCTVERSION** *版本*</span><span class="sxs-lookup"><span data-stu-id="3de0f-126">**PRODUCTVERSION** *version*</span></span>      | <span data-ttu-id="3de0f-127">用來散發檔案的產品二進位版本號碼。</span><span class="sxs-lookup"><span data-stu-id="3de0f-127">Binary version number for the product with which the file is distributed.</span></span> <span data-ttu-id="3de0f-128">*Version* 參數是 2 32 位整數，由 4 16 位整數所定義。</span><span class="sxs-lookup"><span data-stu-id="3de0f-128">The *version* parameter is two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="3de0f-129">如需 *版本* 的詳細資訊，請參閱 **FILEVERSION** 描述。</span><span class="sxs-lookup"><span data-stu-id="3de0f-129">For more information about *version*, see the **FILEVERSION** description.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="3de0f-130">**FILEFLAGSMASK** *FILEFLAGSMASK*</span><span class="sxs-lookup"><span data-stu-id="3de0f-130">**FILEFLAGSMASK** *fileflagsmask*</span></span> | <span data-ttu-id="3de0f-131">指出 **fileflags 機碼** 語句中的位有效。</span><span class="sxs-lookup"><span data-stu-id="3de0f-131">Indicates which bits in the **FILEFLAGS** statement are valid.</span></span> <span data-ttu-id="3de0f-132">若為16位 Windows，則此值為0x3f。</span><span class="sxs-lookup"><span data-stu-id="3de0f-132">For 16-bit Windows, this value is 0x3f.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3de0f-133">**Fileflags 機碼** *fileflags 機碼*</span><span class="sxs-lookup"><span data-stu-id="3de0f-133">**FILEFLAGS** *fileflags*</span></span>         | <span data-ttu-id="3de0f-134">檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="3de0f-134">Attributes of the file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3de0f-135">**FILEOS** *FILEOS*</span><span class="sxs-lookup"><span data-stu-id="3de0f-135">**FILEOS** *fileos*</span></span>               | <span data-ttu-id="3de0f-136">專為其設計此檔案的作業系統。</span><span class="sxs-lookup"><span data-stu-id="3de0f-136">Operating system for which this file was designed.</span></span> <span data-ttu-id="3de0f-137">*Fileos* 參數可以是 [備註] 區段中提供的其中一個作業系統值。</span><span class="sxs-lookup"><span data-stu-id="3de0f-137">The *fileos* parameter can be one of the operating system values given in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3de0f-138">**類型** 類型 *類型*</span><span class="sxs-lookup"><span data-stu-id="3de0f-138">**FILETYPE** *filetype*</span></span>           | <span data-ttu-id="3de0f-139">一般檔案類型。</span><span class="sxs-lookup"><span data-stu-id="3de0f-139">General type of file.</span></span> <span data-ttu-id="3de0f-140">內容 *類型參數可以* 是 [備註] 區段中所列的其中一種檔案類型值。</span><span class="sxs-lookup"><span data-stu-id="3de0f-140">The *filetype* parameter can be one of the file type values listed in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3de0f-141">**FILESUBTYPE** *子類型*</span><span class="sxs-lookup"><span data-stu-id="3de0f-141">**FILESUBTYPE** *subtype*</span></span>         | <span data-ttu-id="3de0f-142">檔案的功能。</span><span class="sxs-lookup"><span data-stu-id="3de0f-142">Function of the file.</span></span> <span data-ttu-id="3de0f-143">除非 **類型類型語句中** 的 *類型* 參數是 VFT winspool.drv、VFT  \_ \_ font-family 或 VFT VXD，否則子類型參數為零 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3de0f-143">The *subtype* parameter is zero unless the *filetype* parameter in the **FILETYPE** statement is VFT\_DRV, VFT\_FONT, or VFT\_VXD.</span></span> <span data-ttu-id="3de0f-144">如需檔案子類型值的清單，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="3de0f-144">For a list of file subtype values, see the Remarks section.</span></span>                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="3de0f-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block 語句*</span><span class="sxs-lookup"><span data-stu-id="3de0f-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-146">指定一或多個版本資訊區塊。</span><span class="sxs-lookup"><span data-stu-id="3de0f-146">Specifies one or more version-information blocks.</span></span> <span data-ttu-id="3de0f-147">區塊可以包含字串資訊或變數資訊。</span><span class="sxs-lookup"><span data-stu-id="3de0f-147">A block can contain string information or variable information.</span></span> <span data-ttu-id="3de0f-148">如需詳細資訊，請參閱 [**StringFileInfo block**](stringfileinfo-block.md) 或 [**VarFileInfo block**](varfileinfo-block.md)。</span><span class="sxs-lookup"><span data-stu-id="3de0f-148">For more information, see [**StringFileInfo Block**](stringfileinfo-block.md) or [**VarFileInfo Block**](varfileinfo-block.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3de0f-149">備註</span><span class="sxs-lookup"><span data-stu-id="3de0f-149">Remarks</span></span>

<span data-ttu-id="3de0f-150">若要使用以 **VERSIONINFO** 語句指定的常數，您必須在資源定義檔中包含 Winver .H 或 Windows .h 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="3de0f-150">To use the constants specified with the **VERSIONINFO** statement, you must include the Winver.h or Windows.h header file in the resource-definition file.</span></span>

<span data-ttu-id="3de0f-151">下列清單描述 **VERSIONINFO** 語句中使用的參數：</span><span class="sxs-lookup"><span data-stu-id="3de0f-151">The following list describes the parameters used in the **VERSIONINFO** statement:</span></span>

<dl> <dt>

<span data-ttu-id="3de0f-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags 機碼*</span><span class="sxs-lookup"><span data-stu-id="3de0f-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-153">下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="3de0f-153">A combination of the following values.</span></span>



| <span data-ttu-id="3de0f-154">值</span><span class="sxs-lookup"><span data-stu-id="3de0f-154">Value</span></span>                      | <span data-ttu-id="3de0f-155">描述</span><span class="sxs-lookup"><span data-stu-id="3de0f-155">Description</span></span>                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de0f-156">**VS \_ FF \_ DEBUG**</span><span class="sxs-lookup"><span data-stu-id="3de0f-156">**VS\_FF\_DEBUG**</span></span>          | <span data-ttu-id="3de0f-157">檔案包含偵錯工具資訊，或是已啟用偵錯工具的編譯功能。</span><span class="sxs-lookup"><span data-stu-id="3de0f-157">File contains debugging information or is compiled with debugging features enabled.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="3de0f-158">**VS \_ FF \_ 修補**</span><span class="sxs-lookup"><span data-stu-id="3de0f-158">**VS\_FF\_PATCHED**</span></span>        | <span data-ttu-id="3de0f-159">檔案已修改，而且與相同版本號碼的原始運送檔案不相同。</span><span class="sxs-lookup"><span data-stu-id="3de0f-159">File has been modified and is not identical to the original shipping file of the same version number.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="3de0f-160">**VS \_ FF \_ 發行前版本**</span><span class="sxs-lookup"><span data-stu-id="3de0f-160">**VS\_FF\_PRERELEASE**</span></span>     | <span data-ttu-id="3de0f-161">檔案是開發版本，而不是商業發行的產品。</span><span class="sxs-lookup"><span data-stu-id="3de0f-161">File is a development version, not a commercially released product.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="3de0f-162">**VS \_ FF \_ PRI加值稅EBUILD**</span><span class="sxs-lookup"><span data-stu-id="3de0f-162">**VS\_FF\_PRIVATEBUILD**</span></span>   | <span data-ttu-id="3de0f-163">檔案不是使用標準發行程式所建立。</span><span class="sxs-lookup"><span data-stu-id="3de0f-163">File was not built using standard release procedures.</span></span> <span data-ttu-id="3de0f-164">如果指定此值， [**StringFileInfo 區塊**](stringfileinfo-block.md) 必須包含 **PrivateBuild** 字串。</span><span class="sxs-lookup"><span data-stu-id="3de0f-164">If this value is given, the [**StringFileInfo block**](stringfileinfo-block.md) must contain a **PrivateBuild** string.</span></span>                                                                                              |
| <span data-ttu-id="3de0f-165">**VS \_ FF \_ SPECIALBUILD**</span><span class="sxs-lookup"><span data-stu-id="3de0f-165">**VS\_FF\_SPECIALBUILD**</span></span>   | <span data-ttu-id="3de0f-166">檔案是由使用標準發行程式的原始公司所建立，但是相同版本號碼之標準檔案的變化。</span><span class="sxs-lookup"><span data-stu-id="3de0f-166">File was built by the original company using standard release procedures but is a variation of the standard file of the same version number.</span></span> <span data-ttu-id="3de0f-167">如果指定了這個值， [ **StringFileInfo** 區塊](stringfileinfo-block.md)區塊就必須包含 **SpecialBuild** 字串。</span><span class="sxs-lookup"><span data-stu-id="3de0f-167">If this value is given, the [**StringFileInfo** block](stringfileinfo-block.md) block must contain a **SpecialBuild** string.</span></span> |
| <span data-ttu-id="3de0f-168">**VS \_ FFI \_ FILEFLAGSMASK**</span><span class="sxs-lookup"><span data-stu-id="3de0f-168">**VS\_FFI\_FILEFLAGSMASK**</span></span> | <span data-ttu-id="3de0f-169">所有上述值的組合。</span><span class="sxs-lookup"><span data-stu-id="3de0f-169">A combination of all the preceding values.</span></span>                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="3de0f-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span><span class="sxs-lookup"><span data-stu-id="3de0f-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-171">下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3de0f-171">One of the following values.</span></span>



| <span data-ttu-id="3de0f-172">值</span><span class="sxs-lookup"><span data-stu-id="3de0f-172">Value</span></span>                   | <span data-ttu-id="3de0f-173">描述</span><span class="sxs-lookup"><span data-stu-id="3de0f-173">Description</span></span>                                                      |
|-------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3de0f-174">**VOS \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="3de0f-174">**VOS\_UNKNOWN**</span></span>        | <span data-ttu-id="3de0f-175">設計檔案的作業系統不明。</span><span class="sxs-lookup"><span data-stu-id="3de0f-175">The operating system for which the file was designed is unknown.</span></span> |
| <span data-ttu-id="3de0f-176">**VOS \_ DOS**</span><span class="sxs-lookup"><span data-stu-id="3de0f-176">**VOS\_DOS**</span></span>            | <span data-ttu-id="3de0f-177">檔案是針對 MS-DOS 所設計。</span><span class="sxs-lookup"><span data-stu-id="3de0f-177">File was designed for MS-DOS.</span></span>                                    |
| <span data-ttu-id="3de0f-178">**VOS \_ NT**</span><span class="sxs-lookup"><span data-stu-id="3de0f-178">**VOS\_NT**</span></span>             | <span data-ttu-id="3de0f-179">檔案是針對32位 Windows 所設計。</span><span class="sxs-lookup"><span data-stu-id="3de0f-179">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="3de0f-180">**VOS \_ \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="3de0f-180">**VOS\_\_WINDOWS16**</span></span>    | <span data-ttu-id="3de0f-181">檔案是針對16位 Windows 所設計。</span><span class="sxs-lookup"><span data-stu-id="3de0f-181">File was designed for 16-bit Windows.</span></span>                            |
| <span data-ttu-id="3de0f-182">**VOS \_ \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="3de0f-182">**VOS\_\_WINDOWS32**</span></span>    | <span data-ttu-id="3de0f-183">檔案是針對32位 Windows 所設計。</span><span class="sxs-lookup"><span data-stu-id="3de0f-183">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="3de0f-184">**VOS \_ DOS \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="3de0f-184">**VOS\_DOS\_WINDOWS16**</span></span> | <span data-ttu-id="3de0f-185">檔案是針對以 MS-DOS 執行的16位 Windows 所設計。</span><span class="sxs-lookup"><span data-stu-id="3de0f-185">File was designed for 16-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="3de0f-186">**VOS \_ DOS \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="3de0f-186">**VOS\_DOS\_WINDOWS32**</span></span> | <span data-ttu-id="3de0f-187">檔案是針對使用 MS-DOS 執行的32位 Windows 所設計。</span><span class="sxs-lookup"><span data-stu-id="3de0f-187">File was designed for 32-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="3de0f-188">**VOS \_ NT \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="3de0f-188">**VOS\_NT\_WINDOWS32**</span></span>  | <span data-ttu-id="3de0f-189">檔案是針對32位 Windows 所設計。</span><span class="sxs-lookup"><span data-stu-id="3de0f-189">File was designed for 32-bit Windows.</span></span>                            |



 

<span data-ttu-id="3de0f-190">0x00002L、0x00003L、0x20000L 和0x30000L 的值是保留的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-190">The values 0x00002L, 0x00003L, 0x20000L and 0x30000L are reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3de0f-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span><span class="sxs-lookup"><span data-stu-id="3de0f-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-192">下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3de0f-192">One of the following values.</span></span>



| <span data-ttu-id="3de0f-193">值</span><span class="sxs-lookup"><span data-stu-id="3de0f-193">Value</span></span>                | <span data-ttu-id="3de0f-194">描述</span><span class="sxs-lookup"><span data-stu-id="3de0f-194">Description</span></span>                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de0f-195">**VFT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="3de0f-195">**VFT\_UNKNOWN**</span></span>     | <span data-ttu-id="3de0f-196">檔案類型未知。</span><span class="sxs-lookup"><span data-stu-id="3de0f-196">File type is unknown.</span></span>                                                                                                       |
| <span data-ttu-id="3de0f-197">**VFT \_ 應用程式**</span><span class="sxs-lookup"><span data-stu-id="3de0f-197">**VFT\_APP**</span></span>         | <span data-ttu-id="3de0f-198">檔案包含應用程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-198">File contains an application.</span></span>                                                                                               |
| <span data-ttu-id="3de0f-199">**VFT \_ DLL**</span><span class="sxs-lookup"><span data-stu-id="3de0f-199">**VFT\_DLL**</span></span>         | <span data-ttu-id="3de0f-200">檔案包含動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="3de0f-200">File contains a dynamic-link library (DLL).</span></span>                                                                                 |
| <span data-ttu-id="3de0f-201">**VFT \_ WINSPOOL.DRV**</span><span class="sxs-lookup"><span data-stu-id="3de0f-201">**VFT\_DRV**</span></span>         | <span data-ttu-id="3de0f-202">檔案包含設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3de0f-202">File contains a device driver.</span></span> <span data-ttu-id="3de0f-203">如果 *類型* 為 **VFT \_ winspool.drv**，則 *子類型* 會包含更具體的驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="3de0f-203">If *filetype* is **VFT\_DRV**, *subtype* contains a more specific description of the driver.</span></span> |
| <span data-ttu-id="3de0f-204">**VFT \_ 字型**</span><span class="sxs-lookup"><span data-stu-id="3de0f-204">**VFT\_FONT**</span></span>        | <span data-ttu-id="3de0f-205">檔案包含字型。</span><span class="sxs-lookup"><span data-stu-id="3de0f-205">File contains a font.</span></span> <span data-ttu-id="3de0f-206">如果 [ *類型* ] 為 [VFT] \_ 字型，則 *子類型* 會包含更明確的字型描述。</span><span class="sxs-lookup"><span data-stu-id="3de0f-206">If *filetype* is VFT\_FONT, *subtype* contains a more specific description of the font.</span></span>               |
| <span data-ttu-id="3de0f-207">**VFT \_ VXD**</span><span class="sxs-lookup"><span data-stu-id="3de0f-207">**VFT\_VXD**</span></span>         | <span data-ttu-id="3de0f-208">檔案包含虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="3de0f-208">File contains a virtual device.</span></span>                                                                                             |
| <span data-ttu-id="3de0f-209">**VFT \_ 靜態 \_ LIB**</span><span class="sxs-lookup"><span data-stu-id="3de0f-209">**VFT\_STATIC\_LIB**</span></span> | <span data-ttu-id="3de0f-210">檔案包含靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="3de0f-210">File contains a static-link library.</span></span>                                                                                        |



 

<span data-ttu-id="3de0f-211">所有其他值都會保留給 Microsoft 使用。</span><span class="sxs-lookup"><span data-stu-id="3de0f-211">All other values are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="3de0f-212"><span id="subtype"></span><span id="SUBTYPE"></span>*亞*</span><span class="sxs-lookup"><span data-stu-id="3de0f-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtype*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-213">有關檔案類型的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="3de0f-213">Additional information about the file type.</span></span>

<span data-ttu-id="3de0f-214">如果資料 *類型* 指定 **VFT \_ winspool.drv**，則此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3de0f-214">If *filetype* specifies **VFT\_DRV**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="3de0f-215">值</span><span class="sxs-lookup"><span data-stu-id="3de0f-215">Value</span></span>                             | <span data-ttu-id="3de0f-216">描述</span><span class="sxs-lookup"><span data-stu-id="3de0f-216">Description</span></span>                               |
|-----------------------------------|-------------------------------------------|
| <span data-ttu-id="3de0f-217">**VFT2 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="3de0f-217">**VFT2\_UNKNOWN**</span></span>                 | <span data-ttu-id="3de0f-218">驅動程式類型未知。</span><span class="sxs-lookup"><span data-stu-id="3de0f-218">Driver type is unknown.</span></span>                   |
| <span data-ttu-id="3de0f-219">**VFT2 \_ Winspool.drv \_ 通訊**</span><span class="sxs-lookup"><span data-stu-id="3de0f-219">**VFT2\_DRV\_COMM**</span></span>               | <span data-ttu-id="3de0f-220">檔案包含通訊驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-220">File contains a communications driver.</span></span>    |
| <span data-ttu-id="3de0f-221">**VFT2 \_ Winspool.drv \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="3de0f-221">**VFT2\_DRV\_PRINTER**</span></span>            | <span data-ttu-id="3de0f-222">檔案包含印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-222">File contains a printer driver.</span></span>           |
| <span data-ttu-id="3de0f-223">**VFT2 \_ Winspool.drv \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="3de0f-223">**VFT2\_DRV\_KEYBOARD**</span></span>           | <span data-ttu-id="3de0f-224">檔案包含鍵盤驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-224">File contains a keyboard driver.</span></span>          |
| <span data-ttu-id="3de0f-225">**VFT2 \_ Winspool.drv \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="3de0f-225">**VFT2\_DRV\_LANGUAGE**</span></span>           | <span data-ttu-id="3de0f-226">檔案包含語言驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-226">File contains a language driver.</span></span>          |
| <span data-ttu-id="3de0f-227">**VFT2 \_ Winspool.drv \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="3de0f-227">**VFT2\_DRV\_DISPLAY**</span></span>            | <span data-ttu-id="3de0f-228">檔案包含顯示驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-228">File contains a display driver.</span></span>           |
| <span data-ttu-id="3de0f-229">**VFT2 \_ Winspool.drv \_ 滑鼠**</span><span class="sxs-lookup"><span data-stu-id="3de0f-229">**VFT2\_DRV\_MOUSE**</span></span>              | <span data-ttu-id="3de0f-230">檔案包含滑鼠驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-230">File contains a mouse driver.</span></span>             |
| <span data-ttu-id="3de0f-231">**VFT2 \_ Winspool.drv \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="3de0f-231">**VFT2\_DRV\_NETWORK**</span></span>            | <span data-ttu-id="3de0f-232">檔案包含網路驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-232">File contains a network driver.</span></span>           |
| <span data-ttu-id="3de0f-233">**VFT2 \_ Winspool.drv \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="3de0f-233">**VFT2\_DRV\_SYSTEM**</span></span>             | <span data-ttu-id="3de0f-234">檔案包含系統驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-234">File contains a system driver.</span></span>            |
| <span data-ttu-id="3de0f-235">**VFT2 \_ winspool.drv 可 \_ 安裝**</span><span class="sxs-lookup"><span data-stu-id="3de0f-235">**VFT2\_DRV\_INSTALLABLE**</span></span>        | <span data-ttu-id="3de0f-236">檔案包含可安裝的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-236">File contains an installable driver.</span></span>      |
| <span data-ttu-id="3de0f-237">**VFT2 \_ Winspool.drv \_ 音效**</span><span class="sxs-lookup"><span data-stu-id="3de0f-237">**VFT2\_DRV\_SOUND**</span></span>              | <span data-ttu-id="3de0f-238">檔案包含音效驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-238">File contains a sound driver.</span></span>             |
| <span data-ttu-id="3de0f-239">**VFT2 \_ Winspool.drv \_ 版本的 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="3de0f-239">**VFT2\_DRV\_VERSIONED\_PRINTER**</span></span> | <span data-ttu-id="3de0f-240">檔案包含已建立版本的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3de0f-240">File contains a versioned printer driver.</span></span> |



 

<span data-ttu-id="3de0f-241">如果資料 *類型* 指定 **VFT \_ 字型**，則此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3de0f-241">If *filetype* specifies **VFT\_FONT**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="3de0f-242">值</span><span class="sxs-lookup"><span data-stu-id="3de0f-242">Value</span></span>                    | <span data-ttu-id="3de0f-243">描述</span><span class="sxs-lookup"><span data-stu-id="3de0f-243">Description</span></span>                    |
|--------------------------|--------------------------------|
| <span data-ttu-id="3de0f-244">**VFT2 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="3de0f-244">**VFT2\_UNKNOWN**</span></span>        | <span data-ttu-id="3de0f-245">字型類型未知。</span><span class="sxs-lookup"><span data-stu-id="3de0f-245">Font type is unknown.</span></span>          |
| <span data-ttu-id="3de0f-246">**VFT2 \_ 字型 \_ 點陣**</span><span class="sxs-lookup"><span data-stu-id="3de0f-246">**VFT2\_FONT\_RASTER**</span></span>   | <span data-ttu-id="3de0f-247">檔案包含點陣字型。</span><span class="sxs-lookup"><span data-stu-id="3de0f-247">File contains a raster font.</span></span>   |
| <span data-ttu-id="3de0f-248">**VFT2 \_ 字型 \_ 向量**</span><span class="sxs-lookup"><span data-stu-id="3de0f-248">**VFT2\_FONT\_VECTOR**</span></span>   | <span data-ttu-id="3de0f-249">檔案包含向量字型。</span><span class="sxs-lookup"><span data-stu-id="3de0f-249">File contains a vector font.</span></span>   |
| <span data-ttu-id="3de0f-250">**VFT2 \_ 字型 \_ TRUETYPE**</span><span class="sxs-lookup"><span data-stu-id="3de0f-250">**VFT2\_FONT\_TRUETYPE**</span></span> | <span data-ttu-id="3de0f-251">檔案包含 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="3de0f-251">File contains a TrueType font.</span></span> |



 

<span data-ttu-id="3de0f-252">如果資料 *類型* 指定 VFT \_ VXD，則此參數必須是虛擬裝置控制區塊中包含的虛擬裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="3de0f-252">If *filetype* specifies VFT\_VXD, this parameter must be the virtual-device identifier included in the virtual-device control block.</span></span>

<span data-ttu-id="3de0f-253">此處未列出的所有 *子類型* 值都是保留給 Microsoft 使用。</span><span class="sxs-lookup"><span data-stu-id="3de0f-253">All *subtype* values not listed here are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="3de0f-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="3de0f-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-255">下列其中一種語言代碼。</span><span class="sxs-lookup"><span data-stu-id="3de0f-255">One of the following language codes.</span></span>



| <span data-ttu-id="3de0f-256">程式碼</span><span class="sxs-lookup"><span data-stu-id="3de0f-256">Code</span></span>   | <span data-ttu-id="3de0f-257">語言</span><span class="sxs-lookup"><span data-stu-id="3de0f-257">Language</span></span>            | <span data-ttu-id="3de0f-258">程式碼</span><span class="sxs-lookup"><span data-stu-id="3de0f-258">Code</span></span>   | <span data-ttu-id="3de0f-259">語言</span><span class="sxs-lookup"><span data-stu-id="3de0f-259">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="3de0f-260">0x0401</span><span class="sxs-lookup"><span data-stu-id="3de0f-260">0x0401</span></span> | <span data-ttu-id="3de0f-261">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="3de0f-261">Arabic</span></span>              | <span data-ttu-id="3de0f-262">0x0415</span><span class="sxs-lookup"><span data-stu-id="3de0f-262">0x0415</span></span> | <span data-ttu-id="3de0f-263">波蘭文</span><span class="sxs-lookup"><span data-stu-id="3de0f-263">Polish</span></span>                    |
| <span data-ttu-id="3de0f-264">0x0402</span><span class="sxs-lookup"><span data-stu-id="3de0f-264">0x0402</span></span> | <span data-ttu-id="3de0f-265">保加利亞文</span><span class="sxs-lookup"><span data-stu-id="3de0f-265">Bulgarian</span></span>           | <span data-ttu-id="3de0f-266">0x0416</span><span class="sxs-lookup"><span data-stu-id="3de0f-266">0x0416</span></span> | <span data-ttu-id="3de0f-267">葡萄牙文 (巴西)</span><span class="sxs-lookup"><span data-stu-id="3de0f-267">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="3de0f-268">0x0403</span><span class="sxs-lookup"><span data-stu-id="3de0f-268">0x0403</span></span> | <span data-ttu-id="3de0f-269">卡達隆尼亞文</span><span class="sxs-lookup"><span data-stu-id="3de0f-269">Catalan</span></span>             | <span data-ttu-id="3de0f-270">0x0417</span><span class="sxs-lookup"><span data-stu-id="3de0f-270">0x0417</span></span> | <span data-ttu-id="3de0f-271">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="3de0f-271">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="3de0f-272">0x0404</span><span class="sxs-lookup"><span data-stu-id="3de0f-272">0x0404</span></span> | <span data-ttu-id="3de0f-273">繁體中文</span><span class="sxs-lookup"><span data-stu-id="3de0f-273">Traditional Chinese</span></span> | <span data-ttu-id="3de0f-274">0x0418</span><span class="sxs-lookup"><span data-stu-id="3de0f-274">0x0418</span></span> | <span data-ttu-id="3de0f-275">羅馬尼亞文</span><span class="sxs-lookup"><span data-stu-id="3de0f-275">Romanian</span></span>                  |
| <span data-ttu-id="3de0f-276">0x0405</span><span class="sxs-lookup"><span data-stu-id="3de0f-276">0x0405</span></span> | <span data-ttu-id="3de0f-277">捷克文</span><span class="sxs-lookup"><span data-stu-id="3de0f-277">Czech</span></span>               | <span data-ttu-id="3de0f-278">0x0419</span><span class="sxs-lookup"><span data-stu-id="3de0f-278">0x0419</span></span> | <span data-ttu-id="3de0f-279">俄文</span><span class="sxs-lookup"><span data-stu-id="3de0f-279">Russian</span></span>                   |
| <span data-ttu-id="3de0f-280">0x0406</span><span class="sxs-lookup"><span data-stu-id="3de0f-280">0x0406</span></span> | <span data-ttu-id="3de0f-281">丹麥文</span><span class="sxs-lookup"><span data-stu-id="3de0f-281">Danish</span></span>              | <span data-ttu-id="3de0f-282">0x041A</span><span class="sxs-lookup"><span data-stu-id="3de0f-282">0x041A</span></span> | <span data-ttu-id="3de0f-283">Croato-Serbian (拉丁) </span><span class="sxs-lookup"><span data-stu-id="3de0f-283">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="3de0f-284">0x0407</span><span class="sxs-lookup"><span data-stu-id="3de0f-284">0x0407</span></span> | <span data-ttu-id="3de0f-285">德文</span><span class="sxs-lookup"><span data-stu-id="3de0f-285">German</span></span>              | <span data-ttu-id="3de0f-286">0x041B</span><span class="sxs-lookup"><span data-stu-id="3de0f-286">0x041B</span></span> | <span data-ttu-id="3de0f-287">斯洛伐克文</span><span class="sxs-lookup"><span data-stu-id="3de0f-287">Slovak</span></span>                    |
| <span data-ttu-id="3de0f-288">0x0408</span><span class="sxs-lookup"><span data-stu-id="3de0f-288">0x0408</span></span> | <span data-ttu-id="3de0f-289">希臘文</span><span class="sxs-lookup"><span data-stu-id="3de0f-289">Greek</span></span>               | <span data-ttu-id="3de0f-290">0x041C</span><span class="sxs-lookup"><span data-stu-id="3de0f-290">0x041C</span></span> | <span data-ttu-id="3de0f-291">阿爾巴尼亞文</span><span class="sxs-lookup"><span data-stu-id="3de0f-291">Albanian</span></span>                  |
| <span data-ttu-id="3de0f-292">0x0409</span><span class="sxs-lookup"><span data-stu-id="3de0f-292">0x0409</span></span> | <span data-ttu-id="3de0f-293">美式英文</span><span class="sxs-lookup"><span data-stu-id="3de0f-293">U.S. English</span></span>        | <span data-ttu-id="3de0f-294">0x041D</span><span class="sxs-lookup"><span data-stu-id="3de0f-294">0x041D</span></span> | <span data-ttu-id="3de0f-295">瑞典文</span><span class="sxs-lookup"><span data-stu-id="3de0f-295">Swedish</span></span>                   |
| <span data-ttu-id="3de0f-296">0x040A</span><span class="sxs-lookup"><span data-stu-id="3de0f-296">0x040A</span></span> | <span data-ttu-id="3de0f-297">標準西班牙文</span><span class="sxs-lookup"><span data-stu-id="3de0f-297">Castilian Spanish</span></span>   | <span data-ttu-id="3de0f-298">0x041E</span><span class="sxs-lookup"><span data-stu-id="3de0f-298">0x041E</span></span> | <span data-ttu-id="3de0f-299">泰文</span><span class="sxs-lookup"><span data-stu-id="3de0f-299">Thai</span></span>                      |
| <span data-ttu-id="3de0f-300">0x040B</span><span class="sxs-lookup"><span data-stu-id="3de0f-300">0x040B</span></span> | <span data-ttu-id="3de0f-301">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="3de0f-301">Finnish</span></span>             | <span data-ttu-id="3de0f-302">0x041F</span><span class="sxs-lookup"><span data-stu-id="3de0f-302">0x041F</span></span> | <span data-ttu-id="3de0f-303">土耳其文</span><span class="sxs-lookup"><span data-stu-id="3de0f-303">Turkish</span></span>                   |
| <span data-ttu-id="3de0f-304">0x040C</span><span class="sxs-lookup"><span data-stu-id="3de0f-304">0x040C</span></span> | <span data-ttu-id="3de0f-305">法文</span><span class="sxs-lookup"><span data-stu-id="3de0f-305">French</span></span>              | <span data-ttu-id="3de0f-306">0x0420</span><span class="sxs-lookup"><span data-stu-id="3de0f-306">0x0420</span></span> | <span data-ttu-id="3de0f-307">烏都文</span><span class="sxs-lookup"><span data-stu-id="3de0f-307">Urdu</span></span>                      |
| <span data-ttu-id="3de0f-308">0x040D</span><span class="sxs-lookup"><span data-stu-id="3de0f-308">0x040D</span></span> | <span data-ttu-id="3de0f-309">Hebrew</span><span class="sxs-lookup"><span data-stu-id="3de0f-309">Hebrew</span></span>              | <span data-ttu-id="3de0f-310">0x0421</span><span class="sxs-lookup"><span data-stu-id="3de0f-310">0x0421</span></span> | <span data-ttu-id="3de0f-311">Bahasa</span><span class="sxs-lookup"><span data-stu-id="3de0f-311">Bahasa</span></span>                    |
| <span data-ttu-id="3de0f-312">0x040E</span><span class="sxs-lookup"><span data-stu-id="3de0f-312">0x040E</span></span> | <span data-ttu-id="3de0f-313">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="3de0f-313">Hungarian</span></span>           | <span data-ttu-id="3de0f-314">0x0804</span><span class="sxs-lookup"><span data-stu-id="3de0f-314">0x0804</span></span> | <span data-ttu-id="3de0f-315">簡體中文</span><span class="sxs-lookup"><span data-stu-id="3de0f-315">Simplified Chinese</span></span>        |
| <span data-ttu-id="3de0f-316">0x040F</span><span class="sxs-lookup"><span data-stu-id="3de0f-316">0x040F</span></span> | <span data-ttu-id="3de0f-317">冰島文</span><span class="sxs-lookup"><span data-stu-id="3de0f-317">Icelandic</span></span>           | <span data-ttu-id="3de0f-318">0x0807</span><span class="sxs-lookup"><span data-stu-id="3de0f-318">0x0807</span></span> | <span data-ttu-id="3de0f-319">瑞士德文</span><span class="sxs-lookup"><span data-stu-id="3de0f-319">Swiss German</span></span>              |
| <span data-ttu-id="3de0f-320">0x0410</span><span class="sxs-lookup"><span data-stu-id="3de0f-320">0x0410</span></span> | <span data-ttu-id="3de0f-321">義大利文</span><span class="sxs-lookup"><span data-stu-id="3de0f-321">Italian</span></span>             | <span data-ttu-id="3de0f-322">0x0809</span><span class="sxs-lookup"><span data-stu-id="3de0f-322">0x0809</span></span> | <span data-ttu-id="3de0f-323">英國。</span><span class="sxs-lookup"><span data-stu-id="3de0f-323">U.K.</span></span> <span data-ttu-id="3de0f-324">英文</span><span class="sxs-lookup"><span data-stu-id="3de0f-324">English</span></span>              |
| <span data-ttu-id="3de0f-325">0x0411</span><span class="sxs-lookup"><span data-stu-id="3de0f-325">0x0411</span></span> | <span data-ttu-id="3de0f-326">日文</span><span class="sxs-lookup"><span data-stu-id="3de0f-326">Japanese</span></span>            | <span data-ttu-id="3de0f-327">0x080A</span><span class="sxs-lookup"><span data-stu-id="3de0f-327">0x080A</span></span> | <span data-ttu-id="3de0f-328">西班牙文 (墨西哥)</span><span class="sxs-lookup"><span data-stu-id="3de0f-328">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="3de0f-329">0x0412</span><span class="sxs-lookup"><span data-stu-id="3de0f-329">0x0412</span></span> | <span data-ttu-id="3de0f-330">韓文</span><span class="sxs-lookup"><span data-stu-id="3de0f-330">Korean</span></span>              | <span data-ttu-id="3de0f-331">0x080C</span><span class="sxs-lookup"><span data-stu-id="3de0f-331">0x080C</span></span> | <span data-ttu-id="3de0f-332">比利時法文</span><span class="sxs-lookup"><span data-stu-id="3de0f-332">Belgian French</span></span>            |
| <span data-ttu-id="3de0f-333">0x0413</span><span class="sxs-lookup"><span data-stu-id="3de0f-333">0x0413</span></span> | <span data-ttu-id="3de0f-334">荷蘭文</span><span class="sxs-lookup"><span data-stu-id="3de0f-334">Dutch</span></span>               | <span data-ttu-id="3de0f-335">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="3de0f-335">0x0C0C</span></span> | <span data-ttu-id="3de0f-336">法文 (加拿大)</span><span class="sxs-lookup"><span data-stu-id="3de0f-336">Canadian French</span></span>           |
| <span data-ttu-id="3de0f-337">0x0414</span><span class="sxs-lookup"><span data-stu-id="3de0f-337">0x0414</span></span> | <span data-ttu-id="3de0f-338">挪威語？</span><span class="sxs-lookup"><span data-stu-id="3de0f-338">Norwegian ?</span></span> <span data-ttu-id="3de0f-339">博克</span><span class="sxs-lookup"><span data-stu-id="3de0f-339">Bokmal</span></span>  | <span data-ttu-id="3de0f-340">0x100C</span><span class="sxs-lookup"><span data-stu-id="3de0f-340">0x100C</span></span> | <span data-ttu-id="3de0f-341">瑞士法文</span><span class="sxs-lookup"><span data-stu-id="3de0f-341">Swiss French</span></span>              |
| <span data-ttu-id="3de0f-342">0x0810</span><span class="sxs-lookup"><span data-stu-id="3de0f-342">0x0810</span></span> | <span data-ttu-id="3de0f-343">瑞士義大利文</span><span class="sxs-lookup"><span data-stu-id="3de0f-343">Swiss Italian</span></span>       | <span data-ttu-id="3de0f-344">0x0816</span><span class="sxs-lookup"><span data-stu-id="3de0f-344">0x0816</span></span> | <span data-ttu-id="3de0f-345">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="3de0f-345">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="3de0f-346">0x0813</span><span class="sxs-lookup"><span data-stu-id="3de0f-346">0x0813</span></span> | <span data-ttu-id="3de0f-347">比利時荷蘭文</span><span class="sxs-lookup"><span data-stu-id="3de0f-347">Belgian Dutch</span></span>       | <span data-ttu-id="3de0f-348">0x081A</span><span class="sxs-lookup"><span data-stu-id="3de0f-348">0x081A</span></span> | <span data-ttu-id="3de0f-349">Serbo-Croatian (斯拉夫) </span><span class="sxs-lookup"><span data-stu-id="3de0f-349">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="3de0f-350">0x0814</span><span class="sxs-lookup"><span data-stu-id="3de0f-350">0x0814</span></span> | <span data-ttu-id="3de0f-351">挪威語？</span><span class="sxs-lookup"><span data-stu-id="3de0f-351">Norwegian ?</span></span> <span data-ttu-id="3de0f-352">耐諾斯克</span><span class="sxs-lookup"><span data-stu-id="3de0f-352">Nynorsk</span></span> |        |                           |



 

</dd> <dt>

<span data-ttu-id="3de0f-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="3de0f-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-354">下列其中一個字元集識別碼。</span><span class="sxs-lookup"><span data-stu-id="3de0f-354">One of the following character-set identifiers.</span></span>



| <span data-ttu-id="3de0f-355">Decimal</span><span class="sxs-lookup"><span data-stu-id="3de0f-355">Decimal</span></span> | <span data-ttu-id="3de0f-356">十六進位</span><span class="sxs-lookup"><span data-stu-id="3de0f-356">Hexadecimal</span></span> | <span data-ttu-id="3de0f-357">字元集</span><span class="sxs-lookup"><span data-stu-id="3de0f-357">Character Set</span></span>              |
|---------|-------------|----------------------------|
| <span data-ttu-id="3de0f-358">0</span><span class="sxs-lookup"><span data-stu-id="3de0f-358">0</span></span>       | <span data-ttu-id="3de0f-359">0000</span><span class="sxs-lookup"><span data-stu-id="3de0f-359">0000</span></span>        | <span data-ttu-id="3de0f-360">7位 ASCII</span><span class="sxs-lookup"><span data-stu-id="3de0f-360">7-bit ASCII</span></span>                |
| <span data-ttu-id="3de0f-361">932</span><span class="sxs-lookup"><span data-stu-id="3de0f-361">932</span></span>     | <span data-ttu-id="3de0f-362">03A4</span><span class="sxs-lookup"><span data-stu-id="3de0f-362">03A4</span></span>        | <span data-ttu-id="3de0f-363">日本 (Shift？</span><span class="sxs-lookup"><span data-stu-id="3de0f-363">Japan (Shift ?</span></span> <span data-ttu-id="3de0f-364">JIS X-0208) </span><span class="sxs-lookup"><span data-stu-id="3de0f-364">JIS X-0208)</span></span> |
| <span data-ttu-id="3de0f-365">949</span><span class="sxs-lookup"><span data-stu-id="3de0f-365">949</span></span>     | <span data-ttu-id="3de0f-366">03B5</span><span class="sxs-lookup"><span data-stu-id="3de0f-366">03B5</span></span>        | <span data-ttu-id="3de0f-367">韓國 (Shift？</span><span class="sxs-lookup"><span data-stu-id="3de0f-367">Korea (Shift ?</span></span> <span data-ttu-id="3de0f-368">KSC 5601) </span><span class="sxs-lookup"><span data-stu-id="3de0f-368">KSC 5601)</span></span>   |
| <span data-ttu-id="3de0f-369">950</span><span class="sxs-lookup"><span data-stu-id="3de0f-369">950</span></span>     | <span data-ttu-id="3de0f-370">03B6</span><span class="sxs-lookup"><span data-stu-id="3de0f-370">03B6</span></span>        | <span data-ttu-id="3de0f-371">臺灣 (Big5) </span><span class="sxs-lookup"><span data-stu-id="3de0f-371">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="3de0f-372">1200</span><span class="sxs-lookup"><span data-stu-id="3de0f-372">1200</span></span>    | <span data-ttu-id="3de0f-373">04B0</span><span class="sxs-lookup"><span data-stu-id="3de0f-373">04B0</span></span>        | <span data-ttu-id="3de0f-374">Unicode</span><span class="sxs-lookup"><span data-stu-id="3de0f-374">Unicode</span></span>                    |
| <span data-ttu-id="3de0f-375">1250</span><span class="sxs-lookup"><span data-stu-id="3de0f-375">1250</span></span>    | <span data-ttu-id="3de0f-376">04E2</span><span class="sxs-lookup"><span data-stu-id="3de0f-376">04E2</span></span>        | <span data-ttu-id="3de0f-377">拉丁美洲 (東部歐洲) </span><span class="sxs-lookup"><span data-stu-id="3de0f-377">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="3de0f-378">1251</span><span class="sxs-lookup"><span data-stu-id="3de0f-378">1251</span></span>    | <span data-ttu-id="3de0f-379">04E3</span><span class="sxs-lookup"><span data-stu-id="3de0f-379">04E3</span></span>        | <span data-ttu-id="3de0f-380">古斯拉夫文</span><span class="sxs-lookup"><span data-stu-id="3de0f-380">Cyrillic</span></span>                   |
| <span data-ttu-id="3de0f-381">1252</span><span class="sxs-lookup"><span data-stu-id="3de0f-381">1252</span></span>    | <span data-ttu-id="3de0f-382">04E4</span><span class="sxs-lookup"><span data-stu-id="3de0f-382">04E4</span></span>        | <span data-ttu-id="3de0f-383">多 語種</span><span class="sxs-lookup"><span data-stu-id="3de0f-383">Multilingual</span></span>               |
| <span data-ttu-id="3de0f-384">1253</span><span class="sxs-lookup"><span data-stu-id="3de0f-384">1253</span></span>    | <span data-ttu-id="3de0f-385">04E5</span><span class="sxs-lookup"><span data-stu-id="3de0f-385">04E5</span></span>        | <span data-ttu-id="3de0f-386">希臘文</span><span class="sxs-lookup"><span data-stu-id="3de0f-386">Greek</span></span>                      |
| <span data-ttu-id="3de0f-387">1254</span><span class="sxs-lookup"><span data-stu-id="3de0f-387">1254</span></span>    | <span data-ttu-id="3de0f-388">04E6</span><span class="sxs-lookup"><span data-stu-id="3de0f-388">04E6</span></span>        | <span data-ttu-id="3de0f-389">土耳其文</span><span class="sxs-lookup"><span data-stu-id="3de0f-389">Turkish</span></span>                    |
| <span data-ttu-id="3de0f-390">1255</span><span class="sxs-lookup"><span data-stu-id="3de0f-390">1255</span></span>    | <span data-ttu-id="3de0f-391">04E7</span><span class="sxs-lookup"><span data-stu-id="3de0f-391">04E7</span></span>        | <span data-ttu-id="3de0f-392">Hebrew</span><span class="sxs-lookup"><span data-stu-id="3de0f-392">Hebrew</span></span>                     |
| <span data-ttu-id="3de0f-393">1256</span><span class="sxs-lookup"><span data-stu-id="3de0f-393">1256</span></span>    | <span data-ttu-id="3de0f-394">04E8</span><span class="sxs-lookup"><span data-stu-id="3de0f-394">04E8</span></span>        | <span data-ttu-id="3de0f-395">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="3de0f-395">Arabic</span></span>                     |



 

</dd> <dt>

<span data-ttu-id="3de0f-396"><span id="string-name"></span><span id="STRING-NAME"></span>*字串名稱*</span><span class="sxs-lookup"><span data-stu-id="3de0f-396"><span id="string-name"></span><span id="STRING-NAME"></span>*string-name*</span></span>
</dt> <dd>

<span data-ttu-id="3de0f-397">下列其中一個預先定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="3de0f-397">One of the following predefined names.</span></span>



| <span data-ttu-id="3de0f-398">Name</span><span class="sxs-lookup"><span data-stu-id="3de0f-398">Name</span></span>                 | <span data-ttu-id="3de0f-399">描述</span><span class="sxs-lookup"><span data-stu-id="3de0f-399">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de0f-400">**註解**</span><span class="sxs-lookup"><span data-stu-id="3de0f-400">**Comments**</span></span>         | <span data-ttu-id="3de0f-401">為了診斷而應顯示的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="3de0f-401">Additional information that should be displayed for diagnostic purposes.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="3de0f-402">**CompanyName**</span><span class="sxs-lookup"><span data-stu-id="3de0f-402">**CompanyName**</span></span>      | <span data-ttu-id="3de0f-403">產生檔案的公司，例如「Microsoft Corporation」或「標準 Microsystems Corporation，Inc.」。</span><span class="sxs-lookup"><span data-stu-id="3de0f-403">Company that produced the file?for example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span> <span data-ttu-id="3de0f-404">這個字串是必要的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-404">This string is required.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="3de0f-405">**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="3de0f-405">**FileDescription**</span></span>  | <span data-ttu-id="3de0f-406">要呈現給使用者的檔案描述。</span><span class="sxs-lookup"><span data-stu-id="3de0f-406">File description to be presented to users.</span></span> <span data-ttu-id="3de0f-407">當使用者選擇要安裝的檔案時，此字串可能會顯示在清單方塊中（例如，「AT-Style 鍵盤的鍵盤驅動程式」）。</span><span class="sxs-lookup"><span data-stu-id="3de0f-407">This string may be displayed in a list box when the user is choosing files to install?for example, "Keyboard Driver for AT-Style Keyboards".</span></span> <span data-ttu-id="3de0f-408">這個字串是必要的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-408">This string is required.</span></span>                                                                                            |
| <span data-ttu-id="3de0f-409">**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="3de0f-409">**FileVersion**</span></span>      | <span data-ttu-id="3de0f-410">檔案的版本號碼，例如 "3.10" 或 "5.00. RC2"。</span><span class="sxs-lookup"><span data-stu-id="3de0f-410">Version number of the file?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="3de0f-411">這個字串是必要的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-411">This string is required.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="3de0f-412">**InternalName**</span><span class="sxs-lookup"><span data-stu-id="3de0f-412">**InternalName**</span></span>     | <span data-ttu-id="3de0f-413">檔案的內部名稱（如果有的話）？例如，如果檔案是動態連結程式庫，則為模組名稱。</span><span class="sxs-lookup"><span data-stu-id="3de0f-413">Internal name of the file, if one exists?for example, a module name if the file is a dynamic-link library.</span></span> <span data-ttu-id="3de0f-414">如果檔案沒有內部名稱，此字串應該是不含副檔名的原始檔案名。</span><span class="sxs-lookup"><span data-stu-id="3de0f-414">If the file has no internal name, this string should be the original filename, without extension.</span></span> <span data-ttu-id="3de0f-415">這個字串是必要的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-415">This string is required.</span></span>                                                                       |
| <span data-ttu-id="3de0f-416">**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="3de0f-416">**LegalCopyright**</span></span>   | <span data-ttu-id="3de0f-417">適用于檔案的著作權注意事項。</span><span class="sxs-lookup"><span data-stu-id="3de0f-417">Copyright notices that apply to the file.</span></span> <span data-ttu-id="3de0f-418">這應該包含所有通知、法律符號、著作權日期等的完整文字。</span><span class="sxs-lookup"><span data-stu-id="3de0f-418">This should include the full text of all notices, legal symbols, copyright dates, and so on.</span></span> <span data-ttu-id="3de0f-419">這個字串是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-419">This string is optional.</span></span>                                                                                                                                             |
| <span data-ttu-id="3de0f-420">**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="3de0f-420">**LegalTrademarks**</span></span>  | <span data-ttu-id="3de0f-421">適用于檔案的商標及注冊商標。</span><span class="sxs-lookup"><span data-stu-id="3de0f-421">Trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="3de0f-422">這應包括所有注意事項全文、法律符號、商標登錄編號等等。</span><span class="sxs-lookup"><span data-stu-id="3de0f-422">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="3de0f-423">這個字串是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-423">This string is optional.</span></span>                                                                                                                        |
| <span data-ttu-id="3de0f-424">**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="3de0f-424">**OriginalFilename**</span></span> | <span data-ttu-id="3de0f-425">檔案的原始名稱，不包含路徑。</span><span class="sxs-lookup"><span data-stu-id="3de0f-425">Original name of the file, not including a path.</span></span> <span data-ttu-id="3de0f-426">這項資訊可讓應用程式判斷使用者是否已重新命名檔案。</span><span class="sxs-lookup"><span data-stu-id="3de0f-426">This information enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="3de0f-427">名稱的格式取決於建立檔案的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="3de0f-427">The format of the name depends on the file system for which the file was created.</span></span> <span data-ttu-id="3de0f-428">這個字串是必要的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-428">This string is required.</span></span>                                                 |
| <span data-ttu-id="3de0f-429">**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="3de0f-429">**PrivateBuild**</span></span>     | <span data-ttu-id="3de0f-430">檔案私用版本的相關資訊，例如「在 TESTBED 上由 TESTER1 建立」 \\ 。</span><span class="sxs-lookup"><span data-stu-id="3de0f-430">Information about a private version of the file?for example, "Built by TESTER1 on \\TESTBED".</span></span> <span data-ttu-id="3de0f-431">只有當 **VS \_ FF \_ PRI加值稅EBUILD** 是在根區塊的 *fileflags 機碼* 參數中指定時，才會出現這個字串。</span><span class="sxs-lookup"><span data-stu-id="3de0f-431">This string should be present only if **VS\_FF\_PRIVATEBUILD** is specified in the *fileflags* parameter of the root block.</span></span>                                                                                   |
| <span data-ttu-id="3de0f-432">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="3de0f-432">**ProductName**</span></span>      | <span data-ttu-id="3de0f-433">用來散發檔案的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="3de0f-433">Name of the product with which the file is distributed.</span></span> <span data-ttu-id="3de0f-434">這個字串是必要的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-434">This string is required.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="3de0f-435">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="3de0f-435">**ProductVersion**</span></span>   | <span data-ttu-id="3de0f-436">散發檔案時所使用的產品版本（例如 "3.10" 或 "5.00. RC2"）。</span><span class="sxs-lookup"><span data-stu-id="3de0f-436">Version of the product with which the file is distributed?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="3de0f-437">這個字串是必要的。</span><span class="sxs-lookup"><span data-stu-id="3de0f-437">This string is required.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="3de0f-438">**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="3de0f-438">**SpecialBuild**</span></span>     | <span data-ttu-id="3de0f-439">指出此檔案版本與標準版本有何差異的文字（例如「TESTER1 在 M250 和 M250E 電腦上解決滑鼠問題的私用組建」）。</span><span class="sxs-lookup"><span data-stu-id="3de0f-439">Text that indicates how this version of the file differs from the standard version?for example, "Private build for TESTER1 solving mouse problems on M250 and M250E computers".</span></span> <span data-ttu-id="3de0f-440">只有當 **VS \_ FF \_ SPECIALBUILD** 是在根區塊的 *fileflags 機碼* 參數中指定時，才會出現這個字串。</span><span class="sxs-lookup"><span data-stu-id="3de0f-440">This string should be present only if **VS\_FF\_SPECIALBUILD** is specified in the *fileflags* parameter of the root block.</span></span> |



 

</dd> </dl>

<span data-ttu-id="3de0f-441">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="3de0f-441">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3de0f-442">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="3de0f-442">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3de0f-443">範例</span><span class="sxs-lookup"><span data-stu-id="3de0f-443">Examples</span></span>

<span data-ttu-id="3de0f-444">下列範例會定義 **VERSIONINFO** 資源：</span><span class="sxs-lookup"><span data-stu-id="3de0f-444">The following example defines a **VERSIONINFO** resource:</span></span>

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a><span data-ttu-id="3de0f-445">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de0f-445">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de0f-446">使用版本資訊</span><span class="sxs-lookup"><span data-stu-id="3de0f-446">Using Version Information</span></span>](./using-version-information.md)
</dt> <dt>

[<span data-ttu-id="3de0f-447">版本資訊</span><span class="sxs-lookup"><span data-stu-id="3de0f-447">Version Information</span></span>](./version-information.md)
</dt> </dl>

 

 