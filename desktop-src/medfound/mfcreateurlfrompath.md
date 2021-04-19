---
description: 將 Microsoft MS-DOS 路徑轉換成正式的 URL。
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966765"
---
# <a name="mfcreateurlfrompath-function"></a><span data-ttu-id="a04fe-103">MFCreateURLFromPath 函式</span><span class="sxs-lookup"><span data-stu-id="a04fe-103">MFCreateURLFromPath function</span></span>

<span data-ttu-id="a04fe-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a04fe-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a04fe-105">相反地，應用程式應該呼叫 [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha)。\]</span><span class="sxs-lookup"><span data-stu-id="a04fe-105">Instead, Applications should call [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span></span>

<span data-ttu-id="a04fe-106">將 Microsoft MS-DOS 路徑轉換成正式的 URL。</span><span class="sxs-lookup"><span data-stu-id="a04fe-106">Converts a Microsoft MS-DOS path to a canonicalized URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04fe-107">語法</span><span class="sxs-lookup"><span data-stu-id="a04fe-107">Syntax</span></span>


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a><span data-ttu-id="a04fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="a04fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04fe-109">*pwszFilePath* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a04fe-109">*pwszFilePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a04fe-110">包含路徑之以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="a04fe-110">A null-terminated string that contains the path.</span></span> <span data-ttu-id="a04fe-111">字串的最大長度為 **網際網路 \_ 最大 \_ URL \_ 長度**。</span><span class="sxs-lookup"><span data-stu-id="a04fe-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="a04fe-112">*ppwszFileURL* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a04fe-112">*ppwszFileURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a04fe-113">接收包含 URL 的以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="a04fe-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="a04fe-114">呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放字串。</span><span class="sxs-lookup"><span data-stu-id="a04fe-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04fe-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a04fe-115">Return value</span></span>

<span data-ttu-id="a04fe-116">函數會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="a04fe-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="a04fe-117">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="a04fe-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a04fe-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a04fe-118">Return code</span></span>                                                                             | <span data-ttu-id="a04fe-119">Description</span><span class="sxs-lookup"><span data-stu-id="a04fe-119">Description</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a04fe-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="a04fe-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a04fe-121">*PwszFilePath* 參數中提供的字串已經是 URL 格式。</span><span class="sxs-lookup"><span data-stu-id="a04fe-121">The string given in the *pwszFilePath* parameter is already in URL format.</span></span> <span data-ttu-id="a04fe-122">在此情況下， *pszFilePath* 只會複製到 *ppszFileURL* 而不需要修改。</span><span class="sxs-lookup"><span data-stu-id="a04fe-122">In this case, *pszFilePath* is simply copied to *ppszFileURL* without modification.</span></span><br/> |
| <dl> <span data-ttu-id="a04fe-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a04fe-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a04fe-124">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="a04fe-124">The function succeeded.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="a04fe-125">備註</span><span class="sxs-lookup"><span data-stu-id="a04fe-125">Remarks</span></span>

<span data-ttu-id="a04fe-126">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="a04fe-126">This function has no associated import library.</span></span> <span data-ttu-id="a04fe-127">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Mfplat.dll。</span><span class="sxs-lookup"><span data-stu-id="a04fe-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a04fe-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a04fe-128">Requirements</span></span>



| <span data-ttu-id="a04fe-129">需求</span><span class="sxs-lookup"><span data-stu-id="a04fe-129">Requirement</span></span> | <span data-ttu-id="a04fe-130">值</span><span class="sxs-lookup"><span data-stu-id="a04fe-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a04fe-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a04fe-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a04fe-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a04fe-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a04fe-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a04fe-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a04fe-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a04fe-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a04fe-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a04fe-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a04fe-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a04fe-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04fe-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a04fe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04fe-138">媒體基礎函式</span><span class="sxs-lookup"><span data-stu-id="a04fe-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
