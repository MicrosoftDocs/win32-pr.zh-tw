---
title: TF_InvalidAssemblyListCacheIfExist 函式
description: TF InvalidAssemblyListCacheIfExist 函式會 \_ 使文字輸入處理器的描述快取失效。
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- TF_InvalidAssemblyListCacheIfExist 函式文字服務架構
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508436"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a><span data-ttu-id="75261-104">TF \_ InvalidAssemblyListCacheIfExist 函式</span><span class="sxs-lookup"><span data-stu-id="75261-104">TF\_InvalidAssemblyListCacheIfExist function</span></span>

<span data-ttu-id="75261-105">**TF \_ InvalidAssemblyListCacheIfExist** 函式會使文字輸入處理器的描述快取失效。</span><span class="sxs-lookup"><span data-stu-id="75261-105">The **TF\_InvalidAssemblyListCacheIfExist** function invalidates the text input processor's description cache.</span></span> <span data-ttu-id="75261-106">如果輸入處理器安裝程式要求您重新開機或登入，就不需要呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="75261-106">It is not necessary to call this function if the input processor setup program requires you to restart or log on.</span></span> <span data-ttu-id="75261-107">快取在使用者登出之前有效。</span><span class="sxs-lookup"><span data-stu-id="75261-107">The cache is valid until the user logs off.</span></span>

## <a name="syntax"></a><span data-ttu-id="75261-108">語法</span><span class="sxs-lookup"><span data-stu-id="75261-108">Syntax</span></span>


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a><span data-ttu-id="75261-109">參數</span><span class="sxs-lookup"><span data-stu-id="75261-109">Parameters</span></span>

<span data-ttu-id="75261-110">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="75261-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75261-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="75261-111">Return value</span></span>

<span data-ttu-id="75261-112">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="75261-112">This function can return one of these values.</span></span>



| <span data-ttu-id="75261-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="75261-113">Return code</span></span>                                                                            | <span data-ttu-id="75261-114">Description</span><span class="sxs-lookup"><span data-stu-id="75261-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="75261-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="75261-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="75261-116">函數成功。</span><span class="sxs-lookup"><span data-stu-id="75261-116">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="75261-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="75261-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="75261-118">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="75261-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="75261-119">範例</span><span class="sxs-lookup"><span data-stu-id="75261-119">Examples</span></span>

<span data-ttu-id="75261-120">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="75261-120">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="75261-121">下列範例示範如何取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="75261-121">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="75261-122">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="75261-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="75261-123">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="75261-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a><span data-ttu-id="75261-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="75261-124">Requirements</span></span>



| <span data-ttu-id="75261-125">需求</span><span class="sxs-lookup"><span data-stu-id="75261-125">Requirement</span></span> | <span data-ttu-id="75261-126">值</span><span class="sxs-lookup"><span data-stu-id="75261-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75261-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75261-127">Minimum supported client</span></span><br/> | <span data-ttu-id="75261-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75261-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="75261-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75261-129">Minimum supported server</span></span><br/> | <span data-ttu-id="75261-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75261-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75261-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="75261-131">Redistributable</span></span><br/>          | <span data-ttu-id="75261-132">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="75261-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="75261-133">DLL</span><span class="sxs-lookup"><span data-stu-id="75261-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75261-134"><dt>Msctf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75261-134"><dt>Msctf.dll</dt></span></span> </dl> |



 

