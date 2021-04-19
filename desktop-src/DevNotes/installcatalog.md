---
description: 在目錄中安裝目錄。
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995414"
---
# <a name="installcatalog-function"></a><span data-ttu-id="4140d-103">InstallCatalog 函式</span><span class="sxs-lookup"><span data-stu-id="4140d-103">InstallCatalog function</span></span>

<span data-ttu-id="4140d-104">\[這項功能不受支援，因此不應該使用。\]</span><span class="sxs-lookup"><span data-stu-id="4140d-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="4140d-105">在目錄中安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="4140d-105">Installs a catalog in a directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="4140d-106">語法</span><span class="sxs-lookup"><span data-stu-id="4140d-106">Syntax</span></span>


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="4140d-107">參數</span><span class="sxs-lookup"><span data-stu-id="4140d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4140d-108">*CatalogFullPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4140d-108">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4140d-109">字串的指標，表示安裝之前的目錄完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4140d-109">A pointer to a string that represents the full path of the catalog before installation.</span></span>

</dd> <dt>

<span data-ttu-id="4140d-110">*NewBaseName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4140d-110">*NewBaseName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4140d-111">新基底名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="4140d-111">A pointer to the new base name.</span></span>

</dd> <dt>

<span data-ttu-id="4140d-112">*NewCatalogFullPath* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="4140d-112">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4140d-113">字串的指標，代表安裝之後目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4140d-113">A pointer to a string that represent the full path of the catalog after installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4140d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4140d-114">Return value</span></span>

<span data-ttu-id="4140d-115">此函式目前未執行，因此不會傳回實際值。</span><span class="sxs-lookup"><span data-stu-id="4140d-115">This function is not currently implemented, so it does not return an actual value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4140d-116">備註</span><span class="sxs-lookup"><span data-stu-id="4140d-116">Remarks</span></span>

<span data-ttu-id="4140d-117">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="4140d-117">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4140d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4140d-118">Requirements</span></span>



| <span data-ttu-id="4140d-119">需求</span><span class="sxs-lookup"><span data-stu-id="4140d-119">Requirement</span></span> | <span data-ttu-id="4140d-120">值</span><span class="sxs-lookup"><span data-stu-id="4140d-120">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4140d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4140d-121">DLL</span></span><br/> | <dl> <span data-ttu-id="4140d-122"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4140d-122"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
