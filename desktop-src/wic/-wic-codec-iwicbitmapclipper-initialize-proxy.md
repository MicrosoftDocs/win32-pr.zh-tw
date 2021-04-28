---
description: Initialize 方法的 IWICBitmapClipper_Initialize_Proxy 函數 Proxy 函式。
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
ms.openlocfilehash: ce3c745d27928765fdfdf664c423f7e2146cbd5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086386"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="d8961-103">IWICBitmapClipper \_ Initialize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d8961-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="d8961-104">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="d8961-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8961-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8961-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="d8961-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8961-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="d8961-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8961-108">類型： **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span><span class="sxs-lookup"><span data-stu-id="d8961-108">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span></span>

<span data-ttu-id="d8961-109">這個 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d8961-109">Pointer to this [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="d8961-110">*pISource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8961-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8961-111">類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="d8961-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="d8961-112">輸入點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="d8961-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="d8961-113">*中國* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8961-113">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8961-114">Type： **Const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***</span><span class="sxs-lookup"><span data-stu-id="d8961-114">Type: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\***</span></span>

<span data-ttu-id="d8961-115">要裁剪之點陣圖來源的矩形。</span><span class="sxs-lookup"><span data-stu-id="d8961-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8961-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8961-116">Return value</span></span>

<span data-ttu-id="d8961-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d8961-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d8961-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d8961-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8961-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d8961-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8961-120">備註</span><span class="sxs-lookup"><span data-stu-id="d8961-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d8961-121">需求</span><span class="sxs-lookup"><span data-stu-id="d8961-121">Requirements</span></span>



| <span data-ttu-id="d8961-122">需求</span><span class="sxs-lookup"><span data-stu-id="d8961-122">Requirement</span></span> | <span data-ttu-id="d8961-123">值</span><span class="sxs-lookup"><span data-stu-id="d8961-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8961-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8961-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d8961-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8961-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d8961-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8961-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d8961-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8961-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d8961-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d8961-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8961-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8961-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




