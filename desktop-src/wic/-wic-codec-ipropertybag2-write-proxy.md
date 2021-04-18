---
description: Windows 影像處理元件適用于 IPropertyBag2：： Write 的 (WIC) proxy 函數。
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: IPropertyBag2_Write_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318276"
---
# <a name="ipropertybag2_write_proxy-function"></a><span data-ttu-id="d6689-103">IPropertyBag2 \_ 寫入 \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d6689-103">IPropertyBag2\_Write\_Proxy function</span></span>

<span data-ttu-id="d6689-104">Windows 影像處理元件適用于 IPropertyBag2：： Write 的 (WIC) proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="d6689-104">Windows Imaging Component (WIC) proxy function for IPropertyBag2::Write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6689-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6689-105">Syntax</span></span>


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="d6689-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6689-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6689-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="d6689-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6689-108">類型： \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="d6689-108">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="d6689-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="d6689-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="d6689-110">_cProperties \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6689-110">_cProperties\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6689-111">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="d6689-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="d6689-112">*ppropBag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6689-112">*ppropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6689-113">類型： \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="d6689-113">Type: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85))\** _</span></span>

</dd> <dt>

<span data-ttu-id="d6689-114">_pvarValue \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6689-114">_pvarValue\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6689-115">類型： \**VARIANT \** _</span><span class="sxs-lookup"><span data-stu-id="d6689-115">Type: \**VARIANT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6689-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6689-116">Return value</span></span>

<span data-ttu-id="d6689-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d6689-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d6689-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d6689-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6689-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6689-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6689-120">備註</span><span class="sxs-lookup"><span data-stu-id="d6689-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d6689-121">需求</span><span class="sxs-lookup"><span data-stu-id="d6689-121">Requirements</span></span>



| <span data-ttu-id="d6689-122">需求</span><span class="sxs-lookup"><span data-stu-id="d6689-122">Requirement</span></span> | <span data-ttu-id="d6689-123">值</span><span class="sxs-lookup"><span data-stu-id="d6689-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6689-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6689-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d6689-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6689-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d6689-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6689-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d6689-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6689-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d6689-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d6689-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6689-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6689-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

