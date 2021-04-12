---
title: IConfigAsfWriter2 StreamNumFromPin 方法
description: StreamNumFromPin 方法會抓取與指定之輸入 pin 相關聯的資料流程號碼。
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- StreamNumFromPin 方法 windows Media 格式
- StreamNumFromPin 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，StreamNumFromPin 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375588"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a><span data-ttu-id="e11e3-106">IConfigAsfWriter2：： StreamNumFromPin 方法</span><span class="sxs-lookup"><span data-stu-id="e11e3-106">IConfigAsfWriter2::StreamNumFromPin method</span></span>

<span data-ttu-id="e11e3-107">**StreamNumFromPin** 方法會抓取與指定之輸入 pin 相關聯的資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="e11e3-107">The **StreamNumFromPin** method retrieves the stream number associated with the specified input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11e3-108">語法</span><span class="sxs-lookup"><span data-stu-id="e11e3-108">Syntax</span></span>


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a><span data-ttu-id="e11e3-109">參數</span><span class="sxs-lookup"><span data-stu-id="e11e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e11e3-110">*pPin* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e11e3-110">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e11e3-111">輸入釘選上 **IPin** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e11e3-111">Pointer to the **IPin** interface on the input pin.</span></span>

</dd> <dt>

<span data-ttu-id="e11e3-112">*pwStreamNum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e11e3-112">*pwStreamNum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e11e3-113">接收資料流程號碼的指標。</span><span class="sxs-lookup"><span data-stu-id="e11e3-113">Pointer that receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e11e3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e11e3-114">Return value</span></span>

<span data-ttu-id="e11e3-115">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e11e3-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e11e3-116">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e11e3-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e11e3-117">備註</span><span class="sxs-lookup"><span data-stu-id="e11e3-117">Remarks</span></span>

<span data-ttu-id="e11e3-118">有時，您可能需要直接使用 Windows Media Format SDK 介面來運算元據流，才能執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e11e3-118">Sometimes you may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running a filter graph.</span></span> <span data-ttu-id="e11e3-119">因為您無法假設 ASF 串流號碼與 DirectShow pin 碼相同，所以會提供這個方法。</span><span class="sxs-lookup"><span data-stu-id="e11e3-119">Because you cannot assume that an ASF stream number is the same as the DirectShow pin number, this method is provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="e11e3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e11e3-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="e11e3-121">[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e11e3-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

 