---
description: GetType 方法的 Proxy 函數。
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: IWICPalette_GetType_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983774"
---
# <a name="iwicpalette_gettype_proxy-function"></a><span data-ttu-id="c8b45-103">IWICPalette \_ GetType \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="c8b45-103">IWICPalette\_GetType\_Proxy function</span></span>

<span data-ttu-id="c8b45-104">[**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype)方法的 Proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="c8b45-104">Proxy function for the [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b45-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8b45-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a><span data-ttu-id="c8b45-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8b45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b45-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="c8b45-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b45-108">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="c8b45-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="c8b45-109">這個 [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c8b45-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="c8b45-110">*pePaletteType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c8b45-110">*pePaletteType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b45-111">類型： \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _</span><span class="sxs-lookup"><span data-stu-id="c8b45-111">Type: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\** _</span></span>

<span data-ttu-id="c8b45-112">接收 bimtap 之調色板型別的指標。</span><span class="sxs-lookup"><span data-stu-id="c8b45-112">Pointer that receives the palette type of the bimtap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b45-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8b45-113">Return value</span></span>

<span data-ttu-id="c8b45-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c8b45-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c8b45-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c8b45-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8b45-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c8b45-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8b45-117">備註</span><span class="sxs-lookup"><span data-stu-id="c8b45-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b45-118">需求</span><span class="sxs-lookup"><span data-stu-id="c8b45-118">Requirements</span></span>



| <span data-ttu-id="c8b45-119">需求</span><span class="sxs-lookup"><span data-stu-id="c8b45-119">Requirement</span></span> | <span data-ttu-id="c8b45-120">值</span><span class="sxs-lookup"><span data-stu-id="c8b45-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b45-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8b45-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b45-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8b45-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c8b45-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8b45-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b45-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8b45-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c8b45-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c8b45-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8b45-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8b45-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




