---
title: EnumEnabledLayoutOrTip 函式
description: 列舉所指定使用者設定的所有已啟用鍵盤配置或文字服務。
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- EnumEnabledLayoutOrTip 函式文字服務架構
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968962"
---
# <a name="enumenabledlayoutortip-function"></a><span data-ttu-id="d032e-104">EnumEnabledLayoutOrTip 函式</span><span class="sxs-lookup"><span data-stu-id="d032e-104">EnumEnabledLayoutOrTip function</span></span>

<span data-ttu-id="d032e-105">列舉所指定使用者設定的所有已啟用鍵盤配置或文字服務。</span><span class="sxs-lookup"><span data-stu-id="d032e-105">Enumerates all enabled keyboard layouts or text services of the specified user setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="d032e-106">語法</span><span class="sxs-lookup"><span data-stu-id="d032e-106">Syntax</span></span>


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a><span data-ttu-id="d032e-107">參數</span><span class="sxs-lookup"><span data-stu-id="d032e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d032e-108">*pszUserReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d032e-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d032e-109">使用者的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="d032e-109">The registry path of the user.</span></span> <span data-ttu-id="d032e-110">如果此參數為 **Null**， \_ \_ 則會使用 HKEY 目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="d032e-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="d032e-111">*pszSystemReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d032e-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d032e-112">系統的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="d032e-112">The registry path of the system.</span></span> <span data-ttu-id="d032e-113">如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦系統。</span><span class="sxs-lookup"><span data-stu-id="d032e-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="d032e-114">*pszSoftwareReg* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d032e-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d032e-115">軟體的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="d032e-115">The registry path of the software.</span></span> <span data-ttu-id="d032e-116">如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦軟體。</span><span class="sxs-lookup"><span data-stu-id="d032e-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="d032e-117">*pLayoutOrTipProfile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d032e-117">*pLayoutOrTipProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d032e-118">接收 LAYOUTORTIPPROFILE 陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="d032e-118">Pointer to the buffer that receives the LAYOUTORTIPPROFILE array.</span></span>

</dd> <dt>

<span data-ttu-id="d032e-119">*uBufLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d032e-119">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d032e-120">*PLayoutOrTipProfile* 所指向的緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="d032e-120">The length of the buffer pointed to by *pLayoutOrTipProfile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d032e-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="d032e-121">Return value</span></span>

<span data-ttu-id="d032e-122">如果 *pLayoutOrTipProfile* 為 **Null**，則為使用者設定中啟用的鍵盤專案數目;否則，會複製到 *pLayoutOrTipProfile* 中的鍵盤專案數目。</span><span class="sxs-lookup"><span data-stu-id="d032e-122">If *pLayoutOrTipProfile* is **NULL**, the number of keyboard items that are enabled in the user setting; otherwise, the number of keyboard items that are copied into *pLayoutOrTipProfile*.</span></span>

<span data-ttu-id="d032e-123">針對輸入法 (IME) 語言，即使只有一個 IME 啟用，也會傳回所有的 ime。</span><span class="sxs-lookup"><span data-stu-id="d032e-123">For Input Method Editor (IME) languages, all IMEs are returned, even when only one IME is enabled.</span></span> <span data-ttu-id="d032e-124">例如，如果使用者已啟用 CHT New Quick IME， **EnumEnabledLayoutOrTip** 函式會傳回所有5個 CHT 的 ime。</span><span class="sxs-lookup"><span data-stu-id="d032e-124">For example, if a user has the CHT New Quick IME enabled, the **EnumEnabledLayoutOrTip** function returns all 5 CHT IMEs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d032e-125">備註</span><span class="sxs-lookup"><span data-stu-id="d032e-125">Remarks</span></span>

<span data-ttu-id="d032e-126">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="d032e-126">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="d032e-127">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="d032e-127">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="d032e-128">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d032e-128">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="d032e-129">LAYOUTORTIPPROFILE 的定義如下：</span><span class="sxs-lookup"><span data-stu-id="d032e-129">The definition of LAYOUTORTIPPROFILE is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a><span data-ttu-id="d032e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d032e-130">Requirements</span></span>



| <span data-ttu-id="d032e-131">需求</span><span class="sxs-lookup"><span data-stu-id="d032e-131">Requirement</span></span> | <span data-ttu-id="d032e-132">值</span><span class="sxs-lookup"><span data-stu-id="d032e-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d032e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d032e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d032e-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d032e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d032e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d032e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d032e-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d032e-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d032e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d032e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d032e-138"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d032e-138"><dt>Input.dll</dt></span></span> </dl> |



 

