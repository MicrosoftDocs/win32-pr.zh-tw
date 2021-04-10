---
title: InstallLayoutOrTipUserReg 函式
description: 為指定的使用者啟用指定的鍵盤配置或文字服務。
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- InstallLayoutOrTipUserReg 函式文字服務架構
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685939"
---
# <a name="installlayoutortipuserreg-function"></a><span data-ttu-id="ef8a9-104">InstallLayoutOrTipUserReg 函式</span><span class="sxs-lookup"><span data-stu-id="ef8a9-104">InstallLayoutOrTipUserReg function</span></span>

<span data-ttu-id="ef8a9-105">為指定的使用者啟用指定的鍵盤配置或文字服務。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-105">Enables the specified keyboard layouts or text services for the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef8a9-106">語法</span><span class="sxs-lookup"><span data-stu-id="ef8a9-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ef8a9-107">參數</span><span class="sxs-lookup"><span data-stu-id="ef8a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef8a9-108">*pszUserReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ef8a9-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8a9-109">使用者的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-109">The registry path of the user.</span></span> <span data-ttu-id="ef8a9-110">如果此參數為 **Null**， \_ \_ 則會使用 HKEY 目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="ef8a9-111">*pszSystemReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ef8a9-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8a9-112">系統的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-112">The registry path of the system.</span></span> <span data-ttu-id="ef8a9-113">如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦系統。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="ef8a9-114">*pszSoftwareReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ef8a9-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8a9-115">軟體的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-115">The registry path of the software.</span></span> <span data-ttu-id="ef8a9-116">如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦軟體。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="ef8a9-117">*psz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef8a9-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8a9-118">表示鍵盤配置清單或文字服務配置檔案清單的字串。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="ef8a9-119">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef8a9-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8a9-120">指定下列旗標的位位。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-120">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="ef8a9-121">下列識別碼未在公用標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="ef8a9-122">您必須使用十六進位值或 \# 定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="ef8a9-123">例如，若要使用 **ILOT \_ 卸載** ，您必須 `#define ILOT_UNINSTALL 0x00000001` 將程式碼包含在程式碼中。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-123">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="ef8a9-124">值</span><span class="sxs-lookup"><span data-stu-id="ef8a9-124">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="ef8a9-125">意義</span><span class="sxs-lookup"><span data-stu-id="ef8a9-125">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="ef8a9-126"><dt>**ILOT \_卸載**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ef8a9-126"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="ef8a9-127">與 **ILOT \_ 已停用**。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-127">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="ef8a9-128"><dt>**ILOT \_DEFPROFILE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ef8a9-128"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="ef8a9-129">將指定的版面配置或提示設定為預設專案。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-129">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="ef8a9-130"><dt>**ILOT \_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="ef8a9-130"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="ef8a9-131">這項設定會儲存，但不會套用到目前的會話。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-131">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="ef8a9-132"><dt>**ILOT \_CLEANINSTALL**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="ef8a9-132"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="ef8a9-133">停用所有目前的鍵盤配置和文字服務。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-133">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="ef8a9-134"><dt>**ILOT \_停用**</dt>的 <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="ef8a9-134"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="ef8a9-135">停用指定的鍵盤配置和文字服務。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-135">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef8a9-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef8a9-136">Return value</span></span>



| <span data-ttu-id="ef8a9-137">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ef8a9-137">Return code</span></span>                                                                         | <span data-ttu-id="ef8a9-138">Description</span><span class="sxs-lookup"><span data-stu-id="ef8a9-138">Description</span></span>                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ef8a9-139"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="ef8a9-139"><dt>**TRUE**</dt></span></span> </dl> | <span data-ttu-id="ef8a9-140">函數成功。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-140">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="ef8a9-141"><dt>**FASE**</dt></span><span class="sxs-lookup"><span data-stu-id="ef8a9-141"><dt>**FASE**</dt></span></span> </dl> | <span data-ttu-id="ef8a9-142">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-142">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef8a9-143">備註</span><span class="sxs-lookup"><span data-stu-id="ef8a9-143">Remarks</span></span>

<span data-ttu-id="ef8a9-144">版面配置清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="ef8a9-144">The string format of the layout list is:</span></span>

<span data-ttu-id="ef8a9-145"><LangID 1>： <KLID 1>; \[...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="ef8a9-145"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="ef8a9-146">文字服務配置檔案清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="ef8a9-146">The string format of the text service profile list is:</span></span>

<span data-ttu-id="ef8a9-147">&lt;LangID 1&gt;： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}; < a0/</span><span class="sxs-lookup"><span data-stu-id="ef8a9-147"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="ef8a9-148">以下是 *psz* 參數值的範例：</span><span class="sxs-lookup"><span data-stu-id="ef8a9-148">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="ef8a9-149">範例</span><span class="sxs-lookup"><span data-stu-id="ef8a9-149">Examples</span></span>

<span data-ttu-id="ef8a9-150">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-150">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="ef8a9-151">下列範例示範如何取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-151">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="ef8a9-152">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-152">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="ef8a9-153">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef8a9-153">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="ef8a9-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef8a9-154">Requirements</span></span>



| <span data-ttu-id="ef8a9-155">需求</span><span class="sxs-lookup"><span data-stu-id="ef8a9-155">Requirement</span></span> | <span data-ttu-id="ef8a9-156">值</span><span class="sxs-lookup"><span data-stu-id="ef8a9-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8a9-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef8a9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ef8a9-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef8a9-158">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ef8a9-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef8a9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ef8a9-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef8a9-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ef8a9-161">DLL</span><span class="sxs-lookup"><span data-stu-id="ef8a9-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef8a9-162"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef8a9-162"><dt>Input.dll</dt></span></span> </dl> |



 

