---
title: QueryLayoutOrTipStringUserReg 函式
description: 查詢指定的字串，這個字串表示指定之登錄路徑的鍵盤配置清單或文字服務配置檔案清單的格式。
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- QueryLayoutOrTipStringUserReg 函式文字服務架構
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966335"
---
# <a name="querylayoutortipstringuserreg-function"></a><span data-ttu-id="27bb8-104">QueryLayoutOrTipStringUserReg 函式</span><span class="sxs-lookup"><span data-stu-id="27bb8-104">QueryLayoutOrTipStringUserReg function</span></span>

<span data-ttu-id="27bb8-105">查詢指定的字串，這個字串表示指定之登錄路徑的鍵盤配置清單或文字服務配置檔案清單的格式。</span><span class="sxs-lookup"><span data-stu-id="27bb8-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list of the specified registry path.</span></span>

## <a name="syntax"></a><span data-ttu-id="27bb8-106">語法</span><span class="sxs-lookup"><span data-stu-id="27bb8-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="27bb8-107">參數</span><span class="sxs-lookup"><span data-stu-id="27bb8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27bb8-108">*pszUserReg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27bb8-108">*pszUserReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bb8-109">使用者的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="27bb8-109">The registry path of the user.</span></span> <span data-ttu-id="27bb8-110">如果此參數為 **Null**， \_ \_ 則會使用 HKEY 目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="27bb8-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="27bb8-111">*pszSystemReg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27bb8-111">*pszSystemReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bb8-112">系統的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="27bb8-112">The registry path of the system.</span></span> <span data-ttu-id="27bb8-113">如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦系統。</span><span class="sxs-lookup"><span data-stu-id="27bb8-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="27bb8-114">*pszSoftwareReg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27bb8-114">*pszSoftwareReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bb8-115">軟體的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="27bb8-115">The registry path of the software.</span></span> <span data-ttu-id="27bb8-116">如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦軟體。</span><span class="sxs-lookup"><span data-stu-id="27bb8-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="27bb8-117">*psz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27bb8-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bb8-118">表示鍵盤配置清單或文字服務配置檔案清單的字串。</span><span class="sxs-lookup"><span data-stu-id="27bb8-118">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="27bb8-119">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27bb8-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bb8-120">這必須是 0。</span><span class="sxs-lookup"><span data-stu-id="27bb8-120">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27bb8-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="27bb8-121">Return value</span></span>

<span data-ttu-id="27bb8-122">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="27bb8-122">This function can return one of these values.</span></span>



| <span data-ttu-id="27bb8-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="27bb8-123">Return code</span></span>                                                                                  | <span data-ttu-id="27bb8-124">Description</span><span class="sxs-lookup"><span data-stu-id="27bb8-124">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27bb8-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="27bb8-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="27bb8-126">**Psz** 中定義的所有版面配置或設定檔都有效。</span><span class="sxs-lookup"><span data-stu-id="27bb8-126">All layouts or profiles defined in **psz** are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="27bb8-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="27bb8-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="27bb8-128">**Psz** 中定義的一或多個版面配置或設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="27bb8-128">One or more of the layouts or profiles defined in **psz** are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27bb8-129">備註</span><span class="sxs-lookup"><span data-stu-id="27bb8-129">Remarks</span></span>

<span data-ttu-id="27bb8-130">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="27bb8-130">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="27bb8-131">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="27bb8-131">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="27bb8-132">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27bb8-132">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="27bb8-133">版面配置清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="27bb8-133">The string format of the layout list is:</span></span>

<span data-ttu-id="27bb8-134"><LangID 1>： <KLID 1>; \[...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="27bb8-134"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="27bb8-135">文字服務配置檔案清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="27bb8-135">The string format of the text service profile list is:</span></span>

<span data-ttu-id="27bb8-136">&lt;LangID 1&gt;： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}; < a0/</span><span class="sxs-lookup"><span data-stu-id="27bb8-136"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="27bb8-137">以下是 *psz* 參數值的範例：</span><span class="sxs-lookup"><span data-stu-id="27bb8-137">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="27bb8-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="27bb8-138">Requirements</span></span>



| <span data-ttu-id="27bb8-139">需求</span><span class="sxs-lookup"><span data-stu-id="27bb8-139">Requirement</span></span> | <span data-ttu-id="27bb8-140">值</span><span class="sxs-lookup"><span data-stu-id="27bb8-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27bb8-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27bb8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="27bb8-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27bb8-142">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="27bb8-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27bb8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="27bb8-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27bb8-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="27bb8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="27bb8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27bb8-146"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27bb8-146"><dt>Input.dll</dt></span></span> </dl> |



 

