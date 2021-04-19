---
description: 傳回 RecordList 物件，這個物件會列舉產品清單。
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: ProductsEx 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992957"
---
# <a name="installerproductsex-property"></a><span data-ttu-id="a3e96-103">ProductsEx 屬性</span><span class="sxs-lookup"><span data-stu-id="a3e96-103">Installer.ProductsEx property</span></span>

<span data-ttu-id="a3e96-104">**ProductsEx** 屬性會傳回列舉產品清單的 [**RecordList**](recordlist-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="a3e96-104">The **ProductsEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of products.</span></span> <span data-ttu-id="a3e96-105">這個屬性會呼叫 [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)。</span><span class="sxs-lookup"><span data-stu-id="a3e96-105">This property calls [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span></span>

<span data-ttu-id="a3e96-106">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a3e96-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e96-107">語法</span><span class="sxs-lookup"><span data-stu-id="a3e96-107">Syntax</span></span>


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a><span data-ttu-id="a3e96-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="a3e96-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e96-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3e96-109">Requirements</span></span>



| <span data-ttu-id="a3e96-110">需求</span><span class="sxs-lookup"><span data-stu-id="a3e96-110">Requirement</span></span> | <span data-ttu-id="a3e96-111">值</span><span class="sxs-lookup"><span data-stu-id="a3e96-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e96-112">版本</span><span class="sxs-lookup"><span data-stu-id="a3e96-112">Version</span></span><br/> | <span data-ttu-id="a3e96-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a3e96-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a3e96-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a3e96-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a3e96-115">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a3e96-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="a3e96-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e96-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3e96-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e96-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="a3e96-118">IID</span><span class="sxs-lookup"><span data-stu-id="a3e96-118">IID</span></span><br/>     | <span data-ttu-id="a3e96-119">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a3e96-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="a3e96-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3e96-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e96-121">**安裝程式**</span><span class="sxs-lookup"><span data-stu-id="a3e96-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="a3e96-122">**MsiEnumProductsEx**</span><span class="sxs-lookup"><span data-stu-id="a3e96-122">**MsiEnumProductsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="a3e96-123">**產品**</span><span class="sxs-lookup"><span data-stu-id="a3e96-123">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="a3e96-124">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="a3e96-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




