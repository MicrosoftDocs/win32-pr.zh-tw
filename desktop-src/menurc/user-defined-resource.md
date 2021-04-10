---
title: User-Defined 資源
description: 使用者定義的資源定義語句會定義包含應用程式特定資料的資源。
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- 使用者定義的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183439"
---
# <a name="user-defined-resource"></a><span data-ttu-id="2da6d-104">User-Defined 資源</span><span class="sxs-lookup"><span data-stu-id="2da6d-104">User-Defined Resource</span></span>

<span data-ttu-id="2da6d-105">使用者定義的資源定義語句會定義包含應用程式特定資料的資源。</span><span class="sxs-lookup"><span data-stu-id="2da6d-105">A user-defined resource-definition statement defines a resource that contains application-specific data.</span></span> <span data-ttu-id="2da6d-106">資料可以具有任何格式，而且可以定義為指定檔案的內容 (如果指定 *檔案名* 參數) 或指定為一系列的數位和字串 (如果) 指定 *原始資料* 區塊。</span><span class="sxs-lookup"><span data-stu-id="2da6d-106">The data can have any format and can be defined either as the content of a given file (if the *filename* parameter is given) or as a series of numbers and strings (if the *raw-data* block is specified).</span></span>

``` syntax
nameID typeID filename
```

<span data-ttu-id="2da6d-107">*檔案名* 會指定包含資源之二進位資料的檔案名。</span><span class="sxs-lookup"><span data-stu-id="2da6d-107">The *filename* specifies the name of a file containing the binary data of the resource.</span></span> <span data-ttu-id="2da6d-108">檔案內容會包含在資源中。</span><span class="sxs-lookup"><span data-stu-id="2da6d-108">The contents of the file are included as the resource.</span></span> <span data-ttu-id="2da6d-109">RC 不會以任何方式解讀二進位資料。</span><span class="sxs-lookup"><span data-stu-id="2da6d-109">RC does not interpret the binary data in any way.</span></span> <span data-ttu-id="2da6d-110">程式設計人員必須負責確保目的電腦架構的資料已正確對齊。</span><span class="sxs-lookup"><span data-stu-id="2da6d-110">It is the programmer's responsibility to ensure that the data is properly aligned for the target computer architecture.</span></span>

<span data-ttu-id="2da6d-111">您也可以使用下列語法，在資源腳本中完全定義使用者定義的資源：</span><span class="sxs-lookup"><span data-stu-id="2da6d-111">A user-defined resource can also be defined completely in the resource script using the following syntax:</span></span>

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a><span data-ttu-id="2da6d-112">參數</span><span class="sxs-lookup"><span data-stu-id="2da6d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da6d-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="2da6d-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="2da6d-114">識別資源的唯一名稱或16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="2da6d-114">Unique name or a 16-bit unsigned integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="2da6d-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span><span class="sxs-lookup"><span data-stu-id="2da6d-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span></span>
</dt> <dd>

<span data-ttu-id="2da6d-116">識別資源類型的唯一名稱或16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="2da6d-116">Unique name or a 16-bit unsigned integer that identifies the resource type.</span></span> <span data-ttu-id="2da6d-117">如果指定了數位，則它必須大於255。</span><span class="sxs-lookup"><span data-stu-id="2da6d-117">If a number is given, it must be greater than 255.</span></span> <span data-ttu-id="2da6d-118">數位1到255會保留給現有和未來重新定義的資源類型。</span><span class="sxs-lookup"><span data-stu-id="2da6d-118">The numbers 1 through 255 are reserved for existing and future redefined resource types.</span></span>

</dd> <dt>

<span data-ttu-id="2da6d-119"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="2da6d-119"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="2da6d-120">包含資源資料的檔案名。</span><span class="sxs-lookup"><span data-stu-id="2da6d-120">Name of the file that contains the resource data.</span></span> <span data-ttu-id="2da6d-121">參數必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2da6d-121">The parameter must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span>

</dd> <dt>

<span data-ttu-id="2da6d-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*原始資料*</span><span class="sxs-lookup"><span data-stu-id="2da6d-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="2da6d-123">由一或多個整數或字元字串所組成的原始資料。</span><span class="sxs-lookup"><span data-stu-id="2da6d-123">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="2da6d-124">您可以用十進位、八進位或十六進位格式來指定整數。</span><span class="sxs-lookup"><span data-stu-id="2da6d-124">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="2da6d-125">為了與16位 Windows 相容，整數會儲存為文字值。</span><span class="sxs-lookup"><span data-stu-id="2da6d-125">To be compatible with 16-bit Windows, integers are stored as WORD values.</span></span> <span data-ttu-id="2da6d-126">您可以使用 "L" 尾碼來限定整數，以將整數儲存為 DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="2da6d-126">You can store an integer as a DWORD value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="2da6d-127">字串會以引號括住。</span><span class="sxs-lookup"><span data-stu-id="2da6d-127">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="2da6d-128">RC 不會自動將終止的 null 字元附加至字串。</span><span class="sxs-lookup"><span data-stu-id="2da6d-128">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="2da6d-129">每個字串都是指定之 ANSI 字元的序列，除非您將它限定為具有 "L" 前置詞的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="2da6d-129">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the "L" prefix.</span></span>

<span data-ttu-id="2da6d-130">資料區塊開始于 **DWORD** 界限，而 RC 不會在 *原始資料* 區塊內執行資料的填補或對齊。</span><span class="sxs-lookup"><span data-stu-id="2da6d-130">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="2da6d-131">程式設計人員必須負責確保區塊內適當的資料對齊。</span><span class="sxs-lookup"><span data-stu-id="2da6d-131">It is the programmer's responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="2da6d-132">範例</span><span class="sxs-lookup"><span data-stu-id="2da6d-132">Example</span></span>

<span data-ttu-id="2da6d-133">下列範例會顯示數個使用者定義的語句：</span><span class="sxs-lookup"><span data-stu-id="2da6d-133">The following example shows several user-defined statements:</span></span>

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




