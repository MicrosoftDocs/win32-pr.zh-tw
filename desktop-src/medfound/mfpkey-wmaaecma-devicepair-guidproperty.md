---
description: 識別應用程式目前與語音捕獲 DSP 搭配使用之音訊裝置的組合。
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: 'MFPKEY_WMAAECMA_DEVICEPAIR_GUID 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114429"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a><span data-ttu-id="ac331-103">MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="ac331-103">MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID Property</span></span>

<span data-ttu-id="ac331-104">識別應用程式目前與語音捕獲 DSP 搭配使用之音訊裝置的組合。</span><span class="sxs-lookup"><span data-stu-id="ac331-104">Identifies the combination of audio devices that the application is currently using with the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ac331-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="ac331-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ac331-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="ac331-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ac331-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="ac331-107">Data Type</span></span>

<span data-ttu-id="ac331-108">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="ac331-108">VT\_CLSID</span></span>

## <a name="applies-to"></a><span data-ttu-id="ac331-109">套用至</span><span class="sxs-lookup"><span data-stu-id="ac331-109">Applies To</span></span>

-   [<span data-ttu-id="ac331-110">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ac331-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="ac331-111">備註</span><span class="sxs-lookup"><span data-stu-id="ac331-111">Remarks</span></span>

<span data-ttu-id="ac331-112">如果您在篩選模式中使用 DSP，且 [MFPKEY \_ WMAAECMA 抓取 \_ \_ TS \_ 統計](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) 資料屬性的值為 VARIANT TRUE，請設定此屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ac331-112">Set this property if you are using the DSP in filter mode and the value of the [MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE.</span></span>

<span data-ttu-id="ac331-113">當 [**MFPKEY \_ WMAAECMA 抓取 \_ \_ TS \_ STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) 屬性為 VARIANT 時 \_ ，DSP 會收集來自音訊裝置之時間戳記的統計資料，並將此資訊儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="ac331-113">When the [**MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE, the DSP collects statistics about the time stamps from the audio devices and stores this information in the registry.</span></span> <span data-ttu-id="ac331-114">每個音訊捕獲裝置和音訊轉譯裝置的組合都會變更這些統計資料。</span><span class="sxs-lookup"><span data-stu-id="ac331-114">These statistics can change for each combination of audio capture device and audio rendering device.</span></span> <span data-ttu-id="ac331-115">因此，應用程式必須指派 GUID 以識別使用中裝置的特定組合。</span><span class="sxs-lookup"><span data-stu-id="ac331-115">Therefore, the application must assign a GUID to identify the particular combination of devices in use.</span></span> <span data-ttu-id="ac331-116">應用程式應該追蹤此 GUID，讓它可以在每次使用同一組音訊裝置時指派相同的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ac331-116">The application should keep track of this GUID, so that it can assign the same GUID whenever it uses the same pair of audio devices.</span></span>

<span data-ttu-id="ac331-117">如果您在來源模式中使用 DSP，則不需要設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ac331-117">If you are using the DSP in source mode, you do not need to set this property.</span></span> <span data-ttu-id="ac331-118">DSP 會根據 [MFPKEY \_ WMAAECMA \_ DEVICE [ \_ 索引](mfpkey-wmaaecma-device-indexesproperty.md) ] 屬性的值自動產生 GUID。</span><span class="sxs-lookup"><span data-stu-id="ac331-118">The DSP automatically generates a GUID based on the value of the [MFPKEY\_WMAAECMA\_DEVICE\_INDEXES](mfpkey-wmaaecma-device-indexesproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac331-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac331-119">Requirements</span></span>



| <span data-ttu-id="ac331-120">需求</span><span class="sxs-lookup"><span data-stu-id="ac331-120">Requirement</span></span> | <span data-ttu-id="ac331-121">值</span><span class="sxs-lookup"><span data-stu-id="ac331-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac331-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac331-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac331-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac331-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ac331-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac331-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac331-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac331-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac331-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ac331-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac331-127"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac331-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac331-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac331-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac331-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ac331-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ac331-130">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ac331-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
