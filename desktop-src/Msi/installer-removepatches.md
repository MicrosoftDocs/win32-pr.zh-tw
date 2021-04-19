---
description: RemovePatches 方法會移除有資格接收修補程式的一或多個產品修補程式。 RemovePatches 方法會呼叫 MsiRemovePatches。
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: RemovePatches 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977760"
---
# <a name="installerremovepatches-method"></a><span data-ttu-id="29944-104">RemovePatches 方法</span><span class="sxs-lookup"><span data-stu-id="29944-104">Installer.RemovePatches method</span></span>

<span data-ttu-id="29944-105">**RemovePatches** 方法會移除有資格接收修補程式的一或多個產品修補程式。</span><span class="sxs-lookup"><span data-stu-id="29944-105">The **RemovePatches** method removes one or more patches to products eligible to receive the patch.</span></span> <span data-ttu-id="29944-106">**RemovePatches** 方法會呼叫 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)。</span><span class="sxs-lookup"><span data-stu-id="29944-106">The **RemovePatches** method calls [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span>

## <a name="syntax"></a><span data-ttu-id="29944-107">語法</span><span class="sxs-lookup"><span data-stu-id="29944-107">Syntax</span></span>


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a><span data-ttu-id="29944-108">參數</span><span class="sxs-lookup"><span data-stu-id="29944-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29944-109">*PatchList*</span><span class="sxs-lookup"><span data-stu-id="29944-109">*PatchList*</span></span> 
</dt> <dd>

<span data-ttu-id="29944-110">字串，包含要移除的修補程式清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="29944-110">A string that contains a semicolon delimited list of patches to remove.</span></span> <span data-ttu-id="29944-111">每個修補程式都可以用修補封裝的完整路徑或 patch GUID 來表示。</span><span class="sxs-lookup"><span data-stu-id="29944-111">Each patch can be represented by either the full path to the patch package or by patch GUID.</span></span> <span data-ttu-id="29944-112">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="29944-112">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="29944-113">*ProductCode*</span><span class="sxs-lookup"><span data-stu-id="29944-113">*ProductCode*</span></span> 
</dt> <dd>

<span data-ttu-id="29944-114">字串，其中包含要從中移除修補程式之產品的 GUID。</span><span class="sxs-lookup"><span data-stu-id="29944-114">A string with the GUID of the product from which the patches are to be removed.</span></span> <span data-ttu-id="29944-115">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="29944-115">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="29944-116">*UninstallType*</span><span class="sxs-lookup"><span data-stu-id="29944-116">*UninstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="29944-117">指定修補程式移除類型的整數值。</span><span class="sxs-lookup"><span data-stu-id="29944-117">An integer value that specifies the type of patch removal.</span></span> <span data-ttu-id="29944-118">此參數必須是 **msiInstallTypeSingleInstance**。</span><span class="sxs-lookup"><span data-stu-id="29944-118">This parameter must be **msiInstallTypeSingleInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="29944-119">*PropertyList*</span><span class="sxs-lookup"><span data-stu-id="29944-119">*PropertyList*</span></span> 
</dt> <dd>

<span data-ttu-id="29944-120">字串，指定要包含的屬性 = 值配對。</span><span class="sxs-lookup"><span data-stu-id="29944-120">A string that specifies the Property=Value pairs to include.</span></span> <span data-ttu-id="29944-121">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="29944-121">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29944-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="29944-122">Return value</span></span>

<span data-ttu-id="29944-123">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="29944-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29944-124">備註</span><span class="sxs-lookup"><span data-stu-id="29944-124">Remarks</span></span>

<span data-ttu-id="29944-125">請參閱 [卸載修補](uninstalling-patches.md) 程式以取得示範應用程式如何從使用者可用的所有產品中移除修補程式的範例。</span><span class="sxs-lookup"><span data-stu-id="29944-125">See [Uninstalling Patches](uninstalling-patches.md) for an example that demonstrates how an application can remove a patch from all products that are available to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="29944-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="29944-126">Requirements</span></span>



| <span data-ttu-id="29944-127">需求</span><span class="sxs-lookup"><span data-stu-id="29944-127">Requirement</span></span> | <span data-ttu-id="29944-128">值</span><span class="sxs-lookup"><span data-stu-id="29944-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29944-129">版本</span><span class="sxs-lookup"><span data-stu-id="29944-129">Version</span></span><br/> | <span data-ttu-id="29944-130">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="29944-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="29944-131">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="29944-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="29944-132">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="29944-132">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="29944-133">DLL</span><span class="sxs-lookup"><span data-stu-id="29944-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="29944-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29944-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="29944-135">IID</span><span class="sxs-lookup"><span data-stu-id="29944-135">IID</span></span><br/>     | <span data-ttu-id="29944-136">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="29944-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="29944-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29944-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29944-138">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="29944-138">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="29944-139">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="29944-139">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[<span data-ttu-id="29944-140">卸載修補程式</span><span class="sxs-lookup"><span data-stu-id="29944-140">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="29944-141">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="29944-141">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




