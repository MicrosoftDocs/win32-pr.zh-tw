---
description: 傳回指定之 DLL 和進程的延遲載入失敗回呼函式的位址。
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993492"
---
# <a name="delayloadfailurehook-function"></a><span data-ttu-id="cf814-103">DelayLoadFailureHook 函式</span><span class="sxs-lookup"><span data-stu-id="cf814-103">DelayLoadFailureHook function</span></span>

<span data-ttu-id="cf814-104">傳回指定之 DLL 和進程的延遲載入失敗回呼函式的位址。</span><span class="sxs-lookup"><span data-stu-id="cf814-104">Returns the address of a delay-load failure callback function for the specified DLL and process.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf814-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf814-105">Syntax</span></span>


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a><span data-ttu-id="cf814-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf814-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf814-107">*pszDllName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf814-107">*pszDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf814-108">DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf814-108">The name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="cf814-109">*pszProcName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf814-109">*pszProcName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf814-110">處理序的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf814-110">The name of the process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf814-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf814-111">Return value</span></span>

<span data-ttu-id="cf814-112">回呼函式的位址。</span><span class="sxs-lookup"><span data-stu-id="cf814-112">The address of the callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf814-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf814-113">Requirements</span></span>



| <span data-ttu-id="cf814-114">需求</span><span class="sxs-lookup"><span data-stu-id="cf814-114">Requirement</span></span> | <span data-ttu-id="cf814-115">值</span><span class="sxs-lookup"><span data-stu-id="cf814-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf814-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf814-116">Library</span></span><br/> | <dl> <span data-ttu-id="cf814-117"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf814-117"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf814-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cf814-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf814-119"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf814-119"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf814-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf814-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf814-121">[失敗攔截](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="cf814-121">[Failure Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




