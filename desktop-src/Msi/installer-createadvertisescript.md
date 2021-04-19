---
description: 安裝程式物件的 CreateAdvertiseScript 方法會產生公告腳本。
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: Installer：： CreateAdvertiseScript 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980246"
---
# <a name="installercreateadvertisescript-method"></a><span data-ttu-id="c50a4-103">Installer：： CreateAdvertiseScript 方法</span><span class="sxs-lookup"><span data-stu-id="c50a4-103">Installer::CreateAdvertiseScript method</span></span>

<span data-ttu-id="c50a4-104">[**安裝程式**](installer-object.md)物件的 **CreateAdvertiseScript** 方法會產生公告腳本。</span><span class="sxs-lookup"><span data-stu-id="c50a4-104">The **CreateAdvertiseScript** method of the [**Installer**](installer-object.md) object generates an advertise script.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="c50a4-105">Syntax</span></span>


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="c50a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="c50a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50a4-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="c50a4-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="c50a4-108">要公告的 Windows Installer 封裝 ( .msi) 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="c50a4-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="c50a4-109">*scriptFilePath*</span><span class="sxs-lookup"><span data-stu-id="c50a4-109">*scriptFilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="c50a4-110">要以公告的資訊建立之腳本檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="c50a4-110">The full path to the script file to be created with the advertised information.</span></span>

</dd> <dt>

<span data-ttu-id="c50a4-111">*變換*</span><span class="sxs-lookup"><span data-stu-id="c50a4-111">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="c50a4-112">要套用至產品的轉換清單。</span><span class="sxs-lookup"><span data-stu-id="c50a4-112">The list of transforms to apply to the product.</span></span> <span data-ttu-id="c50a4-113">清單中的轉換會以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="c50a4-113">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="c50a4-114">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="c50a4-114">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="c50a4-115">*language*</span><span class="sxs-lookup"><span data-stu-id="c50a4-115">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="c50a4-116">要使用之安裝套件的語言。</span><span class="sxs-lookup"><span data-stu-id="c50a4-116">The language of the installation package to use.</span></span> <span data-ttu-id="c50a4-117">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="c50a4-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="c50a4-118">*平台*</span><span class="sxs-lookup"><span data-stu-id="c50a4-118">*platform*</span></span> 
</dt> <dd>

<span data-ttu-id="c50a4-119">此參數會指定安裝程式應建立腳本的平臺。</span><span class="sxs-lookup"><span data-stu-id="c50a4-119">This parameter specifies for which platform the installer should create the script.</span></span> <span data-ttu-id="c50a4-120">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c50a4-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c50a4-121">值</span><span class="sxs-lookup"><span data-stu-id="c50a4-121">Value</span></span>                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="c50a4-122">意義</span><span class="sxs-lookup"><span data-stu-id="c50a4-122">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <span data-ttu-id="c50a4-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c50a4-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="c50a4-124">建立目前平臺的腳本。</span><span class="sxs-lookup"><span data-stu-id="c50a4-124">Creates a script for the current platform.</span></span><br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <span data-ttu-id="c50a4-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c50a4-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="c50a4-126">建立 x86 平臺的腳本。</span><span class="sxs-lookup"><span data-stu-id="c50a4-126">Creates a script for the x86 platform.</span></span><br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <span data-ttu-id="c50a4-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c50a4-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="c50a4-128">建立 Itanium 型系統的腳本。</span><span class="sxs-lookup"><span data-stu-id="c50a4-128">Creates a script for Itanium-based systems.</span></span><br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <span data-ttu-id="c50a4-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c50a4-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="c50a4-130">建立 x64 平臺的腳本。</span><span class="sxs-lookup"><span data-stu-id="c50a4-130">Creates a script for the x64 platform.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="c50a4-131">*options*</span><span class="sxs-lookup"><span data-stu-id="c50a4-131">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="c50a4-132">公告選項。</span><span class="sxs-lookup"><span data-stu-id="c50a4-132">Advertisement options.</span></span> <span data-ttu-id="c50a4-133">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="c50a4-133">This parameter is optional.</span></span> <span data-ttu-id="c50a4-134">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c50a4-134">This parameter can be one of the following values.</span></span> <span data-ttu-id="c50a4-135">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="c50a4-135">This parameter is optional.</span></span>



| <span data-ttu-id="c50a4-136">值</span><span class="sxs-lookup"><span data-stu-id="c50a4-136">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="c50a4-137">意義</span><span class="sxs-lookup"><span data-stu-id="c50a4-137">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="c50a4-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c50a4-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="c50a4-139">標準公告</span><span class="sxs-lookup"><span data-stu-id="c50a4-139">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="c50a4-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c50a4-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c50a4-141">通告產品的新實例。</span><span class="sxs-lookup"><span data-stu-id="c50a4-141">Advertises a new instance of the product.</span></span> <span data-ttu-id="c50a4-142">需要 *轉換* 參數之轉換清單中的第一個轉換是變更產品代碼的實例轉換。</span><span class="sxs-lookup"><span data-stu-id="c50a4-142">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="c50a4-143">如需詳細資訊，請參閱 [安裝多個產品和修補程式實例](installing-multiple-instances-of-products-and-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="c50a4-143">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50a4-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="c50a4-144">Return value</span></span>

<span data-ttu-id="c50a4-145">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c50a4-145">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c50a4-146">備註</span><span class="sxs-lookup"><span data-stu-id="c50a4-146">Remarks</span></span>

<span data-ttu-id="c50a4-147">[**AdvertiseProduct**](installer-advertiseproduct.md)方法會使用 [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)函數。</span><span class="sxs-lookup"><span data-stu-id="c50a4-147">The [**AdvertiseProduct**](installer-advertiseproduct.md) method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="c50a4-148">範例</span><span class="sxs-lookup"><span data-stu-id="c50a4-148">Examples</span></span>

<span data-ttu-id="c50a4-149">下列範例示範如何使用 **CreateAdvertiseScript** 方法。</span><span class="sxs-lookup"><span data-stu-id="c50a4-149">The following example demonstrates the use of the **CreateAdvertiseScript** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a><span data-ttu-id="c50a4-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="c50a4-150">Requirements</span></span>



| <span data-ttu-id="c50a4-151">需求</span><span class="sxs-lookup"><span data-stu-id="c50a4-151">Requirement</span></span> | <span data-ttu-id="c50a4-152">值</span><span class="sxs-lookup"><span data-stu-id="c50a4-152">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c50a4-153">版本</span><span class="sxs-lookup"><span data-stu-id="c50a4-153">Version</span></span><br/> | <span data-ttu-id="c50a4-154">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c50a4-154">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c50a4-155">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c50a4-155">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c50a4-156">Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5</span><span class="sxs-lookup"><span data-stu-id="c50a4-156">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="c50a4-157">DLL</span><span class="sxs-lookup"><span data-stu-id="c50a4-157">DLL</span></span><br/>     | <dl> <span data-ttu-id="c50a4-158"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c50a4-158"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="c50a4-159">IID</span><span class="sxs-lookup"><span data-stu-id="c50a4-159">IID</span></span><br/>     | <span data-ttu-id="c50a4-160">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c50a4-160">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="c50a4-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c50a4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50a4-162">**安裝程式**</span><span class="sxs-lookup"><span data-stu-id="c50a4-162">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="c50a4-163">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="c50a4-163">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




