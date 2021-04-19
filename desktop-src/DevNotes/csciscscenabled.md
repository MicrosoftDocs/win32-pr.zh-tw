---
description: 判斷是否已啟用離線檔案。
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: CSCIsCSCEnabled 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976193"
---
# <a name="csciscscenabled-function"></a><span data-ttu-id="93700-103">CSCIsCSCEnabled 函式</span><span class="sxs-lookup"><span data-stu-id="93700-103">CSCIsCSCEnabled function</span></span>

<span data-ttu-id="93700-104">\[這項功能不受支援，因此不應該使用。\]</span><span class="sxs-lookup"><span data-stu-id="93700-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="93700-105">判斷是否已啟用離線檔案。</span><span class="sxs-lookup"><span data-stu-id="93700-105">Determines whether Offline Files is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="93700-106">語法</span><span class="sxs-lookup"><span data-stu-id="93700-106">Syntax</span></span>


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="93700-107">參數</span><span class="sxs-lookup"><span data-stu-id="93700-107">Parameters</span></span>

<span data-ttu-id="93700-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="93700-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93700-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="93700-109">Return value</span></span>

<span data-ttu-id="93700-110">如果已啟用離線檔案，此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="93700-110">This function returns **TRUE** if Offline Files is enabled and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="93700-111">備註</span><span class="sxs-lookup"><span data-stu-id="93700-111">Remarks</span></span>

<span data-ttu-id="93700-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="93700-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="93700-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="93700-113">Requirements</span></span>



| <span data-ttu-id="93700-114">需求</span><span class="sxs-lookup"><span data-stu-id="93700-114">Requirement</span></span> | <span data-ttu-id="93700-115">值</span><span class="sxs-lookup"><span data-stu-id="93700-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93700-116">DLL</span><span class="sxs-lookup"><span data-stu-id="93700-116">DLL</span></span><br/> | <dl> <span data-ttu-id="93700-117"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93700-117"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93700-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93700-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93700-119">**CSCQueryDatabaseStatus**</span><span class="sxs-lookup"><span data-stu-id="93700-119">**CSCQueryDatabaseStatus**</span></span>](cscquerydatabasestatus.md)
</dt> </dl>

 

 
