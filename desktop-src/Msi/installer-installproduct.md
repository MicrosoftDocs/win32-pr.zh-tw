---
description: 安裝程式物件的 InstallProduct 方法會開啟安裝程式套件，並初始化安裝會話。
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: InstallProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977153"
---
# <a name="installerinstallproduct-method"></a><span data-ttu-id="33c5d-103">InstallProduct 方法</span><span class="sxs-lookup"><span data-stu-id="33c5d-103">Installer.InstallProduct method</span></span>

<span data-ttu-id="33c5d-104">[**安裝程式**](installer-object.md)物件的 **InstallProduct** 方法會開啟安裝程式套件，並初始化安裝會話。</span><span class="sxs-lookup"><span data-stu-id="33c5d-104">The **InstallProduct** method of the [**Installer**](installer-object.md) object opens an installer package and initializes an install session.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c5d-105">語法</span><span class="sxs-lookup"><span data-stu-id="33c5d-105">Syntax</span></span>


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a><span data-ttu-id="33c5d-106">參數</span><span class="sxs-lookup"><span data-stu-id="33c5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c5d-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="33c5d-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="33c5d-108">必要的字串，其中包含安裝套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="33c5d-108">Required string containing the path to the install package.</span></span>

</dd> <dt>

<span data-ttu-id="33c5d-109">*propertyValues*</span><span class="sxs-lookup"><span data-stu-id="33c5d-109">*propertyValues*</span></span> 
</dt> <dd>

<span data-ttu-id="33c5d-110">選擇性字串，包含以空白字元分隔的屬性 = 值配對。</span><span class="sxs-lookup"><span data-stu-id="33c5d-110">Optional string containing property=value pairs separated by white space.</span></span>

<span data-ttu-id="33c5d-111">若要執行系統管理安裝，請在 *propertyValues* 中包含 ACTION = ADMIN。</span><span class="sxs-lookup"><span data-stu-id="33c5d-111">To perform an administrative installation, include ACTION=ADMIN in *propertyValues*.</span></span> <span data-ttu-id="33c5d-112">如需詳細資訊，請參閱 [**ACTION**](action.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="33c5d-112">For more information, see the [**ACTION**](action.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c5d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="33c5d-113">Return value</span></span>

<span data-ttu-id="33c5d-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="33c5d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33c5d-115">備註</span><span class="sxs-lookup"><span data-stu-id="33c5d-115">Remarks</span></span>

<span data-ttu-id="33c5d-116">若要完全移除產品，請在 *propertyValues* 中設定 REMOVE = ALL。</span><span class="sxs-lookup"><span data-stu-id="33c5d-116">To completely remove a product, set REMOVE=ALL in *propertyValues*.</span></span> <span data-ttu-id="33c5d-117">如需詳細資訊，請參閱 [**移除**](remove.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="33c5d-117">For more information, see [**REMOVE**](remove.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c5d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="33c5d-118">Requirements</span></span>



| <span data-ttu-id="33c5d-119">需求</span><span class="sxs-lookup"><span data-stu-id="33c5d-119">Requirement</span></span> | <span data-ttu-id="33c5d-120">值</span><span class="sxs-lookup"><span data-stu-id="33c5d-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c5d-121">版本</span><span class="sxs-lookup"><span data-stu-id="33c5d-121">Version</span></span><br/> | <span data-ttu-id="33c5d-122">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="33c5d-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="33c5d-123">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="33c5d-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="33c5d-124">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="33c5d-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="33c5d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="33c5d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="33c5d-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33c5d-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="33c5d-127">IID</span><span class="sxs-lookup"><span data-stu-id="33c5d-127">IID</span></span><br/>     | <span data-ttu-id="33c5d-128">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="33c5d-128">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




