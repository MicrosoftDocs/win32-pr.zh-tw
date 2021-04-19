---
description: 將解決延遲載入的匯入工作從父二進位檔轉送到目標二進位檔。
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984754"
---
# <a name="resolvedelayloadsfromdll-function"></a><span data-ttu-id="c5b44-103">ResolveDelayLoadsFromDll 函式</span><span class="sxs-lookup"><span data-stu-id="c5b44-103">ResolveDelayLoadsFromDll function</span></span>

<span data-ttu-id="c5b44-104">將解決延遲載入的匯入工作從父二進位檔轉送到目標二進位檔。</span><span class="sxs-lookup"><span data-stu-id="c5b44-104">Forwards the work in resolving delay-loaded imports from the parent binary to a target binary.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b44-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5b44-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="c5b44-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5b44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b44-107">*ParentBase* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5b44-107">*ParentBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b44-108">延遲載入另一個二進位檔之模組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="c5b44-108">The base address of the module that delay loads another binary.</span></span>

</dd> <dt>

<span data-ttu-id="c5b44-109">*TargetDllName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5b44-109">*TargetDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b44-110">目標 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5b44-110">The name of the target DLL.</span></span>

</dd> <dt>

<span data-ttu-id="c5b44-111">*旗標*</span><span class="sxs-lookup"><span data-stu-id="c5b44-111">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b44-112">保護必須是0。</span><span class="sxs-lookup"><span data-stu-id="c5b44-112">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b44-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5b44-113">Return value</span></span>

<span data-ttu-id="c5b44-114">延遲載入描述項的位址（如果找到的話）。否則 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="c5b44-114">The address of the delay-load descriptor, if it is found; otherwise, **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b44-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5b44-115">Requirements</span></span>



| <span data-ttu-id="c5b44-116">需求</span><span class="sxs-lookup"><span data-stu-id="c5b44-116">Requirement</span></span> | <span data-ttu-id="c5b44-117">值</span><span class="sxs-lookup"><span data-stu-id="c5b44-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b44-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5b44-118">Library</span></span><br/> | <dl> <span data-ttu-id="c5b44-119"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5b44-119"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c5b44-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c5b44-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5b44-121"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5b44-121"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5b44-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5b44-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5b44-123">[Delay-Loaded Dll 的連結器支援](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="c5b44-123">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




