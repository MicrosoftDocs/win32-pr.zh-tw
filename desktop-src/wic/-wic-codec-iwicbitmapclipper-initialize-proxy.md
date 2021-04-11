---
description: Initialize 方法的 Proxy 函式。
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: IWICBitmapClipper_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 83c41b8802546b36ad309306ecc83a34c5d3a0c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112852"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="84dd3-103">IWICBitmapClipper \_ Initialize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="84dd3-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="84dd3-104">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="84dd3-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="84dd3-105">語法</span><span class="sxs-lookup"><span data-stu-id="84dd3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="84dd3-106">參數</span><span class="sxs-lookup"><span data-stu-id="84dd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84dd3-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="84dd3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84dd3-108">類型： \**[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) \** _</span><span class="sxs-lookup"><span data-stu-id="84dd3-108">Type: \**[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\** _</span></span>

<span data-ttu-id="84dd3-109">這個 [_ *IWICBitmapClipper* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="84dd3-109">Pointer to this [_ *IWICBitmapClipper*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="84dd3-110">*pISource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84dd3-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84dd3-111">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="84dd3-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="84dd3-112">輸入點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="84dd3-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="84dd3-113">_prc \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84dd3-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84dd3-114">類型： \**Const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="84dd3-114">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="84dd3-115">要裁剪之點陣圖來源的矩形。</span><span class="sxs-lookup"><span data-stu-id="84dd3-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84dd3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="84dd3-116">Return value</span></span>

<span data-ttu-id="84dd3-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="84dd3-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="84dd3-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="84dd3-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84dd3-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84dd3-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="84dd3-120">備註</span><span class="sxs-lookup"><span data-stu-id="84dd3-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="84dd3-121">需求</span><span class="sxs-lookup"><span data-stu-id="84dd3-121">Requirements</span></span>



| <span data-ttu-id="84dd3-122">需求</span><span class="sxs-lookup"><span data-stu-id="84dd3-122">Requirement</span></span> | <span data-ttu-id="84dd3-123">值</span><span class="sxs-lookup"><span data-stu-id="84dd3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84dd3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84dd3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="84dd3-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84dd3-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="84dd3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84dd3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="84dd3-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84dd3-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="84dd3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="84dd3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84dd3-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="84dd3-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




