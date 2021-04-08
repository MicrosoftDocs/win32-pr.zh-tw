---
description: GetColorCount 方法的 Proxy 函式。
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: IWICPalette_GetColorCount_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9518878dd05c6b89152b91863c8996f96b8e6e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850651"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a><span data-ttu-id="a8e7c-103">IWICPalette \_ GetColorCount \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="a8e7c-103">IWICPalette\_GetColorCount\_Proxy function</span></span>

<span data-ttu-id="a8e7c-104">[**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-104">Proxy function for the [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e7c-105">語法</span><span class="sxs-lookup"><span data-stu-id="a8e7c-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="a8e7c-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8e7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e7c-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="a8e7c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8e7c-108">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="a8e7c-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="a8e7c-109">這個 [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="a8e7c-110">*pcCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a8e7c-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8e7c-111">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="a8e7c-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="a8e7c-112">接收色彩表中色彩數目的指標。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-112">Pointer that receives the number of colors in the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e7c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8e7c-113">Return value</span></span>

<span data-ttu-id="a8e7c-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a8e7c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a8e7c-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8e7c-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a8e7c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8e7c-117">備註</span><span class="sxs-lookup"><span data-stu-id="a8e7c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e7c-118">需求</span><span class="sxs-lookup"><span data-stu-id="a8e7c-118">Requirements</span></span>



| <span data-ttu-id="a8e7c-119">需求</span><span class="sxs-lookup"><span data-stu-id="a8e7c-119">Requirement</span></span> | <span data-ttu-id="a8e7c-120">值</span><span class="sxs-lookup"><span data-stu-id="a8e7c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e7c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8e7c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e7c-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8e7c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a8e7c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8e7c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e7c-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8e7c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a8e7c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a8e7c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8e7c-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8e7c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




