---
description: 安裝程式會在初始化時將 ProductState 屬性設定為產品的安裝狀態。
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: ProductState 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994918"
---
# <a name="productstate-property"></a><span data-ttu-id="9286d-103">ProductState 屬性</span><span class="sxs-lookup"><span data-stu-id="9286d-103">ProductState property</span></span>

<span data-ttu-id="9286d-104">安裝程式會在初始化時將 **ProductState** 屬性設定為產品的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="9286d-104">The installer sets the **ProductState** property to the installation state for the product at initialization.</span></span> <span data-ttu-id="9286d-105">這個屬性會設定為下列其中一個 [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)所傳回的 INSTALLSTATE 資料類型。</span><span class="sxs-lookup"><span data-stu-id="9286d-105">This property is set to one of the following INSTALLSTATE data types returned by [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span></span>



| <span data-ttu-id="9286d-106">INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="9286d-106">INSTALLSTATE</span></span>             | <span data-ttu-id="9286d-107">數值</span><span class="sxs-lookup"><span data-stu-id="9286d-107">Numeric value</span></span> | <span data-ttu-id="9286d-108">產品的安裝狀態</span><span class="sxs-lookup"><span data-stu-id="9286d-108">Installation state of product</span></span>                   |
|--------------------------|---------------|-------------------------------------------------|
| <span data-ttu-id="9286d-109">INSTALLSTATE \_ 不明</span><span class="sxs-lookup"><span data-stu-id="9286d-109">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="9286d-110">-1</span><span class="sxs-lookup"><span data-stu-id="9286d-110">-1</span></span>            | <span data-ttu-id="9286d-111">未公告或安裝產品。</span><span class="sxs-lookup"><span data-stu-id="9286d-111">The product is neither advertised or installed.</span></span> |
| <span data-ttu-id="9286d-112">INSTALLSTATE \_ 公告</span><span class="sxs-lookup"><span data-stu-id="9286d-112">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="9286d-113">1</span><span class="sxs-lookup"><span data-stu-id="9286d-113">1</span></span>             | <span data-ttu-id="9286d-114">產品已公告但未安裝。</span><span class="sxs-lookup"><span data-stu-id="9286d-114">The product is advertised but not installed.</span></span>    |
| <span data-ttu-id="9286d-115">INSTALLSTATE 不 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="9286d-115">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="9286d-116">2</span><span class="sxs-lookup"><span data-stu-id="9286d-116">2</span></span>             | <span data-ttu-id="9286d-117">已針對不同的使用者安裝產品。</span><span class="sxs-lookup"><span data-stu-id="9286d-117">The product is installed for a different user.</span></span>  |
| <span data-ttu-id="9286d-118">INSTALLSTATE \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="9286d-118">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="9286d-119">5</span><span class="sxs-lookup"><span data-stu-id="9286d-119">5</span></span>             | <span data-ttu-id="9286d-120">已為目前使用者安裝產品。</span><span class="sxs-lookup"><span data-stu-id="9286d-120">The product is installed for the current user.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="9286d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9286d-121">Requirements</span></span>



| <span data-ttu-id="9286d-122">需求</span><span class="sxs-lookup"><span data-stu-id="9286d-122">Requirement</span></span> | <span data-ttu-id="9286d-123">值</span><span class="sxs-lookup"><span data-stu-id="9286d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9286d-124">版本</span><span class="sxs-lookup"><span data-stu-id="9286d-124">Version</span></span><br/> | <span data-ttu-id="9286d-125">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9286d-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9286d-126">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9286d-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9286d-127">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="9286d-127">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9286d-128">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="9286d-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9286d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9286d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9286d-130">屬性</span><span class="sxs-lookup"><span data-stu-id="9286d-130">Properties</span></span>](properties.md)
</dt> </dl>

 

 




