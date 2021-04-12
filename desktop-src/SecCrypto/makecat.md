---
description: 建立類別目錄檔案的 CryptoAPI 工具。
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848153"
---
# <a name="makecat"></a><span data-ttu-id="34dd1-103">MakeCat</span><span class="sxs-lookup"><span data-stu-id="34dd1-103">MakeCat</span></span>

<span data-ttu-id="34dd1-104">MakeCat 工具是用來建立類別目錄檔案的 CryptoAPI 工具。</span><span class="sxs-lookup"><span data-stu-id="34dd1-104">The MakeCat tool is a CryptoAPI tool that creates a catalog file.</span></span> <span data-ttu-id="34dd1-105">MakeCat 適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK) 的一部分，預設會安裝在 \\ SDK 安裝路徑的 Bin 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="34dd1-105">MakeCat is available as part of the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 and is installed, by default, in the \\Bin folder of the SDK installation path.</span></span>

<span data-ttu-id="34dd1-106">MakeCat 工具會使用下列命令語法：</span><span class="sxs-lookup"><span data-stu-id="34dd1-106">The MakeCat tool uses the following command syntax:</span></span>

<span data-ttu-id="34dd1-107">**MakeCat** \[**-n** \|**-r** \|**-v** \]*檔案名*</span><span class="sxs-lookup"><span data-stu-id="34dd1-107">**MakeCat** \[**-n**\|**-r**\|**-v**\] *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="34dd1-108">參數</span><span class="sxs-lookup"><span data-stu-id="34dd1-108">Parameters</span></span>



| <span data-ttu-id="34dd1-109">參數</span><span class="sxs-lookup"><span data-stu-id="34dd1-109">Parameter</span></span>             | <span data-ttu-id="34dd1-110">描述</span><span class="sxs-lookup"><span data-stu-id="34dd1-110">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34dd1-111">**-n**</span><span class="sxs-lookup"><span data-stu-id="34dd1-111">**-n**</span></span><br/>     | <span data-ttu-id="34dd1-112">請勿在可復原的錯誤上停止。</span><span class="sxs-lookup"><span data-stu-id="34dd1-112">Do not stop on a recoverable error.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="34dd1-113">**-r**</span><span class="sxs-lookup"><span data-stu-id="34dd1-113">**-r**</span></span><br/>     | <span data-ttu-id="34dd1-114">如果遇到可復原的錯誤，則強制 MakeCat 結束。</span><span class="sxs-lookup"><span data-stu-id="34dd1-114">Forces MakeCat to end if it encounters recoverable errors.</span></span> <span data-ttu-id="34dd1-115">具體而言，它會在檔的 [類別目錄檔案] 區段中處理專案時結束。</span><span class="sxs-lookup"><span data-stu-id="34dd1-115">Specifically, it will end when processing the entries in the catalog files section of a .cdf file.</span></span><br/> |
| <span data-ttu-id="34dd1-116">**-v**</span><span class="sxs-lookup"><span data-stu-id="34dd1-116">**-v**</span></span><br/>     | <span data-ttu-id="34dd1-117">詳細。</span><span class="sxs-lookup"><span data-stu-id="34dd1-117">Verbose.</span></span> <span data-ttu-id="34dd1-118">顯示所有進度和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="34dd1-118">Displays all progress and error messages.</span></span><br/>                                                                                                            |
| <span data-ttu-id="34dd1-119">*FileName*</span><span class="sxs-lookup"><span data-stu-id="34dd1-119">*FileName*</span></span><br/> | <span data-ttu-id="34dd1-120">要剖析的 cdf 檔案名。</span><span class="sxs-lookup"><span data-stu-id="34dd1-120">Name of the .cdf file to be parsed.</span></span> <span data-ttu-id="34dd1-121">如需必要的結構和內容，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="34dd1-121">For required structure and contents, see Remarks.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="34dd1-122">備註</span><span class="sxs-lookup"><span data-stu-id="34dd1-122">Remarks</span></span>

