---
description: 用於建立 IWICColorCoNtext 的 Proxy 函數。
ms.assetid: 66348ef2-3056-4ec7-84ad-6e022e320a33
title: WICCreateColorCoNtext_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorContext_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e4861bb1ccb275edc38163335e0da5d26441a334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986983"
---
# <a name="wiccreatecolorcontext_proxy-function"></a><span data-ttu-id="80fbf-103">WICCreateColorCoNtext \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="80fbf-103">WICCreateColorContext\_Proxy function</span></span>

<span data-ttu-id="80fbf-104">用於建立 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)的 Proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="80fbf-104">Proxy function for creating an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

## <a name="syntax"></a><span data-ttu-id="80fbf-105">語法</span><span class="sxs-lookup"><span data-stu-id="80fbf-105">Syntax</span></span>


```C++
HRESULT WICCreateColorContext_Proxy(
  _In_ IWICImagingFactory *THIS_PTR,
       IWICColorContext   ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="80fbf-106">參數</span><span class="sxs-lookup"><span data-stu-id="80fbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80fbf-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="80fbf-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fbf-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="80fbf-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

<span data-ttu-id="80fbf-109">這個 [_ *IWICImagingFactory* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="80fbf-109">Pointer to this [_ *IWICImagingFactory*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="80fbf-110">*ppIColorCoNtext*</span><span class="sxs-lookup"><span data-stu-id="80fbf-110">*ppIColorContext*</span></span> 
</dt> <dd>

<span data-ttu-id="80fbf-111">類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span><span class="sxs-lookup"><span data-stu-id="80fbf-111">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80fbf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="80fbf-112">Return value</span></span>

<span data-ttu-id="80fbf-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="80fbf-113">Type: **HRESULT**</span></span>

<span data-ttu-id="80fbf-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="80fbf-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80fbf-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="80fbf-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80fbf-116">備註</span><span class="sxs-lookup"><span data-stu-id="80fbf-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="80fbf-117">需求</span><span class="sxs-lookup"><span data-stu-id="80fbf-117">Requirements</span></span>



| <span data-ttu-id="80fbf-118">需求</span><span class="sxs-lookup"><span data-stu-id="80fbf-118">Requirement</span></span> | <span data-ttu-id="80fbf-119">值</span><span class="sxs-lookup"><span data-stu-id="80fbf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80fbf-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80fbf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="80fbf-121">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80fbf-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="80fbf-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80fbf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="80fbf-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80fbf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="80fbf-124">DLL</span><span class="sxs-lookup"><span data-stu-id="80fbf-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80fbf-125"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="80fbf-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




