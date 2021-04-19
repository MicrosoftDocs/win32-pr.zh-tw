---
description: 設定媒體資料流程來源的範例。
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: IMFMediaStreamSourceSampleRequest：： SetSample 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997600"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a><span data-ttu-id="c45c3-103">IMFMediaStreamSourceSampleRequest：： SetSample 方法</span><span class="sxs-lookup"><span data-stu-id="c45c3-103">IMFMediaStreamSourceSampleRequest::SetSample method</span></span>

<span data-ttu-id="c45c3-104">設定媒體資料流程來源的範例。</span><span class="sxs-lookup"><span data-stu-id="c45c3-104">Sets the sample for the media stream source.</span></span>

## <a name="syntax"></a><span data-ttu-id="c45c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="c45c3-105">Syntax</span></span>


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a><span data-ttu-id="c45c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="c45c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c45c3-107">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c45c3-107">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45c3-108">媒體資料流程來源的範例。</span><span class="sxs-lookup"><span data-stu-id="c45c3-108">The sample for the media stream source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c45c3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c45c3-109">Return value</span></span>

<span data-ttu-id="c45c3-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c45c3-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c45c3-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c45c3-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c45c3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c45c3-112">Requirements</span></span>



| <span data-ttu-id="c45c3-113">需求</span><span class="sxs-lookup"><span data-stu-id="c45c3-113">Requirement</span></span> | <span data-ttu-id="c45c3-114">值</span><span class="sxs-lookup"><span data-stu-id="c45c3-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c45c3-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c45c3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c45c3-116">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c45c3-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c45c3-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c45c3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c45c3-118">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c45c3-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="c45c3-119">Idl</span><span class="sxs-lookup"><span data-stu-id="c45c3-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c45c3-120"><dt>Mfidl .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c45c3-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c45c3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c45c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45c3-122">**IMFMediaStreamSourceSampleRequest**</span><span class="sxs-lookup"><span data-stu-id="c45c3-122">**IMFMediaStreamSourceSampleRequest**</span></span>](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




