---
description: IEnumString：： Reset 的 Windows 影像處理元件 (WIC) proxy 函數。
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: IEnumString_Reset_WIC_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989907"
---
# <a name="ienumstring_reset_wic_proxy-function"></a><span data-ttu-id="9f5be-103">IEnumString \_ Reset \_ WIC \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="9f5be-103">IEnumString\_Reset\_WIC\_Proxy function</span></span>

<span data-ttu-id="9f5be-104">IEnumString：： Reset 的 Windows 影像處理元件 (WIC) proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="9f5be-104">Windows Imaging Component (WIC) proxy function for IEnumString::Reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f5be-105">語法</span><span class="sxs-lookup"><span data-stu-id="9f5be-105">Syntax</span></span>


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="9f5be-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f5be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f5be-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="9f5be-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f5be-108">類型： \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="9f5be-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="9f5be-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="9f5be-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="9f5be-110">_celt \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f5be-110">_celt\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f5be-111">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="9f5be-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="9f5be-112">*rgelt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9f5be-112">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f5be-113">類型： \**LPOLESTR \** _</span><span class="sxs-lookup"><span data-stu-id="9f5be-113">Type: \**LPOLESTR\** _</span></span>

</dd> <dt>

<span data-ttu-id="9f5be-114">_pceltFetched \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9f5be-114">_pceltFetched\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f5be-115">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="9f5be-115">Type: \**ULONG\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f5be-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f5be-116">Return value</span></span>

<span data-ttu-id="9f5be-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9f5be-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9f5be-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9f5be-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f5be-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9f5be-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f5be-120">備註</span><span class="sxs-lookup"><span data-stu-id="9f5be-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9f5be-121">需求</span><span class="sxs-lookup"><span data-stu-id="9f5be-121">Requirements</span></span>



| <span data-ttu-id="9f5be-122">需求</span><span class="sxs-lookup"><span data-stu-id="9f5be-122">Requirement</span></span> | <span data-ttu-id="9f5be-123">值</span><span class="sxs-lookup"><span data-stu-id="9f5be-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f5be-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f5be-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9f5be-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f5be-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9f5be-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f5be-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9f5be-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f5be-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9f5be-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9f5be-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f5be-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f5be-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




