---
description: SetPalette 方法的 IWICBitmapEncoder_SetPalette_Proxy 函數 Proxy 函式。
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: IWICBitmapEncoder_SetPalette_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8503698a1e91b86698ba288e56cc65e4447c906e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091176"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="58981-103">IWICBitmapEncoder \_ SetPalette \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="58981-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="58981-104">[**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="58981-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="58981-105">語法</span><span class="sxs-lookup"><span data-stu-id="58981-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="58981-106">參數</span><span class="sxs-lookup"><span data-stu-id="58981-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58981-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="58981-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58981-108">類型： **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="58981-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="58981-109">這個 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="58981-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="58981-110">*pIPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58981-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58981-111">類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="58981-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="58981-112">要做為全域調色板使用的 [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) 。</span><span class="sxs-lookup"><span data-stu-id="58981-112">The [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58981-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="58981-113">Return value</span></span>

<span data-ttu-id="58981-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="58981-114">Type: **HRESULT**</span></span>

<span data-ttu-id="58981-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="58981-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58981-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="58981-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58981-117">備註</span><span class="sxs-lookup"><span data-stu-id="58981-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="58981-118">需求</span><span class="sxs-lookup"><span data-stu-id="58981-118">Requirements</span></span>



| <span data-ttu-id="58981-119">需求</span><span class="sxs-lookup"><span data-stu-id="58981-119">Requirement</span></span> | <span data-ttu-id="58981-120">值</span><span class="sxs-lookup"><span data-stu-id="58981-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58981-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58981-121">Minimum supported client</span></span><br/> | <span data-ttu-id="58981-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58981-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="58981-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58981-123">Minimum supported server</span></span><br/> | <span data-ttu-id="58981-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58981-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="58981-125">DLL</span><span class="sxs-lookup"><span data-stu-id="58981-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58981-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="58981-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




