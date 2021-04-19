---
title: InstallLayoutOrTip 函式
description: 啟用指定的鍵盤配置或文字服務。
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- InstallLayoutOrTip 函式文字服務架構
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966314"
---
# <a name="installlayoutortip-function"></a><span data-ttu-id="9af80-104">InstallLayoutOrTip 函式</span><span class="sxs-lookup"><span data-stu-id="9af80-104">InstallLayoutOrTip function</span></span>

<span data-ttu-id="9af80-105">啟用指定的鍵盤配置或文字服務。</span><span class="sxs-lookup"><span data-stu-id="9af80-105">Enables the specified keyboard layouts or text services.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af80-106">語法</span><span class="sxs-lookup"><span data-stu-id="9af80-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9af80-107">參數</span><span class="sxs-lookup"><span data-stu-id="9af80-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af80-108">*psz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9af80-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af80-109">表示鍵盤配置清單或文字服務配置檔案清單的字串。</span><span class="sxs-lookup"><span data-stu-id="9af80-109">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="9af80-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9af80-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af80-111">指定下列旗標的位位：</span><span class="sxs-lookup"><span data-stu-id="9af80-111">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="9af80-112">下列識別碼未在公用標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="9af80-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="9af80-113">您必須使用十六進位值或 \# 定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="9af80-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="9af80-114">例如，若要使用 **ILOT \_ 卸載** ，您必須 `#define ILOT_UNINSTALL 0x00000001` 將程式碼包含在程式碼中。</span><span class="sxs-lookup"><span data-stu-id="9af80-114">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="9af80-115">值</span><span class="sxs-lookup"><span data-stu-id="9af80-115">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="9af80-116">意義</span><span class="sxs-lookup"><span data-stu-id="9af80-116">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="9af80-117"><dt>**ILOT \_卸載**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-117"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="9af80-118">與 **ILOT \_ 已停用**。</span><span class="sxs-lookup"><span data-stu-id="9af80-118">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="9af80-119"><dt>**ILOT \_DEFPROFILE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-119"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="9af80-120">將指定的版面配置或提示設定為預設專案。</span><span class="sxs-lookup"><span data-stu-id="9af80-120">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <span data-ttu-id="9af80-121"><dt>**ILOT \_DEFUSER4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-121"><dt>**ILOT\_DEFUSER4**</dt> <dt>0x00000004</dt></span></span> </dl>                                              | <span data-ttu-id="9af80-122">變更的設定。預設。</span><span class="sxs-lookup"><span data-stu-id="9af80-122">Changes the setting of .Default.</span></span><br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <span data-ttu-id="9af80-123"><dt>**ILOT \_SYSLOCALE**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-123"><dt>**ILOT\_SYSLOCALE**</dt> <dt>0x00000008</dt></span></span> </dl>                                           | <span data-ttu-id="9af80-124">未使用的。</span><span class="sxs-lookup"><span data-stu-id="9af80-124">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <span data-ttu-id="9af80-125"><dt>**ILOT \_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-125"><dt>**ILOT\_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="9af80-126">未使用的。</span><span class="sxs-lookup"><span data-stu-id="9af80-126">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="9af80-127"><dt>**ILOT \_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-127"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="9af80-128">這項設定會儲存，但不會套用到目前的會話。</span><span class="sxs-lookup"><span data-stu-id="9af80-128">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="9af80-129"><dt>**ILOT \_CLEANINSTALL**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-129"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="9af80-130">停用所有目前的鍵盤配置和文字服務。</span><span class="sxs-lookup"><span data-stu-id="9af80-130">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="9af80-131"><dt>**ILOT \_停用**</dt>的 <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-131"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="9af80-132">停用指定的鍵盤配置和文字服務。</span><span class="sxs-lookup"><span data-stu-id="9af80-132">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af80-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="9af80-133">Return value</span></span>



| <span data-ttu-id="9af80-134">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9af80-134">Return code</span></span>                                                                          | <span data-ttu-id="9af80-135">Description</span><span class="sxs-lookup"><span data-stu-id="9af80-135">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9af80-136"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-136"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="9af80-137">函數成功。</span><span class="sxs-lookup"><span data-stu-id="9af80-137">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="9af80-138"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-138"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="9af80-139">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9af80-139">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9af80-140">備註</span><span class="sxs-lookup"><span data-stu-id="9af80-140">Remarks</span></span>

<span data-ttu-id="9af80-141">版面配置清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="9af80-141">The string format of the layout list is:</span></span>

<span data-ttu-id="9af80-142"><LangID 1>： <KLID 1>; \[...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="9af80-142"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="9af80-143">文字服務配置檔案清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="9af80-143">The string format of the text service profile list is:</span></span>

<span data-ttu-id="9af80-144">&lt;LangID 1&gt;： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}; < a0/</span><span class="sxs-lookup"><span data-stu-id="9af80-144"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="9af80-145">以下是 *psz* 參數值的範例：</span><span class="sxs-lookup"><span data-stu-id="9af80-145">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="9af80-146">範例</span><span class="sxs-lookup"><span data-stu-id="9af80-146">Examples</span></span>

<span data-ttu-id="9af80-147">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="9af80-147">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="9af80-148">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="9af80-148">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="9af80-149">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9af80-149">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="9af80-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="9af80-150">Requirements</span></span>



| <span data-ttu-id="9af80-151">需求</span><span class="sxs-lookup"><span data-stu-id="9af80-151">Requirement</span></span> | <span data-ttu-id="9af80-152">值</span><span class="sxs-lookup"><span data-stu-id="9af80-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9af80-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9af80-153">Minimum supported client</span></span><br/> | <span data-ttu-id="9af80-154">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9af80-154">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9af80-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9af80-155">Minimum supported server</span></span><br/> | <span data-ttu-id="9af80-156">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9af80-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9af80-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9af80-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af80-158"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af80-158"><dt>Input.dll</dt></span></span> </dl> |



 

