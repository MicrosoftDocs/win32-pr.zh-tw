---
description: 安裝程式物件的 UseFeature 方法會遞增特定功能的使用計數，並傳回該功能的安裝狀態。 這個方法應該用來表示應用程式使用功能的意圖。
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: UseFeature 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001932"
---
# <a name="installerusefeature-method"></a><span data-ttu-id="d6c17-104">UseFeature 方法</span><span class="sxs-lookup"><span data-stu-id="d6c17-104">Installer.UseFeature method</span></span>

<span data-ttu-id="d6c17-105">[**安裝程式**](installer-object.md)物件的 **UseFeature** 方法會遞增特定功能的使用計數，並傳回該功能的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="d6c17-105">The **UseFeature** method of the [**Installer**](installer-object.md) object increments the usage count for a particular feature and returns the installation state for that feature.</span></span> <span data-ttu-id="d6c17-106">這個方法應該用來表示應用程式使用功能的意圖。</span><span class="sxs-lookup"><span data-stu-id="d6c17-106">This method should be used to indicate an application's intent to use a feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c17-107">語法</span><span class="sxs-lookup"><span data-stu-id="d6c17-107">Syntax</span></span>


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="d6c17-108">參數</span><span class="sxs-lookup"><span data-stu-id="d6c17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c17-109">*產品*</span><span class="sxs-lookup"><span data-stu-id="d6c17-109">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c17-110">指定產品的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="d6c17-110">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="d6c17-111">*功能*</span><span class="sxs-lookup"><span data-stu-id="d6c17-111">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c17-112">識別要使用的功能。</span><span class="sxs-lookup"><span data-stu-id="d6c17-112">Identifies the feature to be used.</span></span>

</dd> <dt>

<span data-ttu-id="d6c17-113">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="d6c17-113">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c17-114">此參數必須是 *msiInstallModeNoDetection*。</span><span class="sxs-lookup"><span data-stu-id="d6c17-114">This parameter must be *msiInstallModeNoDetection*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c17-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6c17-115">Return value</span></span>

<span data-ttu-id="d6c17-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d6c17-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c17-117">備註</span><span class="sxs-lookup"><span data-stu-id="d6c17-117">Remarks</span></span>

<span data-ttu-id="d6c17-118">**UseFeature** 方法只能用於已知要發行的功能。</span><span class="sxs-lookup"><span data-stu-id="d6c17-118">The **UseFeature** method should only be used on features known to be published.</span></span> <span data-ttu-id="d6c17-119">應用程式應該藉由呼叫 [**FeatureState**](installer-featurestate.md) 屬性或 [**功能**](installer-features.md) 屬性或其對等 API 來判斷功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="d6c17-119">The application should determine the status of the feature by calling either the [**FeatureState**](installer-featurestate.md) property or [**Features**](installer-features.md) property or their API equivalents.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c17-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6c17-120">Requirements</span></span>



| <span data-ttu-id="d6c17-121">需求</span><span class="sxs-lookup"><span data-stu-id="d6c17-121">Requirement</span></span> | <span data-ttu-id="d6c17-122">值</span><span class="sxs-lookup"><span data-stu-id="d6c17-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c17-123">版本</span><span class="sxs-lookup"><span data-stu-id="d6c17-123">Version</span></span><br/> | <span data-ttu-id="d6c17-124">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d6c17-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6c17-125">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d6c17-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6c17-126">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d6c17-126">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d6c17-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d6c17-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="d6c17-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6c17-128"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d6c17-129">IID</span><span class="sxs-lookup"><span data-stu-id="d6c17-129">IID</span></span><br/>     | <span data-ttu-id="d6c17-130">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d6c17-130">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="d6c17-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6c17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c17-132">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="d6c17-132">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




