---
description: GetFriendlyName 方法的 Proxy 函式。
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: IWICComponentInfo_GetFriendlyName_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975359"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a><span data-ttu-id="1787b-103">IWICComponentInfo \_ GetFriendlyName \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="1787b-103">IWICComponentInfo\_GetFriendlyName\_Proxy function</span></span>

<span data-ttu-id="1787b-104">[**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="1787b-104">Proxy function for the [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1787b-105">語法</span><span class="sxs-lookup"><span data-stu-id="1787b-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="1787b-106">參數</span><span class="sxs-lookup"><span data-stu-id="1787b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1787b-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="1787b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1787b-108">類型： \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="1787b-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="1787b-109">這個 [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="1787b-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="1787b-110">*cchFriendlyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1787b-110">*cchFriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1787b-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="1787b-111">Type: **UINT**</span></span>

<span data-ttu-id="1787b-112">*WzFriendlyName* 緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="1787b-112">The size of the *wzFriendlyName* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1787b-113">*wzFriendlyName* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1787b-113">*wzFriendlyName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1787b-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="1787b-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="1787b-115">接收元件易記名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="1787b-115">A pointer that receives the friendly name of the component.</span></span>

<span data-ttu-id="1787b-116">傳回的字串是預設的地區設定，預設為1033。</span><span class="sxs-lookup"><span data-stu-id="1787b-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="1787b-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1787b-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1787b-118">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="1787b-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="1787b-119">接收元件之易記名稱實際長度的指標。</span><span class="sxs-lookup"><span data-stu-id="1787b-119">A pointer that receives the actual length of the component's friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1787b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="1787b-120">Return value</span></span>

<span data-ttu-id="1787b-121">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1787b-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1787b-122">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1787b-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1787b-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1787b-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1787b-124">備註</span><span class="sxs-lookup"><span data-stu-id="1787b-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1787b-125">需求</span><span class="sxs-lookup"><span data-stu-id="1787b-125">Requirements</span></span>



| <span data-ttu-id="1787b-126">需求</span><span class="sxs-lookup"><span data-stu-id="1787b-126">Requirement</span></span> | <span data-ttu-id="1787b-127">值</span><span class="sxs-lookup"><span data-stu-id="1787b-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1787b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1787b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1787b-129">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1787b-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1787b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1787b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1787b-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1787b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1787b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1787b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1787b-133"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1787b-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




