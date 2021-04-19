---
description: 安裝類別目錄檔案。
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: pSetupInstallCatalog 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996210"
---
# <a name="psetupinstallcatalog-function"></a><span data-ttu-id="e233e-103">pSetupInstallCatalog 函式</span><span class="sxs-lookup"><span data-stu-id="e233e-103">pSetupInstallCatalog function</span></span>

<span data-ttu-id="e233e-104">\[Microsoft 不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="e233e-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="e233e-105">開發人員應使用 **CryptCATAdminAddCatalog**。\]</span><span class="sxs-lookup"><span data-stu-id="e233e-105">Developers should use **CryptCATAdminAddCatalog**.\]</span></span>

<span data-ttu-id="e233e-106">安裝類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="e233e-106">Installs a catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e233e-107">語法</span><span class="sxs-lookup"><span data-stu-id="e233e-107">Syntax</span></span>


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="e233e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e233e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e233e-109">*CatalogFullPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e233e-109">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e233e-110">要安裝在系統上之目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e233e-110">The fully qualified path of the catalog to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e233e-111">*NewBaseName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e233e-111">*NewBaseName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e233e-112">將類別目錄檔案複製到目錄存放區時要使用的新基底名稱。</span><span class="sxs-lookup"><span data-stu-id="e233e-112">The new base name to use when the catalog file is copied into the catalog store.</span></span>

</dd> <dt>

<span data-ttu-id="e233e-113">*NewCatalogFullPath* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="e233e-113">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e233e-114">（選擇性）在目錄存放區內接收目錄檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e233e-114">Optionally receives the fully qualified path of the catalog file within the catalog store.</span></span> <span data-ttu-id="e233e-115">此緩衝區應至少為 (ANSI 版本) 的 **最大 \_ 路徑** 位元組，或 Unicode 版本)  (的字元數。</span><span class="sxs-lookup"><span data-stu-id="e233e-115">This buffer should be at least **MAX\_PATH** bytes (ANSI version) or chars (Unicode version).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e233e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e233e-116">Return value</span></span>

<span data-ttu-id="e233e-117">如果函式成功，則不會傳回 **任何 \_ 錯誤**，否則會傳回 Win32 錯誤碼，指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="e233e-117">If the function succeeds, it returns **NO\_ERROR**; otherwise, it returns a Win32 error code that indicates the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e233e-118">備註</span><span class="sxs-lookup"><span data-stu-id="e233e-118">Remarks</span></span>

<span data-ttu-id="e233e-119">系統會將檔案複製到特殊目錄，並選擇性地重新命名。</span><span class="sxs-lookup"><span data-stu-id="e233e-119">The file is copied by the system into a special directory and is optionally renamed.</span></span>

<span data-ttu-id="e233e-120">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="e233e-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e233e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e233e-121">Requirements</span></span>



| <span data-ttu-id="e233e-122">需求</span><span class="sxs-lookup"><span data-stu-id="e233e-122">Requirement</span></span> | <span data-ttu-id="e233e-123">值</span><span class="sxs-lookup"><span data-stu-id="e233e-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e233e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e233e-124">DLL</span></span><br/> | <dl> <span data-ttu-id="e233e-125"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e233e-125"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e233e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e233e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e233e-127">**CryptCATAdminAddCatalog**</span><span class="sxs-lookup"><span data-stu-id="e233e-127">**CryptCATAdminAddCatalog**</span></span>](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
