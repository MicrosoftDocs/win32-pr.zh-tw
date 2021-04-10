---
title: IAMWMBufferPassCallback Notify 方法
description: 在串流處理期間傳遞的每個緩衝區，會呼叫通知方法。
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- 通知方法 windows Media 格式
- 通知方法 windows Media 格式，IAMWMBufferPassCallback 介面
- IAMWMBufferPassCallback 介面 windows Media Format，Notify 方法
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093103"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a><span data-ttu-id="9519b-106">IAMWMBufferPassCallback：： Notify 方法</span><span class="sxs-lookup"><span data-stu-id="9519b-106">IAMWMBufferPassCallback::Notify method</span></span>

<span data-ttu-id="9519b-107">在串流處理期間傳遞的每個緩衝區，會呼叫 **通知** 方法。</span><span class="sxs-lookup"><span data-stu-id="9519b-107">The **Notify** method is called by the pin for each buffer that is delivered during streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="9519b-108">語法</span><span class="sxs-lookup"><span data-stu-id="9519b-108">Syntax</span></span>


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="9519b-109">參數</span><span class="sxs-lookup"><span data-stu-id="9519b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9519b-110">*pNSSBuffer3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9519b-110">*pNSSBuffer3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9519b-111">媒體範例上公開的 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="9519b-111">Pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface exposed on the media sample.</span></span>

</dd> <dt>

<span data-ttu-id="9519b-112">*pPin* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9519b-112">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9519b-113">與範例所屬之媒體資料流程相關聯的釘選指標。</span><span class="sxs-lookup"><span data-stu-id="9519b-113">Pointer to the pin associated with the media stream that the sample belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="9519b-114">*prtStart* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9519b-114">*prtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9519b-115">範例的開始時間。</span><span class="sxs-lookup"><span data-stu-id="9519b-115">Start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="9519b-116">*prtEnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9519b-116">*prtEnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9519b-117">範例的結束時間。</span><span class="sxs-lookup"><span data-stu-id="9519b-117">End time of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9519b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="9519b-118">Return value</span></span>

<span data-ttu-id="9519b-119">未指定任何特定的傳回值。</span><span class="sxs-lookup"><span data-stu-id="9519b-119">No particular return value is specified.</span></span> <span data-ttu-id="9519b-120">呼叫的 pin 會忽略 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9519b-120">The calling pin ignores the **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9519b-121">備註</span><span class="sxs-lookup"><span data-stu-id="9519b-121">Remarks</span></span>

<span data-ttu-id="9519b-122">這個方法可讓應用程式在處理緩衝區內容之前，先檢查媒體緩衝區中的資訊並採取行動。</span><span class="sxs-lookup"><span data-stu-id="9519b-122">This method enables an application to examine and act on information in the media buffer before the buffer contents are processed.</span></span> <span data-ttu-id="9519b-123">應用程式會負責瞭解 pin 上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9519b-123">The application is responsible for knowing the media type on the pin.</span></span> <span data-ttu-id="9519b-124">您可以先從設定檔取得串流資訊，然後呼叫 [**IConfigAsfWriter2：： StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) 方法來判斷哪個 pin 與每個資料流程相關聯，藉以取得這項資訊。</span><span class="sxs-lookup"><span data-stu-id="9519b-124">This information can be obtained by first getting the stream information from the profile and then calling [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) method to determine which pin is associated with each stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="9519b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9519b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9519b-126">**DirectShow QASF 參考**</span><span class="sxs-lookup"><span data-stu-id="9519b-126">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="9519b-127">**IAMWMBufferPassCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="9519b-127">**IAMWMBufferPassCallback Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[<span data-ttu-id="9519b-128">**INSSBuffer3 介面**</span><span class="sxs-lookup"><span data-stu-id="9519b-128">**INSSBuffer3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 