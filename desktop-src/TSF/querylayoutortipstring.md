---
title: QueryLayoutOrTipString 函式
description: 查詢指定的字串，表示鍵盤配置清單或文字服務配置檔案清單的格式。
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- QueryLayoutOrTipString 函式文字服務架構
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983316"
---
# <a name="querylayoutortipstring-function"></a><span data-ttu-id="55df8-104">QueryLayoutOrTipString 函式</span><span class="sxs-lookup"><span data-stu-id="55df8-104">QueryLayoutOrTipString function</span></span>

<span data-ttu-id="55df8-105">查詢指定的字串，表示鍵盤配置清單或文字服務配置檔案清單的格式。</span><span class="sxs-lookup"><span data-stu-id="55df8-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list.</span></span>

## <a name="syntax"></a><span data-ttu-id="55df8-106">語法</span><span class="sxs-lookup"><span data-stu-id="55df8-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="55df8-107">參數</span><span class="sxs-lookup"><span data-stu-id="55df8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55df8-108">*psz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55df8-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df8-109">表示鍵盤配置清單或文字服務配置檔案清單的字串。</span><span class="sxs-lookup"><span data-stu-id="55df8-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="55df8-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55df8-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55df8-111">這必須是 0。</span><span class="sxs-lookup"><span data-stu-id="55df8-111">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55df8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="55df8-112">Return value</span></span>

<span data-ttu-id="55df8-113">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="55df8-113">This function can return one of these values.</span></span>



| <span data-ttu-id="55df8-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="55df8-114">Return code</span></span>                                                                                  | <span data-ttu-id="55df8-115">Description</span><span class="sxs-lookup"><span data-stu-id="55df8-115">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55df8-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="55df8-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="55df8-117">*Psz* 中定義的所有版面配置或設定檔都有效。</span><span class="sxs-lookup"><span data-stu-id="55df8-117">All layouts or profiles defined in *psz* are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="55df8-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="55df8-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="55df8-119">*Psz* 中定義的一或多個版面配置或設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="55df8-119">One or more of the layouts or profiles defined in *psz* are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55df8-120">備註</span><span class="sxs-lookup"><span data-stu-id="55df8-120">Remarks</span></span>

<span data-ttu-id="55df8-121">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="55df8-121">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="55df8-122">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="55df8-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="55df8-123">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="55df8-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="55df8-124">版面配置清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="55df8-124">The string format of the layout list is:</span></span>

<span data-ttu-id="55df8-125"><LangID 1>： <KLID 1>; \[...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="55df8-125"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="55df8-126">文字服務配置檔案清單的字串格式為：</span><span class="sxs-lookup"><span data-stu-id="55df8-126">The string format of the text service profile list is:</span></span>

<span data-ttu-id="55df8-127">&lt;LangID 1&gt;： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}; < a0/</span><span class="sxs-lookup"><span data-stu-id="55df8-127"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="55df8-128">以下是 *psz* 參數值的範例：</span><span class="sxs-lookup"><span data-stu-id="55df8-128">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="55df8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="55df8-129">Requirements</span></span>



| <span data-ttu-id="55df8-130">需求</span><span class="sxs-lookup"><span data-stu-id="55df8-130">Requirement</span></span> | <span data-ttu-id="55df8-131">值</span><span class="sxs-lookup"><span data-stu-id="55df8-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55df8-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55df8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="55df8-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55df8-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="55df8-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55df8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="55df8-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55df8-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="55df8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="55df8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55df8-137"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55df8-137"><dt>Input.dll</dt></span></span> </dl> |



 

