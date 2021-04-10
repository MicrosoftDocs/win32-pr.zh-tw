---
description: InitializeFromPalette 方法的 Proxy 函式。
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: IWICPalette_InitializeFromPalette_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 130c135d3c32135aeefd25fe8799e50c0b5ec855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851892"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a><span data-ttu-id="97c99-103">IWICPalette \_ InitializeFromPalette \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="97c99-103">IWICPalette\_InitializeFromPalette\_Proxy function</span></span>

<span data-ttu-id="97c99-104">[**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="97c99-104">Proxy function for the [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c99-105">語法</span><span class="sxs-lookup"><span data-stu-id="97c99-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a><span data-ttu-id="97c99-106">參數</span><span class="sxs-lookup"><span data-stu-id="97c99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c99-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="97c99-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-108">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="97c99-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="97c99-109">這個 [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="97c99-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-110">*pIMILPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97c99-110">*pIMILPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-111">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="97c99-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="97c99-112">來源調色板的指標。</span><span class="sxs-lookup"><span data-stu-id="97c99-112">Pointer to the source palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c99-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="97c99-113">Return value</span></span>

<span data-ttu-id="97c99-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="97c99-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="97c99-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="97c99-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="97c99-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="97c99-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c99-117">備註</span><span class="sxs-lookup"><span data-stu-id="97c99-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="97c99-118">需求</span><span class="sxs-lookup"><span data-stu-id="97c99-118">Requirements</span></span>



| <span data-ttu-id="97c99-119">需求</span><span class="sxs-lookup"><span data-stu-id="97c99-119">Requirement</span></span> | <span data-ttu-id="97c99-120">值</span><span class="sxs-lookup"><span data-stu-id="97c99-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97c99-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97c99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="97c99-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97c99-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="97c99-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97c99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="97c99-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97c99-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="97c99-125">DLL</span><span class="sxs-lookup"><span data-stu-id="97c99-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97c99-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="97c99-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




