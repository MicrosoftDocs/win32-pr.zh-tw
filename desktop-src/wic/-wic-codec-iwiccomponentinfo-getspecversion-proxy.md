---
description: GetSpecVersion 方法的 Proxy 函式。
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976594"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a><span data-ttu-id="57bf6-103">IWICComponentInfo \_ GetSpecVersion \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="57bf6-103">IWICComponentInfo\_GetSpecVersion\_Proxy function</span></span>

<span data-ttu-id="57bf6-104">[**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="57bf6-104">Proxy function for the [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57bf6-105">語法</span><span class="sxs-lookup"><span data-stu-id="57bf6-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="57bf6-106">參數</span><span class="sxs-lookup"><span data-stu-id="57bf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57bf6-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="57bf6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57bf6-108">類型： \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="57bf6-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="57bf6-109">這個 [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="57bf6-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="57bf6-110">*cchSpecVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57bf6-110">*cchSpecVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57bf6-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="57bf6-111">Type: **UINT**</span></span>

<span data-ttu-id="57bf6-112">*WzSpecVersion* 緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="57bf6-112">The size of the *wzSpecVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="57bf6-113">*wzSpecVersion* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="57bf6-113">*wzSpecVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="57bf6-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="57bf6-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="57bf6-115">當此方法傳回時，會包含元件規格版本的文化特性 invarient 字串。</span><span class="sxs-lookup"><span data-stu-id="57bf6-115">When this method returns, contain a culture invarient string of the component's specification version.</span></span> <span data-ttu-id="57bf6-116">版本形式為 NN. nn. nn. nn. nn. nn. nn。</span><span class="sxs-lookup"><span data-stu-id="57bf6-116">The version form is NN.NN.NN.NN.</span></span>

</dd> <dt>

<span data-ttu-id="57bf6-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57bf6-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57bf6-118">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="57bf6-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="57bf6-119">接收元件規格版本實際長度的指標。</span><span class="sxs-lookup"><span data-stu-id="57bf6-119">A pointer that receives the actual length of the component's specification version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57bf6-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="57bf6-120">Return value</span></span>

<span data-ttu-id="57bf6-121">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="57bf6-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="57bf6-122">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="57bf6-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57bf6-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57bf6-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57bf6-124">備註</span><span class="sxs-lookup"><span data-stu-id="57bf6-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="57bf6-125">需求</span><span class="sxs-lookup"><span data-stu-id="57bf6-125">Requirements</span></span>



| <span data-ttu-id="57bf6-126">需求</span><span class="sxs-lookup"><span data-stu-id="57bf6-126">Requirement</span></span> | <span data-ttu-id="57bf6-127">值</span><span class="sxs-lookup"><span data-stu-id="57bf6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57bf6-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57bf6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="57bf6-129">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57bf6-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="57bf6-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57bf6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="57bf6-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57bf6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="57bf6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="57bf6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57bf6-133"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="57bf6-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




