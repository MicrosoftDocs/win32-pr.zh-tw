---
description: 載入指定版本的 .NET Framework 程式庫 DLL。
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982275"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="5f7ea-103">LoadLibraryShim 函式</span><span class="sxs-lookup"><span data-stu-id="5f7ea-103">LoadLibraryShim function</span></span>

<span data-ttu-id="5f7ea-104">載入指定版本的 .NET Framework 程式庫 DLL。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-104">Loads a specified version of a .NET Framework library DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f7ea-105">語法</span><span class="sxs-lookup"><span data-stu-id="5f7ea-105">Syntax</span></span>


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a><span data-ttu-id="5f7ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="5f7ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f7ea-107">*szDllName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f7ea-107">*szDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f7ea-108">要從 .NET Framework 載入的 DLL 名稱。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-108">The name of the DLL to be loaded from the .NET Framework.</span></span>

</dd> <dt>

<span data-ttu-id="5f7ea-109">*szVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f7ea-109">*szVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f7ea-110">要載入的 DLL 版本。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-110">The version of the DLL to be loaded.</span></span> <span data-ttu-id="5f7ea-111">如果 *szVersion* 為 **Null**，則會載入指定 DLL 的最新版本。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-111">If *szVersion* is **NULL**, the latest version of the specified DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="5f7ea-112">*pvReserved*</span><span class="sxs-lookup"><span data-stu-id="5f7ea-112">*pvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="5f7ea-113">保留的。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5f7ea-114">*phModDll* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5f7ea-114">*phModDll* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f7ea-115">模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-115">A handle to the module.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f7ea-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f7ea-116">Return value</span></span>

<span data-ttu-id="5f7ea-117">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f7ea-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f7ea-119">備註</span><span class="sxs-lookup"><span data-stu-id="5f7ea-119">Remarks</span></span>

<span data-ttu-id="5f7ea-120">這個函式是用來載入 .NET Framework 可轉散發套件所包含的程式庫 Dll，而不是使用者產生的 Dll。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-120">This function is used to load library DLLs that are included in the .NET Framework redistributable package, not user-generated DLLs.</span></span>

<span data-ttu-id="5f7ea-121">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f7ea-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f7ea-122">Requirements</span></span>



| <span data-ttu-id="5f7ea-123">需求</span><span class="sxs-lookup"><span data-stu-id="5f7ea-123">Requirement</span></span> | <span data-ttu-id="5f7ea-124">值</span><span class="sxs-lookup"><span data-stu-id="5f7ea-124">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7ea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5f7ea-125">DLL</span></span><br/> | <dl> <span data-ttu-id="5f7ea-126"><dt>Mscoree.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f7ea-126"><dt>Mscoree.dll</dt></span></span> </dl> |



 

 
