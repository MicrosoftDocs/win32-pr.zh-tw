---
description: 找出指定之匯入的目標函式，並將匯入 Thunk 中的函式指標取代為函式實作為目標。
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: ResolveDelayLoadedAPI 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997010"
---
# <a name="resolvedelayloadedapi-function"></a><span data-ttu-id="d1f4a-103">ResolveDelayLoadedAPI 函式</span><span class="sxs-lookup"><span data-stu-id="d1f4a-103">ResolveDelayLoadedAPI function</span></span>

<span data-ttu-id="d1f4a-104">找出指定之匯入的目標函式，並將匯入 Thunk 中的函式指標取代為函式實作為目標。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-104">Locates the target function of the specified import and replaces the function pointer in the import thunk with the target of the function implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f4a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d1f4a-105">Syntax</span></span>


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="d1f4a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d1f4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1f4a-107">*ParentModuleBase* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1f4a-107">*ParentModuleBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f4a-108">匯入延遲載入函數的模組基底位址。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-108">The address of the base of the module importing a delay-loaded function.</span></span>

</dd> <dt>

<span data-ttu-id="d1f4a-109">*DelayloadDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1f4a-109">*DelayloadDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f4a-110">要載入之模組的描述元。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-110">The descriptor for the module to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d1f4a-111">*FailureDllHook* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1f4a-111">*FailureDllHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f4a-112">失敗攔截的位址。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-112">The address of the failure hook.</span></span> <span data-ttu-id="d1f4a-113">請參閱 [**DelayLoadFailureHook**](delayloadfailurehook.md)。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-113">See [**DelayLoadFailureHook**](delayloadfailurehook.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1f4a-114">*FailureSystemHook* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1f4a-114">*FailureSystemHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f4a-115">系統失敗攔截的位址。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-115">The address of the system failure hook.</span></span>

</dd> <dt>

<span data-ttu-id="d1f4a-116">*ThunkAddress* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d1f4a-116">*ThunkAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f4a-117">目標函數的 Thunk 資料。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-117">The thunk data for the target function.</span></span> <span data-ttu-id="d1f4a-118">用來尋找函數的特定名稱資料表專案。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-118">Used to find the specific name table entry of the function.</span></span>

</dd> <dt>

<span data-ttu-id="d1f4a-119">*旗標*</span><span class="sxs-lookup"><span data-stu-id="d1f4a-119">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="d1f4a-120">保護必須是0。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-120">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1f4a-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1f4a-121">Return value</span></span>

<span data-ttu-id="d1f4a-122">匯入的位址，或其失敗的存根。</span><span class="sxs-lookup"><span data-stu-id="d1f4a-122">The address of the import, or the failure stub for it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1f4a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1f4a-123">Requirements</span></span>



| <span data-ttu-id="d1f4a-124">需求</span><span class="sxs-lookup"><span data-stu-id="d1f4a-124">Requirement</span></span> | <span data-ttu-id="d1f4a-125">值</span><span class="sxs-lookup"><span data-stu-id="d1f4a-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f4a-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1f4a-126">Library</span></span><br/> | <dl> <span data-ttu-id="d1f4a-127"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1f4a-127"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1f4a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d1f4a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1f4a-129"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1f4a-129"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1f4a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1f4a-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1f4a-131">[Delay-Loaded Dll 的連結器支援](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="d1f4a-131">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




