---
description: 靜態 creator 函式，可在桌面應用程式中建立呈現介面的 XamlUIPresenter。
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995108"
---
# <a name="createxamluipresenter-function"></a><span data-ttu-id="3ddf7-103">CreateXamlUIPresenter 函式</span><span class="sxs-lookup"><span data-stu-id="3ddf7-103">CreateXamlUIPresenter function</span></span>

<span data-ttu-id="3ddf7-104">靜態 creator 函式，可在桌面應用程式中建立呈現介面的 [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) 。</span><span class="sxs-lookup"><span data-stu-id="3ddf7-104">A static creator function that can create a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) for a render surface in a desktop app.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddf7-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ddf7-105">Syntax</span></span>


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a><span data-ttu-id="3ddf7-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ddf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ddf7-107">*pPresentSite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ddf7-107">*pPresentSite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddf7-108">現有的裝載介面。</span><span class="sxs-lookup"><span data-stu-id="3ddf7-108">An existing hosting interface.</span></span> <span data-ttu-id="3ddf7-109">請參閱 Internet Explorer 檔中的 **IViewObjectPresentNotifySite** 。</span><span class="sxs-lookup"><span data-stu-id="3ddf7-109">See **IViewObjectPresentNotifySite** in Internet Explorer documentation.</span></span>

</dd> <dt>

<span data-ttu-id="3ddf7-110">*ppPresenter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ddf7-110">*ppPresenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddf7-111">[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)的 **\[ exclusiveto \]** 介面。</span><span class="sxs-lookup"><span data-stu-id="3ddf7-111">The **\[exclusiveto\]** interface for a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ddf7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ddf7-112">Return value</span></span>

<span data-ttu-id="3ddf7-113">標準 **HResult**， **S \_ 正常** ，表示成功。</span><span class="sxs-lookup"><span data-stu-id="3ddf7-113">A standard **HResult**, **S\_OK** for success.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ddf7-114">備註</span><span class="sxs-lookup"><span data-stu-id="3ddf7-114">Remarks</span></span>

<span data-ttu-id="3ddf7-115">呼叫這個方法需要 Windows.UI.Xaml.dll 的 **DllImport** 。</span><span class="sxs-lookup"><span data-stu-id="3ddf7-115">Calling this method requires a **DllImport** from Windows.UI.Xaml.dll.</span></span>

<span data-ttu-id="3ddf7-116">您無法從 Windows Store 應用程式呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3ddf7-116">You cannot call this method from a Windows Store app.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddf7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ddf7-117">Requirements</span></span>



| <span data-ttu-id="3ddf7-118">需求</span><span class="sxs-lookup"><span data-stu-id="3ddf7-118">Requirement</span></span> | <span data-ttu-id="3ddf7-119">值</span><span class="sxs-lookup"><span data-stu-id="3ddf7-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddf7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3ddf7-120">Header</span></span><br/> | <dl> <span data-ttu-id="3ddf7-121"><dt>Xaml-coretypes .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ddf7-121"><dt>Windows.ui.xaml-coretypes.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ddf7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3ddf7-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="3ddf7-123"><dt>Windows.UI.Xaml.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ddf7-123"><dt>Windows.UI.Xaml.dll</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="3ddf7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ddf7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddf7-125">**XamlUIPresenter**</span><span class="sxs-lookup"><span data-stu-id="3ddf7-125">**XamlUIPresenter**</span></span>](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
