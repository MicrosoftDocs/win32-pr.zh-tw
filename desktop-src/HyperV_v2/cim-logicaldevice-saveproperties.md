---
description: 要求裝置在備份存放區中捕獲其目前的設定、設定及/或狀態資訊。
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: CIM_LogicalDevice 類別的 SaveProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983876"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="85dd4-103">CIM LogicalDevice 類別的 SaveProperties 方法 \_</span><span class="sxs-lookup"><span data-stu-id="85dd4-103">SaveProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="85dd4-104">要求裝置在備份存放區中捕獲其目前的設定、設定及/或狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="85dd4-104">Requests that the Device capture its current configuration, setup and/or state information in a backing store.</span></span> <span data-ttu-id="85dd4-105">目標是在稍後透過 RestoreProperties 方法) 來使用這項資訊 (，以將裝置傳回到其目前的「條件」。</span><span class="sxs-lookup"><span data-stu-id="85dd4-105">The goal would be to use this information at a later time (via the RestoreProperties method), to return a Device to its present "condition".</span></span> <span data-ttu-id="85dd4-106">並非所有裝置都支援此方法。</span><span class="sxs-lookup"><span data-stu-id="85dd4-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="85dd4-107">如果成功，方法應該會傳回0，如果要求不受支援則傳回1，如果發生任何其他錯誤，則傳回其他值。</span><span class="sxs-lookup"><span data-stu-id="85dd4-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="85dd4-108">在子類別中，可以使用方法上的 ValueMap 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="85dd4-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="85dd4-109">您也可以在子類別中，以值陣列限定詞的形式指定可將 ValueMap 內容「轉譯」的字串。</span><span class="sxs-lookup"><span data-stu-id="85dd4-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="85dd4-110">語法</span><span class="sxs-lookup"><span data-stu-id="85dd4-110">Syntax</span></span>


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a><span data-ttu-id="85dd4-111">參數</span><span class="sxs-lookup"><span data-stu-id="85dd4-111">Parameters</span></span>

<span data-ttu-id="85dd4-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="85dd4-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85dd4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="85dd4-113">Return value</span></span>

<span data-ttu-id="85dd4-114">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="85dd4-114">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="85dd4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="85dd4-115">Requirements</span></span>



| <span data-ttu-id="85dd4-116">需求</span><span class="sxs-lookup"><span data-stu-id="85dd4-116">Requirement</span></span> | <span data-ttu-id="85dd4-117">值</span><span class="sxs-lookup"><span data-stu-id="85dd4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85dd4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85dd4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85dd4-119">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="85dd4-119">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="85dd4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85dd4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85dd4-121">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="85dd4-121">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="85dd4-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="85dd4-122">Namespace</span></span><br/>                | <span data-ttu-id="85dd4-123">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="85dd4-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="85dd4-124">MOF</span><span class="sxs-lookup"><span data-stu-id="85dd4-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85dd4-125"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="85dd4-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85dd4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="85dd4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85dd4-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85dd4-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85dd4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85dd4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85dd4-129">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="85dd4-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




