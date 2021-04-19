---
description: EnableDevice 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 RequestStateChange 方法。
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: CIM_LogicalDevice 類別的 EnableDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990322"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="501ab-103">CIM LogicalDevice 類別的 EnableDevice 方法 \_</span><span class="sxs-lookup"><span data-stu-id="501ab-103">EnableDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="501ab-104">EnableDevice 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 RequestStateChange 方法。</span><span class="sxs-lookup"><span data-stu-id="501ab-104">The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.</span></span>

<span data-ttu-id="501ab-105">要求啟用 LogicalDevice ( "Enabled" 輸入參數 = TRUE) 或停用 (= FALSE) 。</span><span class="sxs-lookup"><span data-stu-id="501ab-105">Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE).</span></span> <span data-ttu-id="501ab-106">如果成功，裝置的 StatusInfo/EnabledState 屬性應該會反映預期狀態 (啟用/停用) 。</span><span class="sxs-lookup"><span data-stu-id="501ab-106">If successful, the Device's StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled).</span></span> <span data-ttu-id="501ab-107">請注意，這個方法的函式與 RequestedState 屬性重迭。</span><span class="sxs-lookup"><span data-stu-id="501ab-107">Note that this method's function overlaps with the RequestedState property.</span></span> <span data-ttu-id="501ab-108">在模型中加入了 RequestedState 來維護記錄， (也就是最後一個狀態要求的保存值) 。</span><span class="sxs-lookup"><span data-stu-id="501ab-108">RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request.</span></span> <span data-ttu-id="501ab-109">叫用 EnableDevice 方法應該適當地設定 RequestedState 屬性。</span><span class="sxs-lookup"><span data-stu-id="501ab-109">Invoking the EnableDevice method should set the RequestedState property appropriately.</span></span>

<span data-ttu-id="501ab-110">如果要求成功執行，傳回碼應為0，如果不支援要求則為1，如果發生錯誤，則為其他值。</span><span class="sxs-lookup"><span data-stu-id="501ab-110">The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred.</span></span> <span data-ttu-id="501ab-111">在子類別中，可以使用方法上的 ValueMap 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="501ab-111">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="501ab-112">您也可以在子類別中，以值陣列限定詞的形式指定可將 ValueMap 內容「轉譯」的字串。</span><span class="sxs-lookup"><span data-stu-id="501ab-112">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="501ab-113">語法</span><span class="sxs-lookup"><span data-stu-id="501ab-113">Syntax</span></span>


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="501ab-114">參數</span><span class="sxs-lookup"><span data-stu-id="501ab-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="501ab-115">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="501ab-115">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="501ab-116">若為 TRUE，則啟用裝置，如果為 FALSE，則停用裝置。</span><span class="sxs-lookup"><span data-stu-id="501ab-116">If TRUE enable the device, if FALSE disable the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="501ab-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="501ab-117">Return value</span></span>

<span data-ttu-id="501ab-118">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="501ab-118">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="501ab-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="501ab-119">Requirements</span></span>



| <span data-ttu-id="501ab-120">需求</span><span class="sxs-lookup"><span data-stu-id="501ab-120">Requirement</span></span> | <span data-ttu-id="501ab-121">值</span><span class="sxs-lookup"><span data-stu-id="501ab-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="501ab-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="501ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="501ab-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="501ab-123">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="501ab-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="501ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="501ab-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="501ab-125">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="501ab-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="501ab-126">Namespace</span></span><br/>                | <span data-ttu-id="501ab-127">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="501ab-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="501ab-128">MOF</span><span class="sxs-lookup"><span data-stu-id="501ab-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="501ab-129"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="501ab-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="501ab-130">DLL</span><span class="sxs-lookup"><span data-stu-id="501ab-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="501ab-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="501ab-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="501ab-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="501ab-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501ab-133">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="501ab-133">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




