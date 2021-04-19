---
description: InitializeFromMemory 方法的 Proxy 函式。
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: IWICStream_InitializeFromMemory_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fe034698635a35c098f6466712d17489f301dd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980086"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="89321-103">IWICStream \_ InitializeFromMemory \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="89321-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="89321-104">[**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="89321-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89321-105">語法</span><span class="sxs-lookup"><span data-stu-id="89321-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="89321-106">參數</span><span class="sxs-lookup"><span data-stu-id="89321-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89321-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="89321-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89321-108">類型： \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="89321-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="89321-109">這個 [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="89321-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="89321-110">*pbBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89321-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89321-111">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="89321-111">Type: \**BYTE\** _</span></span>

<span data-ttu-id="89321-112">用來初始化資料流程的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="89321-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="89321-113">_cbBufferSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89321-113">_cbBufferSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89321-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="89321-114">Type: **DWORD**</span></span>

<span data-ttu-id="89321-115">緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="89321-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89321-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="89321-116">Return value</span></span>

<span data-ttu-id="89321-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89321-117">Type: **HRESULT**</span></span>

<span data-ttu-id="89321-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="89321-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89321-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="89321-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89321-120">備註</span><span class="sxs-lookup"><span data-stu-id="89321-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="89321-121">需求</span><span class="sxs-lookup"><span data-stu-id="89321-121">Requirements</span></span>



| <span data-ttu-id="89321-122">需求</span><span class="sxs-lookup"><span data-stu-id="89321-122">Requirement</span></span> | <span data-ttu-id="89321-123">值</span><span class="sxs-lookup"><span data-stu-id="89321-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89321-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89321-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89321-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89321-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="89321-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89321-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89321-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89321-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="89321-128">DLL</span><span class="sxs-lookup"><span data-stu-id="89321-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89321-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="89321-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




