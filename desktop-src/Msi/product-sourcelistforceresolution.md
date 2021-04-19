---
description: SourceListForceResolution 方法會清除 LastUsedSource 屬性。
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: SourceListForceResolution 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990730"
---
# <a name="productsourcelistforceresolution-method"></a><span data-ttu-id="4ba83-103">SourceListForceResolution 方法</span><span class="sxs-lookup"><span data-stu-id="4ba83-103">Product.SourceListForceResolution method</span></span>

<span data-ttu-id="4ba83-104">**SourceListForceResolution** 方法會清除 LastUsedSource 屬性。</span><span class="sxs-lookup"><span data-stu-id="4ba83-104">The **SourceListForceResolution** method clears the LastUsedSource property.</span></span> <span data-ttu-id="4ba83-105">這會強制安裝程式在下次需要來源時，在來源清單中搜尋有效的產品來源，例如，當安裝程式執行安裝或重新安裝時，或是當元件設定為從來源執行時需要路徑。</span><span class="sxs-lookup"><span data-stu-id="4ba83-105">This forces the installer to search the source list for a valid product source the next time a source is required, such as when the installer performs an installation or a reinstallation, or when the path is required for a component set to run from the source.</span></span>

<span data-ttu-id="4ba83-106">這個方法會呼叫 [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)。</span><span class="sxs-lookup"><span data-stu-id="4ba83-106">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba83-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ba83-107">Syntax</span></span>


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="4ba83-108">參數</span><span class="sxs-lookup"><span data-stu-id="4ba83-108">Parameters</span></span>

<span data-ttu-id="4ba83-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4ba83-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ba83-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ba83-110">Return value</span></span>

<span data-ttu-id="4ba83-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4ba83-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ba83-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ba83-112">Requirements</span></span>



| <span data-ttu-id="4ba83-113">需求</span><span class="sxs-lookup"><span data-stu-id="4ba83-113">Requirement</span></span> | <span data-ttu-id="4ba83-114">值</span><span class="sxs-lookup"><span data-stu-id="4ba83-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba83-115">版本</span><span class="sxs-lookup"><span data-stu-id="4ba83-115">Version</span></span><br/> | <span data-ttu-id="4ba83-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4ba83-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4ba83-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4ba83-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4ba83-118">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4ba83-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="4ba83-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4ba83-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4ba83-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ba83-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="4ba83-121">IID</span><span class="sxs-lookup"><span data-stu-id="4ba83-121">IID</span></span><br/>     | <span data-ttu-id="4ba83-122">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4ba83-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="4ba83-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ba83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba83-124">**產品**</span><span class="sxs-lookup"><span data-stu-id="4ba83-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="4ba83-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="4ba83-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="4ba83-126">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="4ba83-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




