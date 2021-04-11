---
title: /I 參數
description: /I 參數會指定要搜尋匯入之 IDL 檔案的目錄、包含的標頭檔和 ACF 檔。
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I 參數 MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022570"
---
# <a name="i-switch"></a><span data-ttu-id="67aca-104">/I 參數</span><span class="sxs-lookup"><span data-stu-id="67aca-104">/I switch</span></span>

<span data-ttu-id="67aca-105">**/I** 參數會指定要搜尋匯入之 IDL 檔案的目錄、包含的標頭檔和 ACF 檔。</span><span class="sxs-lookup"><span data-stu-id="67aca-105">The **/I** switch specifies directories to be searched for imported IDL files, included header files, and ACF files.</span></span>

``` syntax
midl /I include_path
```

## <a name="switch-options"></a><span data-ttu-id="67aca-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="67aca-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="67aca-107">*包含 \_ 路徑*</span><span class="sxs-lookup"><span data-stu-id="67aca-107">*include\_path*</span></span> 
</dt> <dd>

<span data-ttu-id="67aca-108">指定包含匯入、包含和 ACF 檔案的一或多個目錄。</span><span class="sxs-lookup"><span data-stu-id="67aca-108">Specifies one or more directories that contain import, include, and ACF files.</span></span> <span data-ttu-id="67aca-109">**/I** 參數和 *include \_ 路徑* 之間的空格是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="67aca-109">White space between the **/I** switch and *include\_path* is optional.</span></span> <span data-ttu-id="67aca-110">以分號字元 ( 分隔多個目錄，) 。</span><span class="sxs-lookup"><span data-stu-id="67aca-110">Separate multiple directories with a semicolon character (;).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67aca-111">備註</span><span class="sxs-lookup"><span data-stu-id="67aca-111">Remarks</span></span>

<span data-ttu-id="67aca-112">每個 **/i** 參數可以出現一個以上的目錄，而且每個 MIDL 編譯器調用可以出現一個以上的 **/i** 參數。</span><span class="sxs-lookup"><span data-stu-id="67aca-112">More than one directory can appear with each **/I** switch, and more than one **/I** switch can appear with each MIDL compiler invocation.</span></span> <span data-ttu-id="67aca-113">系統會依照指定的順序來搜尋目錄。</span><span class="sxs-lookup"><span data-stu-id="67aca-113">Directories are searched in the order they are specified.</span></span>

<span data-ttu-id="67aca-114">**/I** 參數設定也會由 MIDL 編譯器傳遞到 c 編譯器的 c 預處理器。</span><span class="sxs-lookup"><span data-stu-id="67aca-114">The **/I** switch setting is also passed by the MIDL compiler to the C compiler's C preprocessor.</span></span> <span data-ttu-id="67aca-115">當 [**/cpp \_ cmd**](-cpp-cmd.md) 參數存在且 [**/cpp \_ opt**](-cpp-opt.md) 參數不是時，MIDL 編譯器會串連 **/cpp \_ cmd** 參數所指定的字串與 **/i**、 [**/d**](-d.md)和 [**/U**](-u.md) 選項，並使用這個串連的字串來叫用每個 IDL 和 ACF 原始程式檔的 C 預處理器。</span><span class="sxs-lookup"><span data-stu-id="67aca-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the **/I**, [**/D**](-d.md), and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="67aca-116">當指定 MIDL 編譯器參數 **/no \_ cpp** 或 **/cpp \_ opt** 時，不會將 midl 編譯器參數 **/i** 傳遞給預處理器。</span><span class="sxs-lookup"><span data-stu-id="67aca-116">The MIDL compiler switch **/I** is not passed to the preprocessor when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

<span data-ttu-id="67aca-117">在 Microsoft 作業系統環境中 (64 位 Windows、32位 windows、16位 Windows 和 MS-DOS) ，會以下列順序搜尋目錄：</span><span class="sxs-lookup"><span data-stu-id="67aca-117">In Microsoft operating-system environments (64-bit Windows, 32-bit Windows, 16-bit Windows, and MS-DOS), directories are searched in the following sequence:</span></span>

1.  <span data-ttu-id="67aca-118">目前的目錄</span><span class="sxs-lookup"><span data-stu-id="67aca-118">Current directory</span></span>
2.  <span data-ttu-id="67aca-119">**/I** 參數所指定的目錄會依參數遵循參數的順序 () </span><span class="sxs-lookup"><span data-stu-id="67aca-119">Directories specified by the **/I** switch (in the order they follow the switch)</span></span>
3.  <span data-ttu-id="67aca-120">INCLUDE 環境變數所指定的目錄</span><span class="sxs-lookup"><span data-stu-id="67aca-120">Directories specified by the INCLUDE environment variable</span></span>

<span data-ttu-id="67aca-121">使用 **/i** 參數指定目錄時， [**/no \_ def \_ idir**](-no-def-idir.md) 參數會指示 MIDL 編譯器忽略目前的目錄、忽略 INCLUDE 環境變數所指定的目錄，並只搜尋指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="67aca-121">When directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to ignore the current directory, ignore the directories specified by the INCLUDE environment variable, and search only the specified directories.</span></span>

<span data-ttu-id="67aca-122">使用 **/i** 參數指定目錄時， [**/no \_ def \_ idir**](-no-def-idir.md) 參數會指示 MIDL 編譯器只搜尋目前目錄。</span><span class="sxs-lookup"><span data-stu-id="67aca-122">When no directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="67aca-123">範例</span><span class="sxs-lookup"><span data-stu-id="67aca-123">Examples</span></span>

<span data-ttu-id="67aca-124">**midl/I c： \\ include; c： \\ include \\ h/i \\ include2 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="67aca-124">**midl /I c:\\include;c:\\include\\h /I\\include2 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="67aca-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67aca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67aca-126">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="67aca-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="67aca-127">**/acf**</span><span class="sxs-lookup"><span data-stu-id="67aca-127">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="67aca-128">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="67aca-128">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="67aca-129">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="67aca-129">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="67aca-130">**/no \_ def \_ idir**</span><span class="sxs-lookup"><span data-stu-id="67aca-130">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




