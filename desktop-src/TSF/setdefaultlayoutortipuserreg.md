---
title: SetDefaultLayoutOrTipUserReg 函式
description: 將指定的鍵盤配置或文字服務設定為使用者登錄的預設輸入專案。
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- SetDefaultLayoutOrTipUserReg 函式文字服務架構
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093967"
---
# <a name="setdefaultlayoutortipuserreg-function"></a><span data-ttu-id="18b0e-104">SetDefaultLayoutOrTipUserReg 函式</span><span class="sxs-lookup"><span data-stu-id="18b0e-104">SetDefaultLayoutOrTipUserReg function</span></span>

<span data-ttu-id="18b0e-105">將指定的鍵盤配置或文字服務設定為使用者登錄的預設輸入專案。</span><span class="sxs-lookup"><span data-stu-id="18b0e-105">Sets the specified keyboard layout or a text service as a default input item of the user registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b0e-106">語法</span><span class="sxs-lookup"><span data-stu-id="18b0e-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="18b0e-107">參數</span><span class="sxs-lookup"><span data-stu-id="18b0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b0e-108">*pszUserReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="18b0e-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18b0e-109">使用者的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="18b0e-109">The registry path of the user.</span></span> <span data-ttu-id="18b0e-110">如果此參數為 **Null**， \_ \_ 則會使用 HKEY 目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="18b0e-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="18b0e-111">*pszSystemReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="18b0e-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18b0e-112">系統的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="18b0e-112">The registry path of the system.</span></span> <span data-ttu-id="18b0e-113">如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦系統。</span><span class="sxs-lookup"><span data-stu-id="18b0e-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="18b0e-114">*pszSoftwareReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="18b0e-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18b0e-115">軟體的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="18b0e-115">The registry path of the software.</span></span> <span data-ttu-id="18b0e-116">如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦軟體。</span><span class="sxs-lookup"><span data-stu-id="18b0e-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="18b0e-117">*psz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18b0e-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b0e-118">表示鍵盤配置清單或文字服務配置檔案清單的字串。</span><span class="sxs-lookup"><span data-stu-id="18b0e-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="18b0e-119">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18b0e-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b0e-120">指定下列旗標的位位：</span><span class="sxs-lookup"><span data-stu-id="18b0e-120">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="18b0e-121">下列識別碼未在公用標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="18b0e-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="18b0e-122">您必須使用十六進位值或 \# 定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="18b0e-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="18b0e-123">例如，若要使用 SDLOT \_ NOAPPLYTOCURRENTSESSION，您必須 \# \_ 在程式碼中包含定義 SDLOT NOAPPLYTOCURRENTSESSION 0x00000001。</span><span class="sxs-lookup"><span data-stu-id="18b0e-123">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="18b0e-124">值</span><span class="sxs-lookup"><span data-stu-id="18b0e-124">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="18b0e-125">意義</span><span class="sxs-lookup"><span data-stu-id="18b0e-125">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="18b0e-126"><dt>**SDLOT \_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="18b0e-126"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="18b0e-127">將設定儲存在登錄中，但無法更新目前會話的執行時間鍵盤設定。</span><span class="sxs-lookup"><span data-stu-id="18b0e-127">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="18b0e-128">如果在 **SetDefaultLayoutOrTipUserReg** 中設定了替代登錄路徑，則應該設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="18b0e-128">If the alternative registry path is set in **SetDefaultLayoutOrTipUserReg**, this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="18b0e-129"><dt>**SDLOT \_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="18b0e-129"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="18b0e-130">立即在目前的執行緒上套用設定。</span><span class="sxs-lookup"><span data-stu-id="18b0e-130">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b0e-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="18b0e-131">Return value</span></span>



| <span data-ttu-id="18b0e-132">傳回碼</span><span class="sxs-lookup"><span data-stu-id="18b0e-132">Return code</span></span>                                                                          | <span data-ttu-id="18b0e-133">Description</span><span class="sxs-lookup"><span data-stu-id="18b0e-133">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="18b0e-134"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="18b0e-134"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="18b0e-135">函數成功。</span><span class="sxs-lookup"><span data-stu-id="18b0e-135">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="18b0e-136"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="18b0e-136"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="18b0e-137">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="18b0e-137">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="18b0e-138">備註</span><span class="sxs-lookup"><span data-stu-id="18b0e-138">Remarks</span></span>

<span data-ttu-id="18b0e-139">版面配置清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="18b0e-139">The string format of the layout list is:</span></span>

<span data-ttu-id="18b0e-140"><LangID 1>： <KLID 1>; \[...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="18b0e-140"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="18b0e-141">文字服務配置檔案清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="18b0e-141">The string format of the text service profile list is:</span></span>

<span data-ttu-id="18b0e-142">&lt;LangID 1&gt;： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}; < a0/</span><span class="sxs-lookup"><span data-stu-id="18b0e-142"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="18b0e-143">以下是 *psz* 參數值的範例：</span><span class="sxs-lookup"><span data-stu-id="18b0e-143">The following is an example of a value for the *psz* parameter:</span></span>


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="18b0e-144">範例</span><span class="sxs-lookup"><span data-stu-id="18b0e-144">Examples</span></span>

<span data-ttu-id="18b0e-145">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="18b0e-145">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="18b0e-146">下列範例示範如何取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="18b0e-146">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="18b0e-147">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="18b0e-147">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="18b0e-148">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="18b0e-148">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="18b0e-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="18b0e-149">Requirements</span></span>



| <span data-ttu-id="18b0e-150">需求</span><span class="sxs-lookup"><span data-stu-id="18b0e-150">Requirement</span></span> | <span data-ttu-id="18b0e-151">值</span><span class="sxs-lookup"><span data-stu-id="18b0e-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="18b0e-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18b0e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="18b0e-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18b0e-153">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="18b0e-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18b0e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="18b0e-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18b0e-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="18b0e-156">DLL</span><span class="sxs-lookup"><span data-stu-id="18b0e-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18b0e-157"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18b0e-157"><dt>Input.dll</dt></span></span> </dl> |



 

