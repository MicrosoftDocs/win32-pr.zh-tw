---
description: 可讓影像處理篩選器將屬性寫回驅動程式 (和裝置) 。
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'IWiaImageFilter：： ApplyProperties 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983503"
---
# <a name="iwiaimagefilterapplyproperties-method"></a><span data-ttu-id="f9f0e-103">IWiaImageFilter：： ApplyProperties 方法</span><span class="sxs-lookup"><span data-stu-id="f9f0e-103">IWiaImageFilter::ApplyProperties method</span></span>

<span data-ttu-id="f9f0e-104">可讓影像處理篩選器將屬性寫回驅動程式 (和裝置) 。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-104">Enables the image processing filter to write properties back to the driver (and device).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f0e-105">語法</span><span class="sxs-lookup"><span data-stu-id="f9f0e-105">Syntax</span></span>


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a><span data-ttu-id="f9f0e-106">參數</span><span class="sxs-lookup"><span data-stu-id="f9f0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9f0e-107">*pWiaPropertyStorage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f9f0e-107">*pWiaPropertyStorage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9f0e-108">類型： \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _</span><span class="sxs-lookup"><span data-stu-id="f9f0e-108">Type: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\** _</span></span>

<span data-ttu-id="f9f0e-109">針對要套用的屬性，指定 [_ *IWiaPropertyStorage* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)的指標。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-109">Specifies a pointer to the [_ *IWiaPropertyStorage*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) for the properties to be applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9f0e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9f0e-110">Return value</span></span>

<span data-ttu-id="f9f0e-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f9f0e-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f9f0e-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9f0e-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9f0e-114">備註</span><span class="sxs-lookup"><span data-stu-id="f9f0e-114">Remarks</span></span>

<span data-ttu-id="f9f0e-115">請勿直接從您的應用程式呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-115">Do not call this method directly from your application.</span></span> <span data-ttu-id="f9f0e-116">在影像處理篩選處理原始資料之後，Windows 映像取得 (WIA) 2.0 會呼叫它。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-116">It is called by Windows Image Acquisition (WIA) 2.0 after the image processing filter has processed the raw data.</span></span>

<span data-ttu-id="f9f0e-117">*pWiaPropertyStorage* 是影像處理篩選器應該在其中寫入屬性的 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-117">*pWiaPropertyStorage* is the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface into which the image processing filter should write properties.</span></span> <span data-ttu-id="f9f0e-118">影像處理篩選器應該只使用 [IPropertyStorage：： WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) 方法來寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-118">An image processing filter should use only the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) method to write properties.</span></span>

<span data-ttu-id="f9f0e-119">此方法可讓影像處理篩選器將屬性寫回驅動程式 (和裝置) 。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-119">This method allows the image processing filter to write properties back to the driver (and device).</span></span> <span data-ttu-id="f9f0e-120">這對執行功能的篩選可能是必要的，例如在膠片掃描期間自動曝光。</span><span class="sxs-lookup"><span data-stu-id="f9f0e-120">This may be necessary for filters that implement features such as auto-exposure during film scanning.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9f0e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9f0e-121">Requirements</span></span>



| <span data-ttu-id="f9f0e-122">需求</span><span class="sxs-lookup"><span data-stu-id="f9f0e-122">Requirement</span></span> | <span data-ttu-id="f9f0e-123">值</span><span class="sxs-lookup"><span data-stu-id="f9f0e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f0e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9f0e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f0e-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9f0e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9f0e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9f0e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f0e-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9f0e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9f0e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f9f0e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9f0e-129"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="f9f0e-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9f0e-130">Idl</span><span class="sxs-lookup"><span data-stu-id="f9f0e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9f0e-131"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9f0e-131"><dt>Wia.idl</dt></span></span> </dl> |



 

 
