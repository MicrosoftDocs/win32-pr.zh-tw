---
description: SetThumbnail 方法的 Proxy 函式。
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: IWICBitmapEncoder_SetThumbnail_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d2670dae0d8ba9eeda7ca1d6dce5d3957dc59b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468968"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="24c96-103">IWICBitmapEncoder \_ SetThumbnail \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="24c96-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="24c96-104">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="24c96-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c96-105">語法</span><span class="sxs-lookup"><span data-stu-id="24c96-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="24c96-106">參數</span><span class="sxs-lookup"><span data-stu-id="24c96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c96-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="24c96-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24c96-108">類型： \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="24c96-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="24c96-109">這個 [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="24c96-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="24c96-110">*pIThumbnail* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24c96-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24c96-111">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="24c96-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="24c96-112">要設定為全域縮圖的 [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。</span><span class="sxs-lookup"><span data-stu-id="24c96-112">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c96-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="24c96-113">Return value</span></span>

<span data-ttu-id="24c96-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="24c96-114">Type: **HRESULT**</span></span>

<span data-ttu-id="24c96-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="24c96-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24c96-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="24c96-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c96-117">備註</span><span class="sxs-lookup"><span data-stu-id="24c96-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="24c96-118">需求</span><span class="sxs-lookup"><span data-stu-id="24c96-118">Requirements</span></span>



| <span data-ttu-id="24c96-119">需求</span><span class="sxs-lookup"><span data-stu-id="24c96-119">Requirement</span></span> | <span data-ttu-id="24c96-120">值</span><span class="sxs-lookup"><span data-stu-id="24c96-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c96-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24c96-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24c96-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24c96-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="24c96-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24c96-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24c96-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24c96-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="24c96-125">DLL</span><span class="sxs-lookup"><span data-stu-id="24c96-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24c96-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="24c96-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




