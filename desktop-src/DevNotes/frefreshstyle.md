---
description: 從登錄重載色彩設定。
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989798"
---
# <a name="frefreshstyle-function"></a><span data-ttu-id="9f74f-103">FRefreshStyle 函式</span><span class="sxs-lookup"><span data-stu-id="9f74f-103">FRefreshStyle function</span></span>

<span data-ttu-id="9f74f-104">從登錄重載色彩設定。</span><span class="sxs-lookup"><span data-stu-id="9f74f-104">Reloads color settings from registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f74f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9f74f-105">Syntax</span></span>


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a><span data-ttu-id="9f74f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f74f-106">Parameters</span></span>

<span data-ttu-id="9f74f-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="9f74f-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f74f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f74f-108">Return value</span></span>

<span data-ttu-id="9f74f-109">成功時傳回 TRUE;否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="9f74f-109">Returns TRUE on success; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f74f-110">備註</span><span class="sxs-lookup"><span data-stu-id="9f74f-110">Remarks</span></span>

<span data-ttu-id="9f74f-111">此函式與匯入程式庫或標頭檔沒有關聯;您必須使用 [**LoadLibrary**](-loadlibrary.md) 和 [**GetProcAddress**](-getprocaddress-.md) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="9f74f-111">This function is not associated with an import library or header file; it must be called using the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f74f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f74f-112">Requirements</span></span>



| <span data-ttu-id="9f74f-113">需求</span><span class="sxs-lookup"><span data-stu-id="9f74f-113">Requirement</span></span> | <span data-ttu-id="9f74f-114">值</span><span class="sxs-lookup"><span data-stu-id="9f74f-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f74f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="9f74f-115">DLL</span></span><br/> | <dl> <span data-ttu-id="9f74f-116"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f74f-116"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f74f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f74f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f74f-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="9f74f-118">**GetProcAddress**</span></span>](-getprocaddress-.md)
</dt> <dt>

[<span data-ttu-id="9f74f-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="9f74f-119">**LoadLibrary**</span></span>](-loadlibrary.md)
</dt> </dl>

 

 




