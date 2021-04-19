---
description: 驗證單一類別目錄檔案。
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992381"
---
# <a name="verifycatalogfile-function"></a><span data-ttu-id="5944e-103">VerifyCatalogFile 函式</span><span class="sxs-lookup"><span data-stu-id="5944e-103">VerifyCatalogFile function</span></span>

<span data-ttu-id="5944e-104">\[這項功能不受支援，因此不應該使用。\]</span><span class="sxs-lookup"><span data-stu-id="5944e-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="5944e-105">驗證單一類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="5944e-105">Verifies a single catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5944e-106">語法</span><span class="sxs-lookup"><span data-stu-id="5944e-106">Syntax</span></span>


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="5944e-107">參數</span><span class="sxs-lookup"><span data-stu-id="5944e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5944e-108">*CatalogFullPath*</span><span class="sxs-lookup"><span data-stu-id="5944e-108">*CatalogFullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="5944e-109">要驗證之類別目錄檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5944e-109">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5944e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5944e-110">Return value</span></span>

<span data-ttu-id="5944e-111">如果函式成功，則會傳回 **錯誤 \_ 成功**; 否則，它會從 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5944e-111">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

<span data-ttu-id="5944e-112">如果目錄是 Authenticode 簽署的目錄，則此函式會在成功時傳回 **錯誤 \_ authenticode \_ 受信任 \_ 發行者** ; 否則，它會傳回 **錯誤 \_ authenticode \_ 信任 \_ 未 \_ 建立**。</span><span class="sxs-lookup"><span data-stu-id="5944e-112">If the catalog is an Authenticode-signed catalog, this function returns **ERROR\_AUTHENTICODE\_TRUSTED\_PUBLISHER** if it succeeds; otherwise, it returns **ERROR\_AUTHENTICODE\_TRUST\_NOT\_ESTABLISHED**.</span></span>

<span data-ttu-id="5944e-113">如果函式無法判斷發行者是否受信任，則可能也會傳回 **錯誤 \_ 不明 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="5944e-113">If the function is unable to determine whether the publisher is trusted, it may also return **ERROR\_UNIDENTIFIED\_ERROR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5944e-114">備註</span><span class="sxs-lookup"><span data-stu-id="5944e-114">Remarks</span></span>

<span data-ttu-id="5944e-115">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5944e-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5944e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5944e-116">Requirements</span></span>



| <span data-ttu-id="5944e-117">需求</span><span class="sxs-lookup"><span data-stu-id="5944e-117">Requirement</span></span> | <span data-ttu-id="5944e-118">值</span><span class="sxs-lookup"><span data-stu-id="5944e-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5944e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5944e-119">DLL</span></span><br/> | <dl> <span data-ttu-id="5944e-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5944e-120"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
