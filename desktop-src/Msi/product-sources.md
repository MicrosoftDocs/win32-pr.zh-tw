---
description: '[來源] 屬性會列舉產品實例的所有來源。'
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Product. 來源屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978426"
---
# <a name="productsources-property"></a><span data-ttu-id="9960c-103">Product. 來源屬性</span><span class="sxs-lookup"><span data-stu-id="9960c-103">Product.Sources property</span></span>

<span data-ttu-id="9960c-104">[ **來源** ] 屬性會列舉產品實例的所有來源。</span><span class="sxs-lookup"><span data-stu-id="9960c-104">The **Sources** property enumerates all the sources for the product instance.</span></span> <span data-ttu-id="9960c-105">這個屬性會呼叫 [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) 並傳回字串陣列，並接受來源型別做為引數。</span><span class="sxs-lookup"><span data-stu-id="9960c-105">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns the array of strings, and accepts the source type as argument.</span></span> <span data-ttu-id="9960c-106">來源類型可以是 MSISOURCETYPE \_ NETWORK 或 MSISOURCETYPE \_ URL。</span><span class="sxs-lookup"><span data-stu-id="9960c-106">The source type can be MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

<span data-ttu-id="9960c-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9960c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9960c-108">語法</span><span class="sxs-lookup"><span data-stu-id="9960c-108">Syntax</span></span>


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a><span data-ttu-id="9960c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="9960c-109">Property value</span></span>

<span data-ttu-id="9960c-110">要列舉的來源型別。</span><span class="sxs-lookup"><span data-stu-id="9960c-110">The type of source to enumerate.</span></span> <span data-ttu-id="9960c-111">值可以 *msiInstallSourceTypeNetwork* (1) 或 *msiInstallSourceTypeURL* (2) 。</span><span class="sxs-lookup"><span data-stu-id="9960c-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="9960c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9960c-112">Requirements</span></span>



| <span data-ttu-id="9960c-113">需求</span><span class="sxs-lookup"><span data-stu-id="9960c-113">Requirement</span></span> | <span data-ttu-id="9960c-114">值</span><span class="sxs-lookup"><span data-stu-id="9960c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9960c-115">版本</span><span class="sxs-lookup"><span data-stu-id="9960c-115">Version</span></span><br/> | <span data-ttu-id="9960c-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9960c-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9960c-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9960c-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9960c-118">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9960c-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9960c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9960c-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="9960c-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9960c-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9960c-121">IID</span><span class="sxs-lookup"><span data-stu-id="9960c-121">IID</span></span><br/>     | <span data-ttu-id="9960c-122">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9960c-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="9960c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9960c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9960c-124">**產品**</span><span class="sxs-lookup"><span data-stu-id="9960c-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="9960c-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="9960c-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="9960c-126">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="9960c-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




