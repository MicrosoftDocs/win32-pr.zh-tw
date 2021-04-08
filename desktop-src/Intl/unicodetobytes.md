---
UID: ''
title: UnicodeToBytes 函式
description: 將 Unicode 字元轉換成 GB18030 位元組。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "103679503"
---
# <a name="unicodetobytes-function"></a><span data-ttu-id="10661-103">UnicodeToBytes 函式</span><span class="sxs-lookup"><span data-stu-id="10661-103">UnicodeToBytes function</span></span>

## <a name="description"></a><span data-ttu-id="10661-104">Description</span><span class="sxs-lookup"><span data-stu-id="10661-104">Description</span></span>

<span data-ttu-id="10661-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="10661-105">Deprecated.</span></span> <span data-ttu-id="10661-106">將 Unicode 字元轉換成 GB18030 位元組。</span><span class="sxs-lookup"><span data-stu-id="10661-106">Converts Unicode characters to GB18030 bytes.</span></span>

<span data-ttu-id="10661-107">**注意**  將 Unicode 字元轉換成 GB18030 位元組時，要在 Windows Vista 和更新版本上執行的應用程式應該使用 [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) 函式。</span><span class="sxs-lookup"><span data-stu-id="10661-107">**Note**  When converting Unicode characters to GB18030 bytes, an application to run on Windows Vista and later should use the [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function.</span></span>

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a><span data-ttu-id="10661-108">參數</span><span class="sxs-lookup"><span data-stu-id="10661-108">Parameters</span></span>

### <a name="lpwidecharstr-in"></a><span data-ttu-id="10661-109">lpWideCharStr [in]</span><span class="sxs-lookup"><span data-stu-id="10661-109">lpWideCharStr [in]</span></span>

<span data-ttu-id="10661-110">要轉換的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="10661-110">Pointer to the Unicode string to convert.</span></span>

### <a name="cchwidechar-in"></a><span data-ttu-id="10661-111">cchWideChar [in]</span><span class="sxs-lookup"><span data-stu-id="10661-111">cchWideChar [in]</span></span>

<span data-ttu-id="10661-112">要轉換的 Unicode 字串的字元計數。</span><span class="sxs-lookup"><span data-stu-id="10661-112">Character count of the Unicode string to convert.</span></span>

### <a name="lpmultibytestr-in"></a><span data-ttu-id="10661-113">lpMultiByteStr [in]</span><span class="sxs-lookup"><span data-stu-id="10661-113">lpMultiByteStr [in]</span></span>

<span data-ttu-id="10661-114">目標多位元組緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="10661-114">Pointer to the target multibyte buffer.</span></span>
<span data-ttu-id="10661-115">如果 *lpMultiByteStr* 為0，則會傳回 GB18030 結果的位元組計數，且不會進行任何轉換。</span><span class="sxs-lookup"><span data-stu-id="10661-115">If *lpMultiByteStr* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

### <a name="cchmultibyte-in"></a><span data-ttu-id="10661-116">cchMultiByte [in]</span><span class="sxs-lookup"><span data-stu-id="10661-116">cchMultiByte [in]</span></span>

<span data-ttu-id="10661-117">目標多位元組緩衝區的位元組計數。</span><span class="sxs-lookup"><span data-stu-id="10661-117">Byte count of the target multibyte buffer.</span></span>
<span data-ttu-id="10661-118">如果 *cchMultiByte* 為0，則會傳回 GB18030 結果的位元組計數，且不會進行任何轉換。</span><span class="sxs-lookup"><span data-stu-id="10661-118">If *cchMultiByte* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

## <a name="returns"></a><span data-ttu-id="10661-119">傳回</span><span class="sxs-lookup"><span data-stu-id="10661-119">Returns</span></span>

<span data-ttu-id="10661-120">如果成功，則傳回所產生之多位元組字元的位元組計數。</span><span class="sxs-lookup"><span data-stu-id="10661-120">Returns the byte count of the multibyte characters that are generated, if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="10661-121">備註</span><span class="sxs-lookup"><span data-stu-id="10661-121">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="10661-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10661-122">See also</span></span>

[<span data-ttu-id="10661-123">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="10661-123">WideCharToMultiByte</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[<span data-ttu-id="10661-124">MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="10661-124">MultiByteToWideChar</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
