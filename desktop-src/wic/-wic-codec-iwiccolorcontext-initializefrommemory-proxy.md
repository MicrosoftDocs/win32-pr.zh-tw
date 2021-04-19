---
description: InitializeFromMemory 方法的 Proxy 函式。
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorCoNtext_InitializeFromMemory_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 32c3c24902b6c3157b9776d84c5a8eea47cce43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979203"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="846a9-103">IWICColorCoNtext \_ InitializeFromMemory \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="846a9-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="846a9-104">[**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="846a9-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="846a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="846a9-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="846a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="846a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="846a9-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="846a9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846a9-108">類型： \**[**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) \** _</span><span class="sxs-lookup"><span data-stu-id="846a9-108">Type: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\** _</span></span>

</dd> <dt>

<span data-ttu-id="846a9-109">_pbBuffer \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="846a9-109">_pbBuffer\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846a9-110">類型： \**CONST BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="846a9-110">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="846a9-111">用來初始化 [_ *IWICColorCoNtext* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="846a9-111">The buffer used to initialize the [_ *IWICColorContext*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="846a9-112">*cbBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="846a9-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846a9-113">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="846a9-113">Type: **UINT**</span></span>

<span data-ttu-id="846a9-114">*PbBuffer* 緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="846a9-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="846a9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="846a9-115">Return value</span></span>

<span data-ttu-id="846a9-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="846a9-116">Type: **HRESULT**</span></span>

<span data-ttu-id="846a9-117">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="846a9-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="846a9-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="846a9-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="846a9-119">備註</span><span class="sxs-lookup"><span data-stu-id="846a9-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="846a9-120">需求</span><span class="sxs-lookup"><span data-stu-id="846a9-120">Requirements</span></span>



| <span data-ttu-id="846a9-121">需求</span><span class="sxs-lookup"><span data-stu-id="846a9-121">Requirement</span></span> | <span data-ttu-id="846a9-122">值</span><span class="sxs-lookup"><span data-stu-id="846a9-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="846a9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="846a9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="846a9-124">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="846a9-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="846a9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="846a9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="846a9-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="846a9-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="846a9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="846a9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="846a9-128"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="846a9-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




