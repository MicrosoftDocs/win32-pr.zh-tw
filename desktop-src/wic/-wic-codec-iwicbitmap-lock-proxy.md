---
description: Lock 方法的 Proxy 函式。
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: IWICBitmap_Lock_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000066"
---
# <a name="iwicbitmap_lock_proxy-function"></a><span data-ttu-id="a7e36-103">IWICBitmap \_ 鎖定 \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="a7e36-103">IWICBitmap\_Lock\_Proxy function</span></span>

<span data-ttu-id="a7e36-104">[**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="a7e36-104">Proxy function for the [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7e36-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7e36-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a><span data-ttu-id="a7e36-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7e36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7e36-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="a7e36-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e36-108">類型： \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="a7e36-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="a7e36-109">這個 [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a7e36-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="a7e36-110">*prcLock* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7e36-110">*prcLock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e36-111">類型： \**Const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="a7e36-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="a7e36-112">要存取的矩形。</span><span class="sxs-lookup"><span data-stu-id="a7e36-112">The rectangle to be accessed.</span></span>

</dd> <dt>

<span data-ttu-id="a7e36-113">_flags \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7e36-113">_flags\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e36-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a7e36-114">Type: **DWORD**</span></span>

<span data-ttu-id="a7e36-115">您想要取得鎖定的存取模式。</span><span class="sxs-lookup"><span data-stu-id="a7e36-115">The access mode you wish to obtain for the lock.</span></span>

</dd> <dt>

<span data-ttu-id="a7e36-116">*ppILock* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a7e36-116">*ppILock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e36-117">類型： **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span><span class="sxs-lookup"><span data-stu-id="a7e36-117">Type: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span></span>

<span data-ttu-id="a7e36-118">接收鎖定之記憶體位置的指標。</span><span class="sxs-lookup"><span data-stu-id="a7e36-118">A pointer that receives the locked memory location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7e36-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7e36-119">Return value</span></span>

<span data-ttu-id="a7e36-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7e36-120">Type: **HRESULT**</span></span>

<span data-ttu-id="a7e36-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a7e36-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7e36-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a7e36-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7e36-123">備註</span><span class="sxs-lookup"><span data-stu-id="a7e36-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a7e36-124">需求</span><span class="sxs-lookup"><span data-stu-id="a7e36-124">Requirements</span></span>



| <span data-ttu-id="a7e36-125">需求</span><span class="sxs-lookup"><span data-stu-id="a7e36-125">Requirement</span></span> | <span data-ttu-id="a7e36-126">值</span><span class="sxs-lookup"><span data-stu-id="a7e36-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e36-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7e36-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a7e36-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7e36-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a7e36-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7e36-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a7e36-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7e36-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a7e36-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a7e36-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7e36-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7e36-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




