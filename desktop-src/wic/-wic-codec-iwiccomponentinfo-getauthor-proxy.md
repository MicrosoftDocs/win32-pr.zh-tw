---
description: GetAuthor 方法的 Proxy 函式。
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f181a567ae4089870d324c7a7e0d67a34b965b5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994488"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a><span data-ttu-id="d10ab-103">IWICComponentInfo \_ GetAuthor \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d10ab-103">IWICComponentInfo\_GetAuthor\_Proxy function</span></span>

<span data-ttu-id="d10ab-104">[**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="d10ab-104">Proxy function for the [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d10ab-105">語法</span><span class="sxs-lookup"><span data-stu-id="d10ab-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="d10ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="d10ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d10ab-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="d10ab-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ab-108">類型： \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="d10ab-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="d10ab-109">這個 [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d10ab-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="d10ab-110">*cchAuthor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d10ab-110">*cchAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ab-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="d10ab-111">Type: **UINT**</span></span>

<span data-ttu-id="d10ab-112">*WzAuthor* 緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="d10ab-112">The size of the *wzAuthor* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d10ab-113">*wzAuthor* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d10ab-113">*wzAuthor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ab-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d10ab-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="d10ab-115">接收元件作者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="d10ab-115">A pointer that receives the name of the component's author.</span></span>

<span data-ttu-id="d10ab-116">傳回的字串是預設的地區設定，預設為1033。</span><span class="sxs-lookup"><span data-stu-id="d10ab-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="d10ab-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d10ab-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ab-118">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="d10ab-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="d10ab-119">接收元件作者名稱實際長度的指標。</span><span class="sxs-lookup"><span data-stu-id="d10ab-119">A pointer that receives the actual length of the component's authors name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d10ab-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="d10ab-120">Return value</span></span>

<span data-ttu-id="d10ab-121">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d10ab-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d10ab-122">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d10ab-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d10ab-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d10ab-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d10ab-124">備註</span><span class="sxs-lookup"><span data-stu-id="d10ab-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d10ab-125">需求</span><span class="sxs-lookup"><span data-stu-id="d10ab-125">Requirements</span></span>



| <span data-ttu-id="d10ab-126">需求</span><span class="sxs-lookup"><span data-stu-id="d10ab-126">Requirement</span></span> | <span data-ttu-id="d10ab-127">值</span><span class="sxs-lookup"><span data-stu-id="d10ab-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10ab-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d10ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d10ab-129">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d10ab-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d10ab-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d10ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d10ab-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d10ab-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d10ab-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d10ab-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d10ab-133"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d10ab-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




