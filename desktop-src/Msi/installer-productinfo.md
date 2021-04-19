---
description: ProductInfo 屬性是唯讀屬性，可傳回已安裝或已發佈產品的指定屬性值。
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: 'ProductInfo 屬性 (Oemupgex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994879"
---
# <a name="installerproductinfo-property"></a><span data-ttu-id="cf889-103">ProductInfo 屬性</span><span class="sxs-lookup"><span data-stu-id="cf889-103">Installer.ProductInfo property</span></span>

<span data-ttu-id="cf889-104">**ProductInfo** 屬性是唯讀屬性，可傳回已安裝或已發佈產品的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="cf889-104">The **ProductInfo** property is a read-only property that returns the value of the specified attribute for an installed or published product.</span></span>

<span data-ttu-id="cf889-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="cf889-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf889-106">語法</span><span class="sxs-lookup"><span data-stu-id="cf889-106">Syntax</span></span>


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a><span data-ttu-id="cf889-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="cf889-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="cf889-108">備註</span><span class="sxs-lookup"><span data-stu-id="cf889-108">Remarks</span></span>

<span data-ttu-id="cf889-109">**ProductInfo** 屬性 ( "LocalPackage" ) 不一定會傳回快取封裝的路徑。</span><span class="sxs-lookup"><span data-stu-id="cf889-109">The **ProductInfo** property ("LocalPackage") does not necessarily return a path to the cached package.</span></span> <span data-ttu-id="cf889-110">不應從 LocalPackage 叫用維護模式安裝。</span><span class="sxs-lookup"><span data-stu-id="cf889-110">Maintenance mode installations should be not be invoked from the LocalPackage.</span></span> <span data-ttu-id="cf889-111">快取的封裝僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="cf889-111">The cached package is for internal uses only.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf889-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf889-112">Requirements</span></span>



| <span data-ttu-id="cf889-113">需求</span><span class="sxs-lookup"><span data-stu-id="cf889-113">Requirement</span></span> | <span data-ttu-id="cf889-114">值</span><span class="sxs-lookup"><span data-stu-id="cf889-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf889-115">版本</span><span class="sxs-lookup"><span data-stu-id="cf889-115">Version</span></span><br/> | <span data-ttu-id="cf889-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="cf889-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cf889-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="cf889-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cf889-118">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="cf889-118">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="cf889-119">標頭</span><span class="sxs-lookup"><span data-stu-id="cf889-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cf889-120"><dt>Oemupgex。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf889-120"><dt>Oemupgex.h</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="cf889-121">DLL</span><span class="sxs-lookup"><span data-stu-id="cf889-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf889-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf889-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="cf889-123">IID</span><span class="sxs-lookup"><span data-stu-id="cf889-123">IID</span></span><br/>     | <span data-ttu-id="cf889-124">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cf889-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="cf889-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf889-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf889-126">**MsiGetProductInfo**</span><span class="sxs-lookup"><span data-stu-id="cf889-126">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="cf889-127">**MsiGetUserInfo**</span><span class="sxs-lookup"><span data-stu-id="cf889-127">**MsiGetUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[<span data-ttu-id="cf889-128">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="cf889-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




