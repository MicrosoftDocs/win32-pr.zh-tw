---
description: pSetupStringTableInitializeEx 函式-初始化字串資料表。
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096646"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="ae91f-103">pSetupStringTableInitializeEx 函式</span><span class="sxs-lookup"><span data-stu-id="ae91f-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="ae91f-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="ae91f-105">初始化字串資料表。</span><span class="sxs-lookup"><span data-stu-id="ae91f-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae91f-106">語法</span><span class="sxs-lookup"><span data-stu-id="ae91f-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="ae91f-107">參數</span><span class="sxs-lookup"><span data-stu-id="ae91f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae91f-108">*ExtraDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae91f-109">額外資料物件的大小。</span><span class="sxs-lookup"><span data-stu-id="ae91f-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="ae91f-110">*保留* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae91f-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae91f-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="ae91f-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae91f-112">備註</span><span class="sxs-lookup"><span data-stu-id="ae91f-112">Remarks</span></span>

<span data-ttu-id="ae91f-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="ae91f-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae91f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae91f-114">Requirements</span></span>



| <span data-ttu-id="ae91f-115">需求</span><span class="sxs-lookup"><span data-stu-id="ae91f-115">Requirement</span></span> | <span data-ttu-id="ae91f-116">值</span><span class="sxs-lookup"><span data-stu-id="ae91f-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae91f-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ae91f-117">DLL</span></span><br/> | <dl> <span data-ttu-id="ae91f-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae91f-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
