---
title: ADSI)  (常見的錯誤
description: 所有 ADSI 特定的錯誤都具有十六進位形式的80005xxx。 下表概述最常遇到的錯誤碼。
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "104314019"
---
# <a name="common-errors-adsi"></a><span data-ttu-id="19279-104">ADSI)  (常見的錯誤</span><span class="sxs-lookup"><span data-stu-id="19279-104">Common Errors (ADSI)</span></span>

<span data-ttu-id="19279-105">所有 ADSI 特定的錯誤都具有十六進位形式的80005xxx。</span><span class="sxs-lookup"><span data-stu-id="19279-105">All ADSI-specific errors have a hexadecimal form of 80005xxx.</span></span> <span data-ttu-id="19279-106">下表概述最常遇到的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19279-106">The most common error codes encountered are outlined in the following table.</span></span>



| <span data-ttu-id="19279-107">ADSI hex 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="19279-107">ADSI hex error code</span></span> | <span data-ttu-id="19279-108">Description</span><span class="sxs-lookup"><span data-stu-id="19279-108">Description</span></span>                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19279-109">80005000</span><span class="sxs-lookup"><span data-stu-id="19279-109">80005000</span></span><br/> | <span data-ttu-id="19279-110">傳遞的 ADSI 路徑名稱無效。</span><span class="sxs-lookup"><span data-stu-id="19279-110">An invalid ADSI pathname was passed.</span></span> <span data-ttu-id="19279-111">此錯誤的結果是在系結至物件時，將不良格式的 ADsPath 傳遞給 **GetObject** 。</span><span class="sxs-lookup"><span data-stu-id="19279-111">This error results from passing a poorly formed ADsPath to **GetObject** when binding to an object.</span></span><br/> |
| <span data-ttu-id="19279-112">8000500D</span><span class="sxs-lookup"><span data-stu-id="19279-112">8000500D</span></span><br/> | <span data-ttu-id="19279-113">屬性快取中找不到 ADSI 屬性。</span><span class="sxs-lookup"><span data-stu-id="19279-113">The ADSI property cannot be found in the property cache.</span></span><br/>                                                                                 |
| <span data-ttu-id="19279-114">8000500E</span><span class="sxs-lookup"><span data-stu-id="19279-114">8000500E</span></span><br/> | <span data-ttu-id="19279-115">ADSI 物件存在。</span><span class="sxs-lookup"><span data-stu-id="19279-115">The ADSI object exists.</span></span> <span data-ttu-id="19279-116">如果您嘗試建立的 ADSI 物件與現有的 ADSI 物件名稱相同，就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="19279-116">If you attempt to create an ADSI object with the same name as an existing ADSI object, this error will occur.</span></span><br/>    |



 

<span data-ttu-id="19279-117">如需 ADSI 錯誤碼的完整清單，請參閱 [一般 Adsi 錯誤碼](generic-adsi-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="19279-117">For a complete list of ADSI error codes, see [Generic ADSI Error Codes](generic-adsi-error-codes.md).</span></span>

## <a name="com-errors"></a><span data-ttu-id="19279-118">COM 錯誤</span><span class="sxs-lookup"><span data-stu-id="19279-118">COM Errors</span></span>

<span data-ttu-id="19279-119">因為 ADSI 是由 COM 物件所組成，所以會傳回標準 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19279-119">Since ADSI is composed of COM objects, it will return standard COM error codes.</span></span> <span data-ttu-id="19279-120">下表列出 ADSI 程式設計中最常遇到的 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19279-120">The following table lists the COM error codes most commonly encountered in ADSI programming.</span></span>



| <span data-ttu-id="19279-121">COM 十六進位錯誤碼</span><span class="sxs-lookup"><span data-stu-id="19279-121">COM hex error code</span></span>  | <span data-ttu-id="19279-122">Description</span><span class="sxs-lookup"><span data-stu-id="19279-122">Description</span></span>                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19279-123">80004005</span><span class="sxs-lookup"><span data-stu-id="19279-123">80004005</span></span><br/> | <span data-ttu-id="19279-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="19279-124">Unspecified error.</span></span> <span data-ttu-id="19279-125">ADSI 無法確定 COM 物件失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="19279-125">The cause of the COM object failure is indeterminate by ADSI.</span></span> <br/>                                  |
| <span data-ttu-id="19279-126">800041E4</span><span class="sxs-lookup"><span data-stu-id="19279-126">800041E4</span></span><br/> | <span data-ttu-id="19279-127">找不到物件。</span><span class="sxs-lookup"><span data-stu-id="19279-127">Object not found.</span></span> <span data-ttu-id="19279-128">發生此錯誤的主要原因是在系結至物件時，ADsPath 字串拼寫錯誤。</span><span class="sxs-lookup"><span data-stu-id="19279-128">This error predominantly occurs due to misspelling the ADsPath string when binding to an object.</span></span><br/> |



 

<span data-ttu-id="19279-129">如需一些可能會在 ADSI 程式設計中發生的 COM 錯誤範例，請參閱 [泛型 Com 錯誤碼](generic-com-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="19279-129">See [Generic COM Error Codes](generic-com-error-codes.md) for a few more examples of COM errors that may occur in ADSI programming.</span></span>

## <a name="win32-errors"></a><span data-ttu-id="19279-130">Win32 錯誤</span><span class="sxs-lookup"><span data-stu-id="19279-130">Win32 Errors</span></span>

<span data-ttu-id="19279-131">十六進位形式8007xxxx 的任何錯誤碼都是標準的 Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19279-131">Any error code of the hexadecimal form 8007xxxx is a standard Win32 error code.</span></span> <span data-ttu-id="19279-132">如果您將最後四個數字從十六進位轉換成十進位，則可以從 Windows 2000 命令列存取錯誤：</span><span class="sxs-lookup"><span data-stu-id="19279-132">If you convert the last four digits from hexadecimal to decimal, you can access the error from the Windows 2000 command line:</span></span>

<span data-ttu-id="19279-133">**net helpmsg <number>**</span><span class="sxs-lookup"><span data-stu-id="19279-133">**net helpmsg <number>**</span></span>

<span data-ttu-id="19279-134">在上述命令列中，" &lt; number &gt; " 是從十六進位轉換錯誤碼的最後四個數字所取得的十進位數。</span><span class="sxs-lookup"><span data-stu-id="19279-134">In the command line above, "&lt;number&gt;" is the decimal number obtained by converting the last four digits of the error code from hexadecimal.</span></span> <span data-ttu-id="19279-135">此命令列將提供更有用的 Win32 錯誤描述，這對您的腳本而言很有説明。</span><span class="sxs-lookup"><span data-stu-id="19279-135">This command line will provide a more useful description of the Win32 error, which can be of great help in debugging your script.</span></span>

 

 





