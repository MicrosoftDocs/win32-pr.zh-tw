---
title: SetDefaultLayoutOrTip 函式
description: 將指定的鍵盤配置或文字服務設定為目前使用者的預設輸入專案。
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- SetDefaultLayoutOrTip 函式文字服務架構
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094143"
---
# <a name="setdefaultlayoutortip-function"></a><span data-ttu-id="6d3c9-104">SetDefaultLayoutOrTip 函式</span><span class="sxs-lookup"><span data-stu-id="6d3c9-104">SetDefaultLayoutOrTip function</span></span>

<span data-ttu-id="6d3c9-105">將指定的鍵盤配置或文字服務設定為目前使用者的預設輸入專案。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-105">Sets the specified keyboard layout or a text service as the default input item of the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3c9-106">語法</span><span class="sxs-lookup"><span data-stu-id="6d3c9-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6d3c9-107">參數</span><span class="sxs-lookup"><span data-stu-id="6d3c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d3c9-108">*psz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6d3c9-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3c9-109">表示鍵盤配置清單或文字服務配置檔案清單的字串。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="6d3c9-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6d3c9-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3c9-111">指定下列旗標的位位。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-111">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="6d3c9-112">下列識別碼未在公用標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="6d3c9-113">您必須使用十六進位值或 \# 定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="6d3c9-114">例如，若要使用 SDLOT \_ NOAPPLYTOCURRENTSESSION，您必須 \# \_ 在程式碼中包含定義 SDLOT NOAPPLYTOCURRENTSESSION 0x00000001。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-114">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="6d3c9-115">值</span><span class="sxs-lookup"><span data-stu-id="6d3c9-115">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="6d3c9-116">意義</span><span class="sxs-lookup"><span data-stu-id="6d3c9-116">Meaning</span></span>                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="6d3c9-117"><dt>**SDLOT \_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c9-117"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6d3c9-118">將設定儲存在登錄中，但無法更新目前會話的執行時間鍵盤設定。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-118">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="6d3c9-119">如果在 [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg)中設定了替代登錄路徑，則應該設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-119">If the alternative registry path is set in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="6d3c9-120"><dt>**SDLOT \_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c9-120"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="6d3c9-121">立即在目前的執行緒上套用設定。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-121">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d3c9-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d3c9-122">Return value</span></span>



| <span data-ttu-id="6d3c9-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6d3c9-123">Return code</span></span>                                                                          | <span data-ttu-id="6d3c9-124">Description</span><span class="sxs-lookup"><span data-stu-id="6d3c9-124">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="6d3c9-125"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c9-125"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="6d3c9-126">函數成功。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-126">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="6d3c9-127"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c9-127"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="6d3c9-128">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-128">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d3c9-129">備註</span><span class="sxs-lookup"><span data-stu-id="6d3c9-129">Remarks</span></span>

<span data-ttu-id="6d3c9-130">版面配置清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="6d3c9-130">The string format of the layout list is:</span></span>

<span data-ttu-id="6d3c9-131"><LangID 1>： <KLID 1>; \[...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="6d3c9-131"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="6d3c9-132">文字服務配置檔案清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="6d3c9-132">The string format of the text service profile list is:</span></span>

<span data-ttu-id="6d3c9-133">&lt;LangID 1&gt;： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}; < a0/</span><span class="sxs-lookup"><span data-stu-id="6d3c9-133"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="6d3c9-134">以下是 *psz* 參數值的範例：</span><span class="sxs-lookup"><span data-stu-id="6d3c9-134">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="6d3c9-135">範例</span><span class="sxs-lookup"><span data-stu-id="6d3c9-135">Examples</span></span>

<span data-ttu-id="6d3c9-136">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-136">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="6d3c9-137">下列範例示範如何取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-137">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="6d3c9-138">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-138">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="6d3c9-139">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6d3c9-139">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="6d3c9-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d3c9-140">Requirements</span></span>



| <span data-ttu-id="6d3c9-141">需求</span><span class="sxs-lookup"><span data-stu-id="6d3c9-141">Requirement</span></span> | <span data-ttu-id="6d3c9-142">值</span><span class="sxs-lookup"><span data-stu-id="6d3c9-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3c9-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d3c9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6d3c9-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d3c9-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6d3c9-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d3c9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6d3c9-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d3c9-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6d3c9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="6d3c9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d3c9-148"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c9-148"><dt>Input.dll</dt></span></span> </dl> |



 

