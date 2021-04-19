---
description: 將檔案 URL 轉換成 Microsoft MS-DOS 路徑。
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MFCreatePathFromURL 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971454"
---
# <a name="mfcreatepathfromurl-function"></a><span data-ttu-id="ef0af-103">MFCreatePathFromURL 函式</span><span class="sxs-lookup"><span data-stu-id="ef0af-103">MFCreatePathFromURL function</span></span>

<span data-ttu-id="ef0af-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ef0af-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ef0af-105">相反地，應用程式應該呼叫 [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla)。\]</span><span class="sxs-lookup"><span data-stu-id="ef0af-105">Instead, applications should call [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span></span>

<span data-ttu-id="ef0af-106">將檔案 URL 轉換成 Microsoft MS-DOS 路徑。</span><span class="sxs-lookup"><span data-stu-id="ef0af-106">Converts a file URL to a Microsoft MS-DOS path.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0af-107">語法</span><span class="sxs-lookup"><span data-stu-id="ef0af-107">Syntax</span></span>


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a><span data-ttu-id="ef0af-108">參數</span><span class="sxs-lookup"><span data-stu-id="ef0af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef0af-109">*pwszFileURL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ef0af-109">*pwszFileURL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0af-110">包含 URL 之以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="ef0af-110">A null-terminated string that contains the URL.</span></span> <span data-ttu-id="ef0af-111">字串的最大長度為 **網際網路 \_ 最大 \_ URL \_ 長度**。</span><span class="sxs-lookup"><span data-stu-id="ef0af-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="ef0af-112">*ppwszFilePath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ef0af-112">*ppwszFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0af-113">接收包含 URL 的以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="ef0af-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="ef0af-114">呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放字串。</span><span class="sxs-lookup"><span data-stu-id="ef0af-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef0af-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef0af-115">Return value</span></span>

<span data-ttu-id="ef0af-116">函數會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ef0af-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="ef0af-117">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ef0af-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef0af-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ef0af-118">Return code</span></span>                                                                                  | <span data-ttu-id="ef0af-119">Description</span><span class="sxs-lookup"><span data-stu-id="ef0af-119">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef0af-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ef0af-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ef0af-121">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="ef0af-121">The function succeeded.</span></span> <br/>                                                                         |
| <dl> <span data-ttu-id="ef0af-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ef0af-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ef0af-123">無效引數。</span><span class="sxs-lookup"><span data-stu-id="ef0af-123">Invalid argument.</span></span> <span data-ttu-id="ef0af-124">*PwszFileURL* 參數中提供的字串無法轉換成路徑。</span><span class="sxs-lookup"><span data-stu-id="ef0af-124">The string given in the *pwszFileURL* parameter cannot be converted to a path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef0af-125">備註</span><span class="sxs-lookup"><span data-stu-id="ef0af-125">Remarks</span></span>

<span data-ttu-id="ef0af-126">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="ef0af-126">This function has no associated import library.</span></span> <span data-ttu-id="ef0af-127">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Mfplat.dll。</span><span class="sxs-lookup"><span data-stu-id="ef0af-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef0af-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef0af-128">Requirements</span></span>



| <span data-ttu-id="ef0af-129">需求</span><span class="sxs-lookup"><span data-stu-id="ef0af-129">Requirement</span></span> | <span data-ttu-id="ef0af-130">值</span><span class="sxs-lookup"><span data-stu-id="ef0af-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0af-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef0af-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0af-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef0af-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef0af-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef0af-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0af-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef0af-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef0af-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ef0af-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0af-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef0af-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef0af-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef0af-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0af-138">媒體基礎函式</span><span class="sxs-lookup"><span data-stu-id="ef0af-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
