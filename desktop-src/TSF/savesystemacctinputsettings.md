---
title: SaveSystemAcctInputSettings 函式
description: 將使用者鍵盤配置和文字服務設定套用至系統帳戶 hive。
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- SaveSystemAcctInputSettings 函式文字服務架構
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383970"
---
# <a name="savesystemacctinputsettings-function"></a><span data-ttu-id="23fa8-104">SaveSystemAcctInputSettings 函式</span><span class="sxs-lookup"><span data-stu-id="23fa8-104">SaveSystemAcctInputSettings function</span></span>

<span data-ttu-id="23fa8-105">將使用者鍵盤配置和文字服務設定套用至系統帳戶 hive。</span><span class="sxs-lookup"><span data-stu-id="23fa8-105">Applies the user keyboard layout and text service setting to the system accounts hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fa8-106">語法</span><span class="sxs-lookup"><span data-stu-id="23fa8-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="23fa8-107">參數</span><span class="sxs-lookup"><span data-stu-id="23fa8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23fa8-108">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23fa8-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23fa8-109">警告對話方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="23fa8-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="23fa8-110">警告對話方塊不一定會顯示出來，而且會適當地出現。</span><span class="sxs-lookup"><span data-stu-id="23fa8-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="23fa8-111">如果此參數為 **Null**，則不會顯示警告對話方塊。</span><span class="sxs-lookup"><span data-stu-id="23fa8-111">If this parameter is **NULL**, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="23fa8-112">*hSourceRegKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23fa8-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23fa8-113">要複製之使用者設定的根登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="23fa8-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23fa8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="23fa8-114">Return value</span></span>



| <span data-ttu-id="23fa8-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="23fa8-115">Return code</span></span>                                                                          | <span data-ttu-id="23fa8-116">Description</span><span class="sxs-lookup"><span data-stu-id="23fa8-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="23fa8-117"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="23fa8-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="23fa8-118">函數成功。</span><span class="sxs-lookup"><span data-stu-id="23fa8-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="23fa8-119"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="23fa8-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="23fa8-120">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="23fa8-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23fa8-121">備註</span><span class="sxs-lookup"><span data-stu-id="23fa8-121">Remarks</span></span>

<span data-ttu-id="23fa8-122">系統帳戶 hive 是 HKEY \_ USERS \\ 。預設值、HKEY \_ 使用者 \\ s-1-5-19，以及 HKEY \_ 使用者 \\ s-1-5-20。</span><span class="sxs-lookup"><span data-stu-id="23fa8-122">The system account hive is HKEY\_USERS\\.DEFAULT, HKEY\_USERS\\S-1-5-19, and HKEY\_USERS\\S-1-5-20.</span></span>

## <a name="examples"></a><span data-ttu-id="23fa8-123">範例</span><span class="sxs-lookup"><span data-stu-id="23fa8-123">Examples</span></span>

<span data-ttu-id="23fa8-124">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="23fa8-124">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="23fa8-125">下列範例示範如何取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="23fa8-125">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="23fa8-126">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="23fa8-126">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="23fa8-127">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="23fa8-127">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="23fa8-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="23fa8-128">Requirements</span></span>



| <span data-ttu-id="23fa8-129">需求</span><span class="sxs-lookup"><span data-stu-id="23fa8-129">Requirement</span></span> | <span data-ttu-id="23fa8-130">值</span><span class="sxs-lookup"><span data-stu-id="23fa8-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23fa8-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23fa8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="23fa8-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23fa8-132">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="23fa8-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23fa8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="23fa8-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23fa8-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="23fa8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="23fa8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23fa8-136"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23fa8-136"><dt>Input.dll</dt></span></span> </dl> |



 

