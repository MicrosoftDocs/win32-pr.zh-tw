---
title: EnumLayoutOrTipForSetup 函式
description: 列舉安裝程式 UI 或 OOBE 的已安裝鍵盤配置和文字服務。
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- EnumLayoutOrTipForSetup 函式文字服務架構
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965076"
---
# <a name="enumlayoutortipforsetup-function"></a><span data-ttu-id="da56c-104">EnumLayoutOrTipForSetup 函式</span><span class="sxs-lookup"><span data-stu-id="da56c-104">EnumLayoutOrTipForSetup function</span></span>

<span data-ttu-id="da56c-105">列舉安裝程式 UI 或 OOBE 的已安裝鍵盤配置和文字服務。</span><span class="sxs-lookup"><span data-stu-id="da56c-105">Enumerates the installed keyboard layouts and text services of the setup UI or OOBE.</span></span>

## <a name="syntax"></a><span data-ttu-id="da56c-106">語法</span><span class="sxs-lookup"><span data-stu-id="da56c-106">Syntax</span></span>


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="da56c-107">參數</span><span class="sxs-lookup"><span data-stu-id="da56c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da56c-108">*langid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da56c-108">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da56c-109">要列舉之專案的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="da56c-109">The language id of the item to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="da56c-110">*pLayoutOrTip* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="da56c-110">*pLayoutOrTip* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da56c-111">接收 LAYOUTORTIP 結構陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="da56c-111">Pointer to the buffer that receives the array of LAYOUTORTIP structures.</span></span> <span data-ttu-id="da56c-112">這可以是 **Null** 來取得專案數目。</span><span class="sxs-lookup"><span data-stu-id="da56c-112">This can be **NULL** to get the number of items.</span></span>

</dd> <dt>

<span data-ttu-id="da56c-113">*uBufLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da56c-113">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da56c-114">*PLayoutOrTip* 所指向的緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="da56c-114">The length of the buffer pointed to by *pLayoutOrTip*.</span></span> <span data-ttu-id="da56c-115">如果 *pLayoutOrTip* 為 Null，則會忽略此 **值**。</span><span class="sxs-lookup"><span data-stu-id="da56c-115">This is ignored if *pLayoutOrTip* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da56c-116">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da56c-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da56c-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="da56c-117">Not used.</span></span> <span data-ttu-id="da56c-118">這必須為零。</span><span class="sxs-lookup"><span data-stu-id="da56c-118">This must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da56c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="da56c-119">Return value</span></span>

<span data-ttu-id="da56c-120">如果 *pLayoutOrTip* 為 **Null**，則為系統中註冊的鍵盤專案數目;否則，會複製到 *pLayoutOrTip* 中的鍵盤專案數目。</span><span class="sxs-lookup"><span data-stu-id="da56c-120">If *pLayoutOrTip* is **NULL**, the number of keyboard items that are registered in System; otherwise, the number of keyboard items that are copied into *pLayoutOrTip*.</span></span>

## <a name="remarks"></a><span data-ttu-id="da56c-121">備註</span><span class="sxs-lookup"><span data-stu-id="da56c-121">Remarks</span></span>

<span data-ttu-id="da56c-122">沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。</span><span class="sxs-lookup"><span data-stu-id="da56c-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="da56c-123">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="da56c-123">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="da56c-124">請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da56c-124">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="da56c-125">LAYOUTORTIP 的定義如下：</span><span class="sxs-lookup"><span data-stu-id="da56c-125">The definition of LAYOUTORTIP is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a><span data-ttu-id="da56c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="da56c-126">Requirements</span></span>



| <span data-ttu-id="da56c-127">需求</span><span class="sxs-lookup"><span data-stu-id="da56c-127">Requirement</span></span> | <span data-ttu-id="da56c-128">值</span><span class="sxs-lookup"><span data-stu-id="da56c-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="da56c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da56c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="da56c-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da56c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="da56c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da56c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="da56c-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da56c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="da56c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="da56c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da56c-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da56c-134"><dt>Input.dll</dt></span></span> </dl> |



 

