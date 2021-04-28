---
description: IWiaUIExtension2：： GetDeviceIcon 方法-取得自訂裝置圖示。
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'IWiaUIExtension2：： GetDeviceIcon 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116616"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="0191e-103">IWiaUIExtension2：： GetDeviceIcon 方法</span><span class="sxs-lookup"><span data-stu-id="0191e-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="0191e-104">取得自訂裝置圖示。</span><span class="sxs-lookup"><span data-stu-id="0191e-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="0191e-105">語法</span><span class="sxs-lookup"><span data-stu-id="0191e-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="0191e-106">參數</span><span class="sxs-lookup"><span data-stu-id="0191e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0191e-107">*bstrDeviceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0191e-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0191e-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0191e-108">Type: **BSTR**</span></span>

<span data-ttu-id="0191e-109">指定要取得其圖示之 WIA 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="0191e-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="0191e-110">*phIcon* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0191e-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0191e-111">類型： **HICON \***</span><span class="sxs-lookup"><span data-stu-id="0191e-111">Type: **HICON\***</span></span>

<span data-ttu-id="0191e-112">指向將接收裝置圖示控制碼的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="0191e-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="0191e-113">*nSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0191e-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0191e-114">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="0191e-114">Type: **ULONG**</span></span>

<span data-ttu-id="0191e-115">指定所需的圖示大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0191e-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="0191e-116">此圖示會假設為正方形，而 nSize 會指定所要求圖示的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="0191e-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0191e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0191e-117">Return value</span></span>

<span data-ttu-id="0191e-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0191e-118">Type: **HRESULT**</span></span>

<span data-ttu-id="0191e-119">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0191e-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="0191e-120">如果方法失敗，則會傳回適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0191e-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="0191e-121">下表顯示一些可能的傳回狀態碼。</span><span class="sxs-lookup"><span data-stu-id="0191e-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="0191e-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0191e-122">Error code</span></span>    | <span data-ttu-id="0191e-123">描述</span><span class="sxs-lookup"><span data-stu-id="0191e-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0191e-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0191e-124">E\_INVALIDARG</span></span> | <span data-ttu-id="0191e-125">參數 bstrDeviceId 或 phIcon 為 **Null**，或 bstrDeviceId 未指向有效的 WIA 裝置識別碼字串</span><span class="sxs-lookup"><span data-stu-id="0191e-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="0191e-126">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="0191e-126">E\_FAIL</span></span>       | <span data-ttu-id="0191e-127">沒有可用的圖示資源。</span><span class="sxs-lookup"><span data-stu-id="0191e-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="0191e-128">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="0191e-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="0191e-129">未提供所要求大小的圖示。</span><span class="sxs-lookup"><span data-stu-id="0191e-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="0191e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="0191e-130">Requirements</span></span>



| <span data-ttu-id="0191e-131">需求</span><span class="sxs-lookup"><span data-stu-id="0191e-131">Requirement</span></span> | <span data-ttu-id="0191e-132">值</span><span class="sxs-lookup"><span data-stu-id="0191e-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0191e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0191e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0191e-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0191e-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0191e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0191e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0191e-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0191e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0191e-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0191e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0191e-138"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="0191e-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




