---
description: 在並行安裝期間，安裝程式會將並行安裝會話中的 ParentProductCode 屬性設定為與父安裝會話中的 [ProductCode] 屬性相同的值。
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: ParentProductCode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82385a4df94d3a044f0ee6a77461d69e63cc6d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995795"
---
# <a name="parentproductcode-property"></a><span data-ttu-id="69e14-103">ParentProductCode 屬性</span><span class="sxs-lookup"><span data-stu-id="69e14-103">ParentProductCode property</span></span>

<span data-ttu-id="69e14-104">在並行安裝期間，安裝程式會將並行安裝會話中的 **ParentProductCode** 屬性設定為與父安裝會話中的 [ [**ProductCode**](productcode.md) ] 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="69e14-104">During a concurrent installation, the installer sets the **ParentProductCode** property in the concurrent installation's session to the same value as the [**ProductCode**](productcode.md) property in the parent installation's session.</span></span> <span data-ttu-id="69e14-105">父安裝會執行並行安裝動作來執行並行安裝。</span><span class="sxs-lookup"><span data-stu-id="69e14-105">Parent installations run the concurrent installation actions to perform a concurrent installation.</span></span> <span data-ttu-id="69e14-106">安裝套件可以藉由檢查這個屬性的值，判斷是否由並行安裝動作安裝。</span><span class="sxs-lookup"><span data-stu-id="69e14-106">An installation package can determine whether it is being installed by a concurrent installation action by checking the value of this property.</span></span>

> [!Note]  
> <span data-ttu-id="69e14-107">不建議將並行安裝用於安裝應用程式，以供公開發行。</span><span class="sxs-lookup"><span data-stu-id="69e14-107">Concurrent Installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="69e14-108">如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="69e14-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="69e14-109">如果 [RemoveExistingProducts](removeexistingproducts-action.md) 動作正在執行並行安裝，就不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="69e14-109">This property is not set if the concurrent installation is being run by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="69e14-110">備註</span><span class="sxs-lookup"><span data-stu-id="69e14-110">Remarks</span></span>

<span data-ttu-id="69e14-111">若要防止封裝安裝為並行安裝，請將下列其中一個條件陳述式加入至 [LaunchCondition](launchcondition-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="69e14-111">To prevent a package from ever being installed as a concurrent installation, add either of the following conditional statements to the [LaunchCondition](launchcondition-table.md) table.</span></span> <span data-ttu-id="69e14-112">這可防止另一個安裝執行的並行安裝動作來安裝套件。</span><span class="sxs-lookup"><span data-stu-id="69e14-112">This prevents the package from ever being installed by a concurrent installation action run by another installation.</span></span> <span data-ttu-id="69e14-113">這不會防止 [RemoveExistingProducts](removeexistingproducts-action.md) 動作安裝套件。</span><span class="sxs-lookup"><span data-stu-id="69e14-113">This does not prevent the package from being installed by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a><span data-ttu-id="69e14-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="69e14-114">Requirements</span></span>



| <span data-ttu-id="69e14-115">需求</span><span class="sxs-lookup"><span data-stu-id="69e14-115">Requirement</span></span> | <span data-ttu-id="69e14-116">值</span><span class="sxs-lookup"><span data-stu-id="69e14-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e14-117">版本</span><span class="sxs-lookup"><span data-stu-id="69e14-117">Version</span></span><br/> | <span data-ttu-id="69e14-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="69e14-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="69e14-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="69e14-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="69e14-120">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="69e14-120">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="69e14-121">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="69e14-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69e14-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69e14-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e14-123">屬性</span><span class="sxs-lookup"><span data-stu-id="69e14-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="69e14-124">**ParentOriginalDatabase**</span><span class="sxs-lookup"><span data-stu-id="69e14-124">**ParentOriginalDatabase**</span></span>](parentoriginaldatabase.md)
</dt> </dl>

 

 




