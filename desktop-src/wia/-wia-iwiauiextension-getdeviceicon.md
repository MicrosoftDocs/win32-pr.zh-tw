---
description: IWiaUIExtension：： GetDeviceIcon 方法-取得自訂裝置圖示。
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'IWiaUIExtension：： GetDeviceIcon 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116656"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="de8f2-103">IWiaUIExtension：： GetDeviceIcon 方法</span><span class="sxs-lookup"><span data-stu-id="de8f2-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="de8f2-104">取得自訂裝置圖示。</span><span class="sxs-lookup"><span data-stu-id="de8f2-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="de8f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="de8f2-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="de8f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="de8f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de8f2-107">*bstrDeviceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de8f2-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de8f2-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="de8f2-108">Type: **BSTR**</span></span>

<span data-ttu-id="de8f2-109">指定要取得其圖示之 WIA 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="de8f2-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="de8f2-110">*phIcon* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="de8f2-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de8f2-111">類型： **HICON \***</span><span class="sxs-lookup"><span data-stu-id="de8f2-111">Type: **HICON\***</span></span>

<span data-ttu-id="de8f2-112">指向將接收裝置圖示控制碼的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="de8f2-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="de8f2-113">*nSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de8f2-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de8f2-114">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="de8f2-114">Type: **ULONG**</span></span>

<span data-ttu-id="de8f2-115">指定所需的圖示大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="de8f2-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="de8f2-116">此圖示會假設為正方形，而 nSize 會指定所要求圖示的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="de8f2-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de8f2-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="de8f2-117">Return value</span></span>

<span data-ttu-id="de8f2-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de8f2-118">Type: **HRESULT**</span></span>

<span data-ttu-id="de8f2-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="de8f2-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de8f2-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="de8f2-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="de8f2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="de8f2-121">Requirements</span></span>



| <span data-ttu-id="de8f2-122">需求</span><span class="sxs-lookup"><span data-stu-id="de8f2-122">Requirement</span></span> | <span data-ttu-id="de8f2-123">值</span><span class="sxs-lookup"><span data-stu-id="de8f2-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="de8f2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de8f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="de8f2-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de8f2-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="de8f2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de8f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="de8f2-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de8f2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="de8f2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="de8f2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="de8f2-129"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="de8f2-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




