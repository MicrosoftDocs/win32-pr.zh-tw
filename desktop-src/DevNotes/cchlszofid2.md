---
description: 解碼和儲存字串。
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990763"
---
# <a name="cchlszofid2-function"></a><span data-ttu-id="03204-103">CchLszOfId2 函式</span><span class="sxs-lookup"><span data-stu-id="03204-103">CchLszOfId2 function</span></span>

<span data-ttu-id="03204-104">解碼和儲存字串。</span><span class="sxs-lookup"><span data-stu-id="03204-104">Decodes and stores a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="03204-105">語法</span><span class="sxs-lookup"><span data-stu-id="03204-105">Syntax</span></span>


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a><span data-ttu-id="03204-106">參數</span><span class="sxs-lookup"><span data-stu-id="03204-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03204-107">*id*</span><span class="sxs-lookup"><span data-stu-id="03204-107">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="03204-108">要解碼和儲存的資源檔中的字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="03204-108">The identifier of the string in the resource file to be decoded and stored.</span></span> <span data-ttu-id="03204-109">未驗證字串的有效性。</span><span class="sxs-lookup"><span data-stu-id="03204-109">The validity of the string is not verified.</span></span>

</dd> <dt>

<span data-ttu-id="03204-110">*lsz*</span><span class="sxs-lookup"><span data-stu-id="03204-110">*lsz*</span></span> 
</dt> <dd>

<span data-ttu-id="03204-111">長度為 *cbmax* 之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="03204-111">A pointer to a buffer with a length of *cbmax*.</span></span> <span data-ttu-id="03204-112">長度超過 *cbmax* 的字串會被截斷。</span><span class="sxs-lookup"><span data-stu-id="03204-112">Strings that are longer than *cbmax* are truncated.</span></span>

</dd> <dt>

<span data-ttu-id="03204-113">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="03204-113">*cbmax*</span></span> 
</dt> <dd>

<span data-ttu-id="03204-114">要儲存在 *lsz* 參數中之字串的最大長度。</span><span class="sxs-lookup"><span data-stu-id="03204-114">The maximum length of the string to be stored in the *lsz* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03204-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="03204-115">Return value</span></span>

<span data-ttu-id="03204-116">此函數會傳回已解碼的字串。</span><span class="sxs-lookup"><span data-stu-id="03204-116">This function returns the decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="03204-117">備註</span><span class="sxs-lookup"><span data-stu-id="03204-117">Remarks</span></span>

<span data-ttu-id="03204-118">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="03204-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="03204-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="03204-119">Requirements</span></span>



| <span data-ttu-id="03204-120">需求</span><span class="sxs-lookup"><span data-stu-id="03204-120">Requirement</span></span> | <span data-ttu-id="03204-121">值</span><span class="sxs-lookup"><span data-stu-id="03204-121">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03204-122">DLL</span><span class="sxs-lookup"><span data-stu-id="03204-122">DLL</span></span><br/> | <dl> <span data-ttu-id="03204-123"><dt>Msjint40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03204-123"><dt>Msjint40.dll</dt></span></span> </dl> |



 

 
