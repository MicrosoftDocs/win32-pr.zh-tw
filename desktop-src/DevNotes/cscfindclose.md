---
description: 關閉搜尋控制碼。
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: CSCFindClose 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001609"
---
# <a name="cscfindclose-function"></a><span data-ttu-id="c194c-103">CSCFindClose 函式</span><span class="sxs-lookup"><span data-stu-id="c194c-103">CSCFindClose function</span></span>

<span data-ttu-id="c194c-104">\[這項功能不受支援，因此不應該使用。\]</span><span class="sxs-lookup"><span data-stu-id="c194c-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="c194c-105">關閉搜尋控制碼。</span><span class="sxs-lookup"><span data-stu-id="c194c-105">Closes a search handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c194c-106">語法</span><span class="sxs-lookup"><span data-stu-id="c194c-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a><span data-ttu-id="c194c-107">參數</span><span class="sxs-lookup"><span data-stu-id="c194c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c194c-108">*hFind* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c194c-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c194c-109">[**CSCFindFirstFileW**](cscfindfirstfilew.md)函數所傳回的搜尋控制碼。</span><span class="sxs-lookup"><span data-stu-id="c194c-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c194c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c194c-110">Return value</span></span>

<span data-ttu-id="c194c-111">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c194c-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c194c-112">備註</span><span class="sxs-lookup"><span data-stu-id="c194c-112">Remarks</span></span>

<span data-ttu-id="c194c-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="c194c-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c194c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c194c-114">Requirements</span></span>



| <span data-ttu-id="c194c-115">需求</span><span class="sxs-lookup"><span data-stu-id="c194c-115">Requirement</span></span> | <span data-ttu-id="c194c-116">值</span><span class="sxs-lookup"><span data-stu-id="c194c-116">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c194c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c194c-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c194c-118"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c194c-118"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c194c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c194c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c194c-120">**CSCFindFirstFileW**</span><span class="sxs-lookup"><span data-stu-id="c194c-120">**CSCFindFirstFileW**</span></span>](cscfindfirstfilew.md)
</dt> </dl>

 

 
