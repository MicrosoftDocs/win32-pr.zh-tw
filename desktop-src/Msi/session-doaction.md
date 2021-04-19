---
description: Session 物件的 Dataadapter.doaction 方法會執行對應至提供之名稱的動作函數。
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: 'Dataadapter.doaction 方法 (Photoacquire .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989650"
---
# <a name="sessiondoaction-method"></a><span data-ttu-id="d072e-103">Dataadapter.doaction 方法</span><span class="sxs-lookup"><span data-stu-id="d072e-103">Session.DoAction method</span></span>

<span data-ttu-id="d072e-104">[**Session**](session-object.md)物件的 **dataadapter.doaction** 方法會執行對應至提供之名稱的動作函數。</span><span class="sxs-lookup"><span data-stu-id="d072e-104">The **DoAction** method of the [**Session**](session-object.md) object executes the action function corresponding to the name supplied.</span></span> <span data-ttu-id="d072e-105">如果提供 Null 動作名稱，引擎會使用 [action 屬性](action.md) 的大寫值做為要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="d072e-105">If a Null action name is supplied, the engine uses the uppercase value of the [ACTION property](action.md) as the action to perform.</span></span> <span data-ttu-id="d072e-106">如果未定義屬性值，則會執行預設動作，目前已定義為 [安裝]。</span><span class="sxs-lookup"><span data-stu-id="d072e-106">If no property value is defined, the default action is performed, currently defined as INSTALL.</span></span> <span data-ttu-id="d072e-107">這個方法會傳回整數列舉。</span><span class="sxs-lookup"><span data-stu-id="d072e-107">This method returns an integer enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d072e-108">語法</span><span class="sxs-lookup"><span data-stu-id="d072e-108">Syntax</span></span>


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a><span data-ttu-id="d072e-109">參數</span><span class="sxs-lookup"><span data-stu-id="d072e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d072e-110">*action*</span><span class="sxs-lookup"><span data-stu-id="d072e-110">*action*</span></span> 
</dt> <dd>

<span data-ttu-id="d072e-111">要執行的動作所需的字串名稱。</span><span class="sxs-lookup"><span data-stu-id="d072e-111">Required string name of the action to execute.</span></span> <span data-ttu-id="d072e-112">區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d072e-112">Case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d072e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d072e-113">Return value</span></span>

<span data-ttu-id="d072e-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d072e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d072e-115">備註</span><span class="sxs-lookup"><span data-stu-id="d072e-115">Remarks</span></span>

<span data-ttu-id="d072e-116">藉由呼叫 **dataadapter.doaction** 方法，無法執行更新系統的動作，例如 [InstallFiles](installfiles-action.md)和 [WriteRegistryValues](writeregistryvalues-action.md)動作。</span><span class="sxs-lookup"><span data-stu-id="d072e-116">Actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **DoAction** method.</span></span> <span data-ttu-id="d072e-117">這項規則的例外狀況是從 [InstallInitialize](installinitialize-action.md)和 [InstallFinalize 動作](installfinalize-action.md)之間 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中排程的自訂動作呼叫 **dataadapter.doaction** 方法。</span><span class="sxs-lookup"><span data-stu-id="d072e-117">The exception to this rule is if the **DoAction** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="d072e-118">您可以呼叫不會更新系統的動作，例如 [AppSearch](appsearch-action.md) 或 [CostInitialize](costinitialize-action.md)。</span><span class="sxs-lookup"><span data-stu-id="d072e-118">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d072e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d072e-119">Requirements</span></span>



| <span data-ttu-id="d072e-120">需求</span><span class="sxs-lookup"><span data-stu-id="d072e-120">Requirement</span></span> | <span data-ttu-id="d072e-121">值</span><span class="sxs-lookup"><span data-stu-id="d072e-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d072e-122">版本</span><span class="sxs-lookup"><span data-stu-id="d072e-122">Version</span></span><br/> | <span data-ttu-id="d072e-123">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d072e-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d072e-124">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d072e-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d072e-125">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d072e-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d072e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d072e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d072e-127"><dt>Photoacquire。h</dt></span><span class="sxs-lookup"><span data-stu-id="d072e-127"><dt>Photoacquire.h</dt></span></span> </dl>                                                                                                                                                               |
| <span data-ttu-id="d072e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d072e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d072e-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d072e-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d072e-130">IID</span><span class="sxs-lookup"><span data-stu-id="d072e-130">IID</span></span><br/>     | <span data-ttu-id="d072e-131">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d072e-131">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




