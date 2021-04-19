---
description: 安裝程式物件的 AdvertiseProduct 方法會通告安裝套件。
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: Installer：： AdvertiseProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987128"
---
# <a name="installeradvertiseproduct-method"></a><span data-ttu-id="4a45b-103">Installer：： AdvertiseProduct 方法</span><span class="sxs-lookup"><span data-stu-id="4a45b-103">Installer::AdvertiseProduct method</span></span>

<span data-ttu-id="4a45b-104">[**安裝程式**](installer-object.md)物件的 **AdvertiseProduct** 方法會通告安裝套件。</span><span class="sxs-lookup"><span data-stu-id="4a45b-104">The **AdvertiseProduct** method of the [**Installer**](installer-object.md) object advertises an installation package.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a45b-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a45b-105">Syntax</span></span>


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="4a45b-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a45b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a45b-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="4a45b-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="4a45b-108">要公告的 Windows Installer 封裝 ( .msi) 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4a45b-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="4a45b-109">*內容*</span><span class="sxs-lookup"><span data-stu-id="4a45b-109">*context*</span></span> 
</dt> <dd>

<span data-ttu-id="4a45b-110">公告的內容。</span><span class="sxs-lookup"><span data-stu-id="4a45b-110">The context of the advertisement.</span></span> <span data-ttu-id="4a45b-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4a45b-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4a45b-112">值</span><span class="sxs-lookup"><span data-stu-id="4a45b-112">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="4a45b-113">意義</span><span class="sxs-lookup"><span data-stu-id="4a45b-113">Meaning</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <span data-ttu-id="4a45b-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4a45b-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="4a45b-115">在每一部電腦的 [安裝內容](installation-context.md)中，為安裝通告應用程式。</span><span class="sxs-lookup"><span data-stu-id="4a45b-115">Advertises the application for an instalation in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="4a45b-116">這讓封裝可供電腦的所有使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="4a45b-116">This makes the package available for installation by all users of the computer.</span></span><br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <span data-ttu-id="4a45b-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4a45b-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="4a45b-118">在每個使用者 [安裝內容](installation-context.md)中通告應用程式以進行安裝。</span><span class="sxs-lookup"><span data-stu-id="4a45b-118">Advertises the application for an installation in the per-user [installation context](installation-context.md).</span></span><br/>                                                                                   |



 

</dd> <dt>

<span data-ttu-id="4a45b-119">*變換*</span><span class="sxs-lookup"><span data-stu-id="4a45b-119">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="4a45b-120">要套用至產品的轉換清單。</span><span class="sxs-lookup"><span data-stu-id="4a45b-120">The list of transforms to apply to the product.</span></span> <span data-ttu-id="4a45b-121">清單中的轉換會以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="4a45b-121">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="4a45b-122">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="4a45b-122">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4a45b-123">*language*</span><span class="sxs-lookup"><span data-stu-id="4a45b-123">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="4a45b-124">要使用之安裝套件的語言。</span><span class="sxs-lookup"><span data-stu-id="4a45b-124">The language of the installation package to use.</span></span> <span data-ttu-id="4a45b-125">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="4a45b-125">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4a45b-126">*options*</span><span class="sxs-lookup"><span data-stu-id="4a45b-126">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="4a45b-127">公告選項。</span><span class="sxs-lookup"><span data-stu-id="4a45b-127">The advertisement options.</span></span> <span data-ttu-id="4a45b-128">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="4a45b-128">This parameter is optional.</span></span> <span data-ttu-id="4a45b-129">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4a45b-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4a45b-130">值</span><span class="sxs-lookup"><span data-stu-id="4a45b-130">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="4a45b-131">意義</span><span class="sxs-lookup"><span data-stu-id="4a45b-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="4a45b-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4a45b-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="4a45b-133">標準公告</span><span class="sxs-lookup"><span data-stu-id="4a45b-133">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="4a45b-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4a45b-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="4a45b-135">通告產品的新實例。</span><span class="sxs-lookup"><span data-stu-id="4a45b-135">Advertises a new instance of the product.</span></span> <span data-ttu-id="4a45b-136">需要 *轉換* 參數之轉換清單中的第一個轉換是變更產品代碼的實例轉換。</span><span class="sxs-lookup"><span data-stu-id="4a45b-136">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="4a45b-137">如需詳細資訊，請參閱 [安裝多個產品和修補程式實例](installing-multiple-instances-of-products-and-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="4a45b-137">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a45b-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a45b-138">Return value</span></span>

<span data-ttu-id="4a45b-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4a45b-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a45b-140">備註</span><span class="sxs-lookup"><span data-stu-id="4a45b-140">Remarks</span></span>

<span data-ttu-id="4a45b-141">**AdvertiseProduct** 方法會使用 [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)函數。</span><span class="sxs-lookup"><span data-stu-id="4a45b-141">The **AdvertiseProduct** method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="4a45b-142">範例</span><span class="sxs-lookup"><span data-stu-id="4a45b-142">Examples</span></span>

<span data-ttu-id="4a45b-143">下列範例示範如何使用 **AdvertiseProduct** 方法。</span><span class="sxs-lookup"><span data-stu-id="4a45b-143">The following example demonstrates the use of the **AdvertiseProduct** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a><span data-ttu-id="4a45b-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a45b-144">Requirements</span></span>



| <span data-ttu-id="4a45b-145">需求</span><span class="sxs-lookup"><span data-stu-id="4a45b-145">Requirement</span></span> | <span data-ttu-id="4a45b-146">值</span><span class="sxs-lookup"><span data-stu-id="4a45b-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a45b-147">版本</span><span class="sxs-lookup"><span data-stu-id="4a45b-147">Version</span></span><br/> | <span data-ttu-id="4a45b-148">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4a45b-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4a45b-149">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4a45b-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4a45b-150">Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5</span><span class="sxs-lookup"><span data-stu-id="4a45b-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="4a45b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="4a45b-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="4a45b-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a45b-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="4a45b-153">IID</span><span class="sxs-lookup"><span data-stu-id="4a45b-153">IID</span></span><br/>     | <span data-ttu-id="4a45b-154">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4a45b-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="4a45b-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a45b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a45b-156">**安裝程式**</span><span class="sxs-lookup"><span data-stu-id="4a45b-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="4a45b-157">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="4a45b-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




