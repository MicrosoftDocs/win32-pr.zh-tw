---
description: 製作未簽署的類別目錄檔案，其中包含一組檔案的雜湊，以及集合中每個檔案的相關聯屬性。 類別目錄檔案可讓使用者 (目錄簽署一個檔案) ，而不是簽署許多個別的檔案。
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: 使用 MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974958"
---
# <a name="using-makecat"></a><span data-ttu-id="e9e3a-104">使用 MakeCat</span><span class="sxs-lookup"><span data-stu-id="e9e3a-104">Using MakeCat</span></span>

<span data-ttu-id="e9e3a-105">[MakeCat](makecat.md)工具會建立未簽署的類別目錄檔案，其中包含一組檔案的 [*雜湊*](../secgloss/h-gly.md)，以及集合中每個檔案的相關聯屬性。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-105">The [MakeCat](makecat.md) tool makes an unsigned catalog file, which contains the [*hashes*](../secgloss/h-gly.md) of a set of files along with associated attributes of each file in the set.</span></span> <span data-ttu-id="e9e3a-106">類別目錄檔案可讓使用者 (目錄簽署一個檔案) ，而不是簽署許多個別的檔案。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-106">A catalog file allows the user to sign one file (the catalog) instead of signing numerous individual files.</span></span>

<span data-ttu-id="e9e3a-107">簽署並傳輸未簽署的類別目錄檔案之後，接收者可以比較原始檔案的雜湊與目錄檔案中包含的雜湊，並確認檔案不會受到篡改。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-107">After the unsigned catalog file is signed and transmitted, the receiver can compare the hashes of the original files to the hashes contained within the catalog file and verify that the files are free of tampering.</span></span>

<span data-ttu-id="e9e3a-108">在使用 [MakeCat](makecat.md) 工具之前，使用者必須使用任何文字編輯器來準備目錄定義檔 ( 的 cdf) 。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-108">Prior to using the [MakeCat](makecat.md) tool, the user must prepare a Catalog Definition File (.cdf), by using any text editor.</span></span> <span data-ttu-id="e9e3a-109">此 cdf 檔案包含檔案清單以及要編目之檔案的屬性 (下列) 所列的規格。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-109">The .cdf file contains the list of files and the attributes of the files to be cataloged (the specifications are listed below).</span></span> <span data-ttu-id="e9e3a-110">MakeCat 工具會掃描 cdf 檔案、確認每個所列出檔案的屬性清單、將列出的屬性新增至目錄本身、將每個列出的檔案雜湊，然後將每個檔案的雜湊儲存至類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-110">The MakeCat tool scans the .cdf file, verifies the list of attributes of each listed file, adds the listed attributes to the catalog itself, hashes each of the listed files, and stores the hashes of each file into the catalog file.</span></span> <span data-ttu-id="e9e3a-111">每個檔案的雜湊和屬性分別儲存在目錄內。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-111">Each file has its hash and attributes stored separately within the catalog.</span></span> <span data-ttu-id="e9e3a-112">然後可以簽署和傳送此類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-112">This catalog file can then be signed and transmitted.</span></span> <span data-ttu-id="e9e3a-113">接收者接著可以將目錄中每個檔案的雜湊與原始檔案的雜湊進行比較，以證明原始內容完全不會受到篡改。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-113">The receiver can subsequently compare the hash of each file within the catalog with the hash of the original files to prove that the original content is free of tampering.</span></span> <span data-ttu-id="e9e3a-114">MakeCat 不會修改 cdf 檔。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-114">MakeCat does not modify the .cdf file.</span></span>

<span data-ttu-id="e9e3a-115">下列範例會使用 [MakeCat](makecat.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-115">The following examples use [MakeCat](makecat.md) commands.</span></span>

-   <span data-ttu-id="e9e3a-116">從檔案的副檔名產生類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-116">Generate a catalog file from the file Good.cdf.</span></span>

    <span data-ttu-id="e9e3a-117">**MakeCat-v 不錯的 cdf**</span><span class="sxs-lookup"><span data-stu-id="e9e3a-117">**MakeCat -v good.cdf**</span></span>

<span data-ttu-id="e9e3a-118">檔案（cdf）會剖析 UnsignedPE.exe、UnsignedDOS.exe、Unsigned.cab、不帶 SignedPE.exe 正負號的檔案，藉以產生類別目錄檔案 Good.cat。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-118">A file, Good.cdf, produces a catalog file, Good.cat, by parsing the files UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned.Class, and SignedPE.exe.</span></span> <span data-ttu-id="e9e3a-119">經過剖析的檔案以及良好的 cdf 和新產生的 Good.cat，全都在相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-119">The parsed files, along with Good.cdf and the newly generated Good.cat, are all in the same directory.</span></span>

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> <span data-ttu-id="e9e3a-120">專案中的最後一個專案必須在行尾必須有明確的分行符號。</span><span class="sxs-lookup"><span data-stu-id="e9e3a-120">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

 

 
