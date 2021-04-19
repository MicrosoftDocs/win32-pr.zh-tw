---
description: CopyPalette 方法的 Proxy 函式。
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: IWICBitmapSource_CopyPalette_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 792738a6be3966e898527c357c99a8cd6c5cfdb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983923"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="49e70-103">IWICBitmapSource \_ CopyPalette \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="49e70-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="49e70-104">[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="49e70-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e70-105">語法</span><span class="sxs-lookup"><span data-stu-id="49e70-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="49e70-106">參數</span><span class="sxs-lookup"><span data-stu-id="49e70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e70-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="49e70-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e70-108">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="49e70-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="49e70-109">這個 [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="49e70-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="49e70-110">*pIPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49e70-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e70-111">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="49e70-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="49e70-112">調色板。</span><span class="sxs-lookup"><span data-stu-id="49e70-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e70-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="49e70-113">Return value</span></span>

<span data-ttu-id="49e70-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="49e70-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="49e70-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="49e70-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49e70-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="49e70-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e70-117">備註</span><span class="sxs-lookup"><span data-stu-id="49e70-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="49e70-118">需求</span><span class="sxs-lookup"><span data-stu-id="49e70-118">Requirements</span></span>



| <span data-ttu-id="49e70-119">需求</span><span class="sxs-lookup"><span data-stu-id="49e70-119">Requirement</span></span> | <span data-ttu-id="49e70-120">值</span><span class="sxs-lookup"><span data-stu-id="49e70-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e70-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49e70-121">Minimum supported client</span></span><br/> | <span data-ttu-id="49e70-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49e70-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="49e70-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49e70-123">Minimum supported server</span></span><br/> | <span data-ttu-id="49e70-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49e70-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="49e70-125">DLL</span><span class="sxs-lookup"><span data-stu-id="49e70-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49e70-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="49e70-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




