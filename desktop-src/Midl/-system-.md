---
title: /系統交換器
description: /系統參數會指示 MIDL 編譯器為指定的系統產生類型程式庫。 預設值為目前的作業系統。
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /系統交換器 MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312656"
---
# <a name="system-switch"></a><span data-ttu-id="78a34-105">/<system> 開關</span><span class="sxs-lookup"><span data-stu-id="78a34-105">/<system> switch</span></span>

<span data-ttu-id="78a34-106">此 **/<system>** 參數會指示 MIDL 編譯器為指定的系統產生類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="78a34-106">The **/<system>** switch directs the MIDL compiler to generate a type library for the specified system.</span></span> <span data-ttu-id="78a34-107">預設值為目前的作業系統。</span><span class="sxs-lookup"><span data-stu-id="78a34-107">The default is the current operating system.</span></span>

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a><span data-ttu-id="78a34-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="78a34-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="78a34-109"><span id="win32"></span><span id="WIN32"></span>win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="78a34-109"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="78a34-110">Windows 2000、Windows XP、Windows Vista、Windows 7</span><span class="sxs-lookup"><span data-stu-id="78a34-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="78a34-111"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="78a34-111"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="78a34-112">Intel 架構的64位 Windows 環境，例如 Windows 2000、Windows Server 2003、Windows XP Professional x64 Edition、Windows Vista 或 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="78a34-112">An Intel-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="78a34-113"><span id="amd64"></span><span id="AMD64"></span>amd64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="78a34-113"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="78a34-114">以美國微裝置為基礎的64位 Windows 環境，例如 Windows 2000、Windows Server 2003、Windows XP Professional x64 Edition、Windows Vista 或 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="78a34-114">An American Micro Devices-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78a34-115">備註</span><span class="sxs-lookup"><span data-stu-id="78a34-115">Remarks</span></span>

<span data-ttu-id="78a34-116">**/<system>** 參數的功能與 midl [**/env**](-env.md)選項相同，而且 midl 編譯器只會針對回溯相容性與 mktyplib.exe 進行辨識。</span><span class="sxs-lookup"><span data-stu-id="78a34-116">The **/<system>** switch is functionally the same as the MIDL [**/env**](-env.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span> <span data-ttu-id="78a34-117">如果您要產生新的 makefile，請使用 **/env** 參數。</span><span class="sxs-lookup"><span data-stu-id="78a34-117">If you are generating a new makefile, use the **/env** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="78a34-118">範例</span><span class="sxs-lookup"><span data-stu-id="78a34-118">Examples</span></span>

<span data-ttu-id="78a34-119">**midl/win32 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="78a34-119">**midl /win32 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="78a34-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78a34-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a34-121">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="78a34-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="78a34-122">**/env**</span><span class="sxs-lookup"><span data-stu-id="78a34-122">**/env**</span></span>](-env.md)
</dt> </dl>

 

 




