---
title: SaveDefaultUserInputSettings 函式
description: 將使用者鍵盤配置和文字服務設定套用至預設使用者 hive。
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- SaveDefaultUserInputSettings 函式文字服務架構
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384234"
---
# <a name="savedefaultuserinputsettings-function"></a><span data-ttu-id="361c2-104">SaveDefaultUserInputSettings 函式</span><span class="sxs-lookup"><span data-stu-id="361c2-104">SaveDefaultUserInputSettings function</span></span>

<span data-ttu-id="361c2-105">將使用者鍵盤配置和文字服務設定套用至預設使用者 hive。</span><span class="sxs-lookup"><span data-stu-id="361c2-105">Applies the user keyboard layout and text service setting to the default user hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="361c2-106">語法</span><span class="sxs-lookup"><span data-stu-id="361c2-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="361c2-107">參數</span><span class="sxs-lookup"><span data-stu-id="361c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="361c2-108">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="361c2-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="361c2-109">警告對話方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="361c2-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="361c2-110">警告對話方塊不一定會顯示出來，而且會適當地出現。</span><span class="sxs-lookup"><span data-stu-id="361c2-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="361c2-111">如果此參數為 Null，則不會顯示警告對話方塊。</span><span class="sxs-lookup"><span data-stu-id="361c2-111">If this parameter is NULL, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="361c2-112">*hSourceRegKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="361c2-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="361c2-113">要複製之使用者設定的根登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="361c2-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="361c2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="361c2-114">Return value</span></span>



| <span data-ttu-id="361c2-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="361c2-115">Return code</span></span>                                                                          | <span data-ttu-id="361c2-116">Description</span><span class="sxs-lookup"><span data-stu-id="361c2-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="361c2-117"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="361c2-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="361c2-118">函數成功。</span><span class="sxs-lookup"><span data-stu-id="361c2-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="361c2-119"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="361c2-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="361c2-120">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="361c2-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="361c2-121">範例</span><span class="sxs-lookup"><span data-stu-id="361c2-121">Examples</span></span>

<span data-ttu-id="361c2-122">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="361c2-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="361c2-123">下列範例示範如何取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="361c2-123">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="361c2-124">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="361c2-124">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="361c2-125">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="361c2-125">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="361c2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="361c2-126">Requirements</span></span>



| <span data-ttu-id="361c2-127">需求</span><span class="sxs-lookup"><span data-stu-id="361c2-127">Requirement</span></span> | <span data-ttu-id="361c2-128">值</span><span class="sxs-lookup"><span data-stu-id="361c2-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="361c2-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="361c2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="361c2-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="361c2-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="361c2-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="361c2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="361c2-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="361c2-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="361c2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="361c2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="361c2-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="361c2-134"><dt>Input.dll</dt></span></span> </dl> |



 

