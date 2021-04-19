---
description: GetVersion 方法的 Proxy 函數。
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980087"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a><span data-ttu-id="f3e51-103">IWICComponentInfo \_ GetVersion \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="f3e51-103">IWICComponentInfo\_GetVersion\_Proxy function</span></span>

<span data-ttu-id="f3e51-104">[**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion)方法的 Proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="f3e51-104">Proxy function for the [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e51-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3e51-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="f3e51-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3e51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3e51-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="f3e51-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e51-108">類型： \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="f3e51-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="f3e51-109">這個 [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f3e51-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="f3e51-110">*cchVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3e51-110">*cchVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e51-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="f3e51-111">Type: **UINT**</span></span>

<span data-ttu-id="f3e51-112">*WzVersion* 緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="f3e51-112">The size of the *wzVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f3e51-113">*wzVersion* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f3e51-113">*wzVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e51-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="f3e51-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="f3e51-115">接收元件版本之文化特性不變字串的指標。</span><span class="sxs-lookup"><span data-stu-id="f3e51-115">A pointer that receives a culture invariant string of the component's version.</span></span>

</dd> <dt>

<span data-ttu-id="f3e51-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f3e51-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e51-117">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="f3e51-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="f3e51-118">接收元件版本實際長度的指標。</span><span class="sxs-lookup"><span data-stu-id="f3e51-118">A pointer that receives the actual length of the component's version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3e51-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3e51-119">Return value</span></span>

<span data-ttu-id="f3e51-120">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f3e51-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f3e51-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f3e51-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3e51-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f3e51-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3e51-123">備註</span><span class="sxs-lookup"><span data-stu-id="f3e51-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e51-124">需求</span><span class="sxs-lookup"><span data-stu-id="f3e51-124">Requirements</span></span>



| <span data-ttu-id="f3e51-125">需求</span><span class="sxs-lookup"><span data-stu-id="f3e51-125">Requirement</span></span> | <span data-ttu-id="f3e51-126">值</span><span class="sxs-lookup"><span data-stu-id="f3e51-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e51-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3e51-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e51-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3e51-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f3e51-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3e51-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e51-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3e51-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f3e51-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f3e51-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3e51-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3e51-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




