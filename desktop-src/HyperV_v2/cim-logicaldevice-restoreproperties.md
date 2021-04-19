---
description: 要求裝置從備份存放區重新建立其設定、設定及/或狀態資訊。
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: CIM_LogicalDevice 類別的 RestoreProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987765"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="f1e4e-103">CIM LogicalDevice 類別的 RestoreProperties 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f1e4e-103">RestoreProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="f1e4e-104">要求裝置從備份存放區重新建立其設定、設定及/或狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f1e4e-104">Requests that the Device re-establish its configuration, setup and/or state information from a backing store.</span></span> <span data-ttu-id="f1e4e-105">其目的是要透過 SaveProperties 方法) 在較早的時間來捕捉這項資訊 (，並使用它將裝置傳回到先前的「條件」。</span><span class="sxs-lookup"><span data-stu-id="f1e4e-105">The intent is to capture this information at an earlier time (via the SaveProperties method), and use it to return a Device to this earlier "condition".</span></span> <span data-ttu-id="f1e4e-106">並非所有裝置都支援此方法。</span><span class="sxs-lookup"><span data-stu-id="f1e4e-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="f1e4e-107">如果成功，方法應該會傳回0，如果要求不受支援則傳回1，如果發生任何其他錯誤，則傳回其他值。</span><span class="sxs-lookup"><span data-stu-id="f1e4e-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="f1e4e-108">在子類別中，可以使用方法上的 ValueMap 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="f1e4e-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="f1e4e-109">您也可以在子類別中，以值陣列限定詞的形式指定可將 ValueMap 內容「轉譯」的字串。</span><span class="sxs-lookup"><span data-stu-id="f1e4e-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e4e-110">語法</span><span class="sxs-lookup"><span data-stu-id="f1e4e-110">Syntax</span></span>


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a><span data-ttu-id="f1e4e-111">參數</span><span class="sxs-lookup"><span data-stu-id="f1e4e-111">Parameters</span></span>

<span data-ttu-id="f1e4e-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f1e4e-112">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e4e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1e4e-113">Requirements</span></span>



| <span data-ttu-id="f1e4e-114">需求</span><span class="sxs-lookup"><span data-stu-id="f1e4e-114">Requirement</span></span> | <span data-ttu-id="f1e4e-115">值</span><span class="sxs-lookup"><span data-stu-id="f1e4e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e4e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1e4e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e4e-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f1e4e-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f1e4e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1e4e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e4e-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f1e4e-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f1e4e-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="f1e4e-120">Namespace</span></span><br/>                | <span data-ttu-id="f1e4e-121">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1e4e-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f1e4e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="f1e4e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1e4e-123"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f1e4e-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1e4e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f1e4e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1e4e-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1e4e-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1e4e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1e4e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e4e-127">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="f1e4e-127">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




