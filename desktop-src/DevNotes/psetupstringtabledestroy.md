---
description: 刪除字串資料表。
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: pSetupStringTableDestroy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975973"
---
# <a name="psetupstringtabledestroy-function"></a><span data-ttu-id="7c382-103">pSetupStringTableDestroy 函式</span><span class="sxs-lookup"><span data-stu-id="7c382-103">pSetupStringTableDestroy function</span></span>

<span data-ttu-id="7c382-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="7c382-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="7c382-105">刪除字串資料表。</span><span class="sxs-lookup"><span data-stu-id="7c382-105">Deletes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c382-106">語法</span><span class="sxs-lookup"><span data-stu-id="7c382-106">Syntax</span></span>


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a><span data-ttu-id="7c382-107">參數</span><span class="sxs-lookup"><span data-stu-id="7c382-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c382-108">*StringTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c382-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c382-109">字串資料表的指標。</span><span class="sxs-lookup"><span data-stu-id="7c382-109">A pointer to the string table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c382-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c382-110">Return value</span></span>

<span data-ttu-id="7c382-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7c382-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c382-112">備註</span><span class="sxs-lookup"><span data-stu-id="7c382-112">Remarks</span></span>

<span data-ttu-id="7c382-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="7c382-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c382-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c382-114">Requirements</span></span>



| <span data-ttu-id="7c382-115">需求</span><span class="sxs-lookup"><span data-stu-id="7c382-115">Requirement</span></span> | <span data-ttu-id="7c382-116">值</span><span class="sxs-lookup"><span data-stu-id="7c382-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c382-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7c382-117">DLL</span></span><br/> | <dl> <span data-ttu-id="7c382-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c382-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
