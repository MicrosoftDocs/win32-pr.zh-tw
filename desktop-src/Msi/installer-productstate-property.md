---
description: ProductState 屬性是唯讀屬性，可傳回產品的安裝狀態資訊。
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: ProductState 屬性方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994745"
---
# <a name="installerproductstate-property-method"></a><span data-ttu-id="2dd5c-103">ProductState 屬性方法</span><span class="sxs-lookup"><span data-stu-id="2dd5c-103">Installer.ProductState Property method</span></span>

<span data-ttu-id="2dd5c-104">**ProductState 屬性** 是唯讀屬性，可傳回產品的安裝狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-104">The **ProductState property** is a read-only property that returns the install state information for a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd5c-105">語法</span><span class="sxs-lookup"><span data-stu-id="2dd5c-105">Syntax</span></span>


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="2dd5c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2dd5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd5c-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="2dd5c-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="2dd5c-108">指定產品的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-108">Specifies the product code of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dd5c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2dd5c-109">Return value</span></span>

<span data-ttu-id="2dd5c-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dd5c-111">備註</span><span class="sxs-lookup"><span data-stu-id="2dd5c-111">Remarks</span></span>

<span data-ttu-id="2dd5c-112">傳回下表所示的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-112">Returns one of the values shown in the following table.</span></span>



| <span data-ttu-id="2dd5c-113">安裝狀態</span><span class="sxs-lookup"><span data-stu-id="2dd5c-113">Installation state</span></span>        | <span data-ttu-id="2dd5c-114">Description</span><span class="sxs-lookup"><span data-stu-id="2dd5c-114">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="2dd5c-115">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="2dd5c-115">msiInstallStateAbsent</span></span>     | <span data-ttu-id="2dd5c-116">已針對不同的使用者安裝產品。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-116">The product is installed for a different user.</span></span>   |
| <span data-ttu-id="2dd5c-117">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="2dd5c-117">msiInstallStateDefault</span></span>    | <span data-ttu-id="2dd5c-118">已為目前使用者安裝產品。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-118">The product is installed for the current user.</span></span>   |
| <span data-ttu-id="2dd5c-119">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="2dd5c-119">msiInstallStateAdvertised</span></span> | <span data-ttu-id="2dd5c-120">產品已公告但未安裝。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-120">The product is advertised but not installed.</span></span>     |
| <span data-ttu-id="2dd5c-121">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="2dd5c-121">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="2dd5c-122">傳遞給函數的參數無效。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-122">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="2dd5c-123">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="2dd5c-123">msiInstallStateUnknown</span></span>    | <span data-ttu-id="2dd5c-124">這項產品未公告或安裝。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-124">The product is neither advertised nor installed.</span></span> |
| <span data-ttu-id="2dd5c-125">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="2dd5c-125">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="2dd5c-126">設定資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-126">The configuration data is corrupt.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="2dd5c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dd5c-127">Requirements</span></span>



| <span data-ttu-id="2dd5c-128">需求</span><span class="sxs-lookup"><span data-stu-id="2dd5c-128">Requirement</span></span> | <span data-ttu-id="2dd5c-129">值</span><span class="sxs-lookup"><span data-stu-id="2dd5c-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd5c-130">版本</span><span class="sxs-lookup"><span data-stu-id="2dd5c-130">Version</span></span><br/> | <span data-ttu-id="2dd5c-131">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2dd5c-132">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="2dd5c-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2dd5c-133">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2dd5c-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2dd5c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2dd5c-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="2dd5c-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dd5c-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2dd5c-136">IID</span><span class="sxs-lookup"><span data-stu-id="2dd5c-136">IID</span></span><br/>     | <span data-ttu-id="2dd5c-137">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2dd5c-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="2dd5c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dd5c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd5c-139">**MsiQueryProductState**</span><span class="sxs-lookup"><span data-stu-id="2dd5c-139">**MsiQueryProductState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