<span data-ttu-id="34dd1-123">您必須使用下列規格來建立此 cdf 檔案。</span><span class="sxs-lookup"><span data-stu-id="34dd1-123">The .cdf file must be built with the following specifications.</span></span>

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> <span data-ttu-id="34dd1-124">專案中的最後一個專案必須在行尾必須有明確的分行符號。</span><span class="sxs-lookup"><span data-stu-id="34dd1-124">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

<span data-ttu-id="34dd1-125">\[CatalogHeader \] 區段會定義整個類別目錄檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="34dd1-125">The \[CatalogHeader\] section defines information about the entire catalog file.</span></span>



| <span data-ttu-id="34dd1-126">選項</span><span class="sxs-lookup"><span data-stu-id="34dd1-126">Option</span></span>                    | <span data-ttu-id="34dd1-127">描述</span><span class="sxs-lookup"><span data-stu-id="34dd1-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34dd1-128">Name</span><span class="sxs-lookup"><span data-stu-id="34dd1-128">Name</span></span><br/>           | <span data-ttu-id="34dd1-129">類別目錄檔案的名稱，包括它的副檔名。</span><span class="sxs-lookup"><span data-stu-id="34dd1-129">Name of the catalog file, including its extension.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="34dd1-130">>\dreplayclient\resultdir</span><span class="sxs-lookup"><span data-stu-id="34dd1-130">ResultDir</span></span><br/>      | <span data-ttu-id="34dd1-131">將放置建立之 .cat 檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="34dd1-131">Directory where the created .cat file will be placed.</span></span> <span data-ttu-id="34dd1-132">如果未指定，則會使用預設的目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="34dd1-132">If not indicated, the default current directory is used.</span></span> <span data-ttu-id="34dd1-133">如果目錄不存在，則會建立該目錄。</span><span class="sxs-lookup"><span data-stu-id="34dd1-133">If the directory does not exist, it is created.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="34dd1-134">PublicVersion</span><span class="sxs-lookup"><span data-stu-id="34dd1-134">PublicVersion</span></span><br/>  | <span data-ttu-id="34dd1-135">不支援這個選項。</span><span class="sxs-lookup"><span data-stu-id="34dd1-135">This option is not supported.</span></span> <br/> <span data-ttu-id="34dd1-136">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 目錄版本。</span><span class="sxs-lookup"><span data-stu-id="34dd1-136">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Catalog version.</span></span> <span data-ttu-id="34dd1-137">如果保留空白，則會使用預設值1。</span><span class="sxs-lookup"><span data-stu-id="34dd1-137">If left blank, the default value, 1, is used.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="34dd1-138">CatalogVersion</span><span class="sxs-lookup"><span data-stu-id="34dd1-138">CatalogVersion</span></span><br/> | <span data-ttu-id="34dd1-139">目錄版本。</span><span class="sxs-lookup"><span data-stu-id="34dd1-139">Catalog version.</span></span> <span data-ttu-id="34dd1-140">如果版本不存在或設定為1，則會將 "0x100" 傳遞給 [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)函式的 *dwPublicVersion* 參數，並建立第1版的類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="34dd1-140">If the version is not present or is set to 1, then "0x100" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 1 catalog file is created.</span></span> <span data-ttu-id="34dd1-141">HashAlgorithms 選項必須空白或包含 SHA1。</span><span class="sxs-lookup"><span data-stu-id="34dd1-141">The HashAlgorithms option must be empty or contain SHA1.</span></span><br/> <span data-ttu-id="34dd1-142">如果版本設定為2，則會將 "0x200" 傳遞給 [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)函式的 *dwPublicVersion* 參數，並建立第2版的類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="34dd1-142">If the version is set to 2, then "0x200" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 2 catalog file is created.</span></span> <span data-ttu-id="34dd1-143">HashAlgorithms 選項必須包含 SHA256。</span><span class="sxs-lookup"><span data-stu-id="34dd1-143">The HashAlgorithms option must contain SHA256.</span></span><br/> <span data-ttu-id="34dd1-144">如果這個選項存在，但包含1或2以外的任何值，MakeCat 工具將會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="34dd1-144">If this option is present but contains any value other than 1 or 2, the MakeCat tool will error out.</span></span><br/> <span data-ttu-id="34dd1-145">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援此選項。</span><span class="sxs-lookup"><span data-stu-id="34dd1-145">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/> |
| <span data-ttu-id="34dd1-146">HashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="34dd1-146">HashAlgorithms</span></span><br/> | <span data-ttu-id="34dd1-147">使用的雜湊演算法名稱。</span><span class="sxs-lookup"><span data-stu-id="34dd1-147">Name of the hashing algorithm used.</span></span> <span data-ttu-id="34dd1-148">如需詳細資訊，請參閱 CatalogVersion 選項。</span><span class="sxs-lookup"><span data-stu-id="34dd1-148">For more information, see the CatalogVersion option.</span></span><br/> <span data-ttu-id="34dd1-149">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援此選項。</span><span class="sxs-lookup"><span data-stu-id="34dd1-149">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="34dd1-150">PageHashes</span><span class="sxs-lookup"><span data-stu-id="34dd1-150">PageHashes</span></span><br/>     | <span data-ttu-id="34dd1-151">指定是否將 <HASH> \[ CatalogFiles \] 區段中的選項所列的檔案雜湊</span><span class="sxs-lookup"><span data-stu-id="34dd1-151">Specifies whether to hash the files listed in the <HASH> option in the \[CatalogFiles\] section</span></span><br/> <span data-ttu-id="34dd1-152">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援此選項。</span><span class="sxs-lookup"><span data-stu-id="34dd1-152">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="34dd1-153">EncodingType</span><span class="sxs-lookup"><span data-stu-id="34dd1-153">EncodingType</span></span><br/>   | <span data-ttu-id="34dd1-154">使用的訊息編碼類型。</span><span class="sxs-lookup"><span data-stu-id="34dd1-154">Type of message encoding used.</span></span> <span data-ttu-id="34dd1-155">如果保留空白，預設 Edi.encodingtype 為 PKCS \_ 7 \_ ASN \_ 編碼 \| X509 \_ ASN \_ 編碼，0x00010001。</span><span class="sxs-lookup"><span data-stu-id="34dd1-155">If left blank, the default EncodingType is PKCS\_7\_ASN\_ENCODING \| X509\_ASN\_ENCODING, 0x00010001.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="34dd1-156">\[CatalogFiles \] 區段會定義每個類別目錄檔案的成員，並在不同的群組中包含各種類型的檔案和不同類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="34dd1-156">The \[CatalogFiles\] section defines each member of the catalog file with files of various types and attributes of various types in separate groups.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34dd1-157">選項</span><span class="sxs-lookup"><span data-stu-id="34dd1-157">Option</span></span></th>
<th><span data-ttu-id="34dd1-158">Description</span><span class="sxs-lookup"><span data-stu-id="34dd1-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34dd1-159">參考標記</span><span class="sxs-lookup"><span data-stu-id="34dd1-159">reference tag</span></span><br/></td>
<td><span data-ttu-id="34dd1-160">檔案的文字參考。</span><span class="sxs-lookup"><span data-stu-id="34dd1-160">Text reference to the file.</span></span> <span data-ttu-id="34dd1-161">這可以包含任何 ASCII 文字字元，但等號 (=) 除外。</span><span class="sxs-lookup"><span data-stu-id="34dd1-161">This can include any ASCII text characters except the equal sign (=).</span></span> <span data-ttu-id="34dd1-162">安裝之後，系統必須能夠重現此標記。</span><span class="sxs-lookup"><span data-stu-id="34dd1-162">The system must be able to reproduce this tag after installation.</span></span> <br/> <span data-ttu-id="34dd1-163">用 <HASH> 做檔案名的前置詞。</span><span class="sxs-lookup"><span data-stu-id="34dd1-163">Use <HASH> as a prefix of the file name.</span></span> <span data-ttu-id="34dd1-164">這會導致標記成為 ASCII 字串格式的檔案雜湊。</span><span class="sxs-lookup"><span data-stu-id="34dd1-164">This results in the tag being the file's hash in ASCII string form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34dd1-165">檔案路徑和名稱</span><span class="sxs-lookup"><span data-stu-id="34dd1-165">file path and name</span></span><br/></td>
<td><span data-ttu-id="34dd1-166">檔案名，包括要剖析的副檔名和檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="34dd1-166">The file name, including the extension to be parsed and the relative path to the file.</span></span> <span data-ttu-id="34dd1-167">可使用 SignTool 簽署的任何檔案類型都可以新增至目錄。</span><span class="sxs-lookup"><span data-stu-id="34dd1-167">Any type of file that can be signed with SignTool can be added to a catalog.</span></span> <span data-ttu-id="34dd1-168">例如，具有下列副檔名的檔案名，也可以加入至類別目錄： .exe、.cab、.cat、.ocx、.dll 和 stl 中。</span><span class="sxs-lookup"><span data-stu-id="34dd1-168">For example, file names with the following extensions, among others, can be added to a catalog: .exe, .cab, .cat, .ocx, .dll, and .stl.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34dd1-169">ALTSIPID</span><span class="sxs-lookup"><span data-stu-id="34dd1-169">ALTSIPID</span></span><br/></td>
<td><span data-ttu-id="34dd1-170">用於雜湊的 SIP GUID，而不是根據檔案類型的標準 SIP。</span><span class="sxs-lookup"><span data-stu-id="34dd1-170">SIP GUID that is to be used for hashing instead of the standard SIP based on file type.</span></span> <span data-ttu-id="34dd1-171">這是選用項目。</span><span class="sxs-lookup"><span data-stu-id="34dd1-171">This entry is optional.</span></span> <span data-ttu-id="34dd1-172">如果省略此專案，則會使用預設的 SIP 來雜湊成員。</span><span class="sxs-lookup"><span data-stu-id="34dd1-172">If this entry is omitted, the member will be hashed using the default SIP.</span></span> <span data-ttu-id="34dd1-173">如果找不到預設安裝的 SIP，則會使用一般 SIP。</span><span class="sxs-lookup"><span data-stu-id="34dd1-173">If no default installed SIP is found, the Flat SIP will be used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34dd1-174">guid</span><span class="sxs-lookup"><span data-stu-id="34dd1-174">guid</span></span><br/></td>
<td><span data-ttu-id="34dd1-175">GUID 的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="34dd1-175">Text representation of a GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34dd1-176">ATTRx</span><span class="sxs-lookup"><span data-stu-id="34dd1-176">ATTRx</span></span><br/></td>
<td><span data-ttu-id="34dd1-177">選擇性。</span><span class="sxs-lookup"><span data-stu-id="34dd1-177">Optional.</span></span> <span data-ttu-id="34dd1-178">檔案或內容的相關屬性或語句。</span><span class="sxs-lookup"><span data-stu-id="34dd1-178">Attribute or statement about the file or content.</span></span> <span data-ttu-id="34dd1-179">您可以有任意數目的屬性，包括 none。</span><span class="sxs-lookup"><span data-stu-id="34dd1-179">There can be any number of attributes, including none.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34dd1-180">類型</span><span class="sxs-lookup"><span data-stu-id="34dd1-180">type</span></span><br/></td>
<td><span data-ttu-id="34dd1-181">定義要在格式 0x00000000 (文字) 中加入的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="34dd1-181">Defines what type of attribute is being added in the format 0x00000000 (text).</span></span> <span data-ttu-id="34dd1-182">這個選項可以是零或多個下列值的位<strong>or</strong> 組合：</span><span class="sxs-lookup"><span data-stu-id="34dd1-182">This option can be a bitwise-<strong>OR</strong> combination of zero or more of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="34dd1-183">0x10000000 驗證的屬性 (簽署，包含在雜湊) 中。</span><span class="sxs-lookup"><span data-stu-id="34dd1-183">0x10000000 Authenticated attribute (signed, included in the hash).</span></span></li>
<li><span data-ttu-id="34dd1-184">0x20000000 未驗證的屬性 (不帶正負號，不包含在雜湊中，無法驗證) 。</span><span class="sxs-lookup"><span data-stu-id="34dd1-184">0x20000000 Unauthenticated attribute (unsigned, not included in the hash, not verifiable).</span></span></li>
<li><span data-ttu-id="34dd1-185">0x01000000 屬性不會複寫到 CatalogVersion 2 目錄中的 SHA1 專案。</span><span class="sxs-lookup"><span data-stu-id="34dd1-185">0x01000000 Attribute will not be replicated to SHA1 entries in a CatalogVersion 2 catalog.</span></span></li>
<li><span data-ttu-id="34dd1-186">0x00010000 屬性會以純文字表示。</span><span class="sxs-lookup"><span data-stu-id="34dd1-186">0x00010000 Attribute is represented in plaintext.</span></span> <span data-ttu-id="34dd1-187">不會進行任何轉換。</span><span class="sxs-lookup"><span data-stu-id="34dd1-187">No conversion will be done.</span></span></li>
<li><span data-ttu-id="34dd1-188">0x00020000 屬性以64編碼方式表示。</span><span class="sxs-lookup"><span data-stu-id="34dd1-188">0x00020000 Attribute is represented in base-64 encoding.</span></span> <span data-ttu-id="34dd1-189">這會用來代表二進位資料。</span><span class="sxs-lookup"><span data-stu-id="34dd1-189">This is used to represent binary data.</span></span></li>
<li><span data-ttu-id="34dd1-190">0x00000001 屬性是成對的名稱/值。</span><span class="sxs-lookup"><span data-stu-id="34dd1-190">0x00000001 Attribute is a name-value pair.</span></span> <span data-ttu-id="34dd1-191">針對名稱使用 oid 選項。</span><span class="sxs-lookup"><span data-stu-id="34dd1-191">Use the oid option for the name.</span></span> <span data-ttu-id="34dd1-192">這個屬性很慢;因此，請謹慎使用此選項。</span><span class="sxs-lookup"><span data-stu-id="34dd1-192">This attribute is slow; therefore, use this option sparingly.</span></span></li>
<li><span data-ttu-id="34dd1-193"> (OID) 的 <a href="/windows/desktop/SecGloss/o-gly"><em>物件識別碼</em></a> 參考了0x00000002 屬性。</span><span class="sxs-lookup"><span data-stu-id="34dd1-193">0x00000002 Attribute is referenced by an <a href="/windows/desktop/SecGloss/o-gly"><em>object identifier</em></a> (OID).</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34dd1-194">oid</span><span class="sxs-lookup"><span data-stu-id="34dd1-194">oid</span></span><br/></td>
<td><span data-ttu-id="34dd1-195">屬性參考索引鍵的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="34dd1-195">The text representation of the attribute's reference key.</span></span> <span data-ttu-id="34dd1-196">它是以點符四標記法的文字字串格式的 OID (例如，b.) 或文字名稱。</span><span class="sxs-lookup"><span data-stu-id="34dd1-196">It is an OID in the form of a text string in dotted quad notation (for example, a.b.c.d) or a text Name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34dd1-197">value</span><span class="sxs-lookup"><span data-stu-id="34dd1-197">value</span></span><br/></td>
<td><span data-ttu-id="34dd1-198">屬性值的文字表示。</span><span class="sxs-lookup"><span data-stu-id="34dd1-198">The text representation of the value of the attribute.</span></span> <span data-ttu-id="34dd1-199">使用的文字表示型別取決於 type 選項的值。</span><span class="sxs-lookup"><span data-stu-id="34dd1-199">The type of text representation used depends on the value of the type option.</span></span> <span data-ttu-id="34dd1-200">EOL 字元會決定長度。</span><span class="sxs-lookup"><span data-stu-id="34dd1-200">The EOL characters determine the length.</span></span><br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td><span data-ttu-id="34dd1-201">雜湊指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="34dd1-201">Hashes the specified file.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="34dd1-202">產生的類別目錄檔案未簽署。</span><span class="sxs-lookup"><span data-stu-id="34dd1-202">The generated catalog file is unsigned.</span></span> <span data-ttu-id="34dd1-203">如果要在傳送前簽署，則會使用 [SignTool](signtool.md)進行簽署。</span><span class="sxs-lookup"><span data-stu-id="34dd1-203">If it is to be signed prior to transmittal, it is signed by using [SignTool](signtool.md).</span></span>

 

 
