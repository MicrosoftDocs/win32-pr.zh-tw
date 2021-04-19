---
description: 使用標準作業系統程式碼簽署原則（例如驅動程式簽署）來驗證單一類別目錄檔案。
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: pSetupVerifyCatalogFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995618"
---
# <a name="psetupverifycatalogfile-function"></a><span data-ttu-id="9e2bf-103">pSetupVerifyCatalogFile 函式</span><span class="sxs-lookup"><span data-stu-id="9e2bf-103">pSetupVerifyCatalogFile function</span></span>

<span data-ttu-id="9e2bf-104">\[Microsoft 不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="9e2bf-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="9e2bf-105">若為 INF 檔案 (裝置安裝) ，開發人員應該使用 **SetupVerifyInfFile**。</span><span class="sxs-lookup"><span data-stu-id="9e2bf-105">For an INF file (device install), developers should use **SetupVerifyInfFile**.</span></span> <span data-ttu-id="9e2bf-106">若要驗證非 INF 型類別目錄，請使用 **WinVerifyTrust**。\]</span><span class="sxs-lookup"><span data-stu-id="9e2bf-106">To validate a non-INF based catalog, use **WinVerifyTrust**.\]</span></span>

<span data-ttu-id="9e2bf-107">使用標準作業系統程式碼簽署原則（例如驅動程式簽署）來驗證單一類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="9e2bf-107">Verifies a single catalog file using standard operating system code signing policy, such as driver signing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2bf-108">語法</span><span class="sxs-lookup"><span data-stu-id="9e2bf-108">Syntax</span></span>


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="9e2bf-109">參數</span><span class="sxs-lookup"><span data-stu-id="9e2bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e2bf-110">*CatalogFullPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e2bf-110">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e2bf-111">要驗證之類別目錄檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9e2bf-111">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e2bf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e2bf-112">Return value</span></span>

<span data-ttu-id="9e2bf-113">如果函式成功，則會傳回 **錯誤 \_ 成功**; 否則，它會從 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9e2bf-113">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e2bf-114">備註</span><span class="sxs-lookup"><span data-stu-id="9e2bf-114">Remarks</span></span>

<span data-ttu-id="9e2bf-115">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="9e2bf-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e2bf-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e2bf-116">Requirements</span></span>



| <span data-ttu-id="9e2bf-117">需求</span><span class="sxs-lookup"><span data-stu-id="9e2bf-117">Requirement</span></span> | <span data-ttu-id="9e2bf-118">值</span><span class="sxs-lookup"><span data-stu-id="9e2bf-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2bf-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9e2bf-119">DLL</span></span><br/> | <dl> <span data-ttu-id="9e2bf-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e2bf-120"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e2bf-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e2bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e2bf-122">**SetupVerifyInfFile**</span><span class="sxs-lookup"><span data-stu-id="9e2bf-122">**SetupVerifyInfFile**</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[<span data-ttu-id="9e2bf-123">**WinVerifyTrust**</span><span class="sxs-lookup"><span data-stu-id="9e2bf-123">**WinVerifyTrust**</span></span>](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
