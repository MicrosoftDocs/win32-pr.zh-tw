---
description: 初始化字串資料表。
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: pSetupStringTableInitialize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993964"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="fb745-103">pSetupStringTableInitialize 函式</span><span class="sxs-lookup"><span data-stu-id="fb745-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="fb745-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="fb745-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="fb745-105">初始化字串資料表。</span><span class="sxs-lookup"><span data-stu-id="fb745-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb745-106">語法</span><span class="sxs-lookup"><span data-stu-id="fb745-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="fb745-107">參數</span><span class="sxs-lookup"><span data-stu-id="fb745-107">Parameters</span></span>

<span data-ttu-id="fb745-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="fb745-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb745-109">備註</span><span class="sxs-lookup"><span data-stu-id="fb745-109">Remarks</span></span>

<span data-ttu-id="fb745-110">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="fb745-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb745-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb745-111">Requirements</span></span>



| <span data-ttu-id="fb745-112">需求</span><span class="sxs-lookup"><span data-stu-id="fb745-112">Requirement</span></span> | <span data-ttu-id="fb745-113">值</span><span class="sxs-lookup"><span data-stu-id="fb745-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb745-114">DLL</span><span class="sxs-lookup"><span data-stu-id="fb745-114">DLL</span></span><br/> | <dl> <span data-ttu-id="fb745-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb745-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
