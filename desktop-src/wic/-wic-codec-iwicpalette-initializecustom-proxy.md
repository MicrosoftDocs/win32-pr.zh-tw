---
description: InitializeCustom 方法的 Proxy 函式。
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: IWICPalette_InitializeCustom_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975880"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a><span data-ttu-id="0650a-103">IWICPalette \_ InitializeCustom \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="0650a-103">IWICPalette\_InitializeCustom\_Proxy function</span></span>

<span data-ttu-id="0650a-104">[**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="0650a-104">Proxy function for the [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0650a-105">語法</span><span class="sxs-lookup"><span data-stu-id="0650a-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a><span data-ttu-id="0650a-106">參數</span><span class="sxs-lookup"><span data-stu-id="0650a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0650a-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="0650a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0650a-108">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="0650a-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="0650a-109">這個 [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0650a-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="0650a-110">*pColors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0650a-110">*pColors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0650a-111">類型： \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="0650a-111">Type: \**WICColor\** _</span></span>

<span data-ttu-id="0650a-112">色彩陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="0650a-112">Pointer to the color array.</span></span>

</dd> <dt>

<span data-ttu-id="0650a-113">_colorCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0650a-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0650a-114">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="0650a-114">Type: **UINT**</span></span>

<span data-ttu-id="0650a-115">*PColors* 中的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="0650a-115">The number of colors in *pColors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0650a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0650a-116">Return value</span></span>

<span data-ttu-id="0650a-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0650a-117">Type: **HRESULT**</span></span>

<span data-ttu-id="0650a-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0650a-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0650a-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0650a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0650a-120">備註</span><span class="sxs-lookup"><span data-stu-id="0650a-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0650a-121">需求</span><span class="sxs-lookup"><span data-stu-id="0650a-121">Requirements</span></span>



| <span data-ttu-id="0650a-122">需求</span><span class="sxs-lookup"><span data-stu-id="0650a-122">Requirement</span></span> | <span data-ttu-id="0650a-123">值</span><span class="sxs-lookup"><span data-stu-id="0650a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0650a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0650a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0650a-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0650a-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0650a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0650a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0650a-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0650a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0650a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0650a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0650a-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0650a-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




