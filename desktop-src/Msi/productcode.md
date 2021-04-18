---
description: '[ProductCode] 屬性是特定產品版本的唯一識別碼，以字串 GUID 表示，例如 &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;。'
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: ProductCode 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976169"
---
# <a name="productcode-property"></a><span data-ttu-id="62eab-103">ProductCode 屬性</span><span class="sxs-lookup"><span data-stu-id="62eab-103">ProductCode property</span></span>

<span data-ttu-id="62eab-104">[ **ProductCode** ] 屬性是特定產品版本的唯一識別碼，以字串 [GUID](guid.md)表示，例如 " {12345678-1234-1234-1234-123456789012} "。</span><span class="sxs-lookup"><span data-stu-id="62eab-104">The **ProductCode** property is a unique identifier for the particular product release, represented as a string [GUID](guid.md), for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="62eab-105">此 GUID 中使用的字母必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="62eab-105">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="62eab-106">此識別碼必須因不同版本和語言而有所不同。</span><span class="sxs-lookup"><span data-stu-id="62eab-106">This ID must vary for different versions and languages.</span></span>

<span data-ttu-id="62eab-107">將產品更新為全新產品的產品升級，也必須變更產品代碼。</span><span class="sxs-lookup"><span data-stu-id="62eab-107">A product upgrade that updates a product into an entirely new product must also change the product code.</span></span> <span data-ttu-id="62eab-108">應用程式套件的32位和64位版本必須獲派不同的產品代碼。</span><span class="sxs-lookup"><span data-stu-id="62eab-108">The 32-bit and 64-bit versions of an application's package must be assigned different product codes.</span></span>

<span data-ttu-id="62eab-109">**ProductCode** 會公告為 product 屬性，而且是指定產品的主要方法。</span><span class="sxs-lookup"><span data-stu-id="62eab-109">The **ProductCode** is advertised as a product property, and is the primary method of specifying the product.</span></span> <span data-ttu-id="62eab-110">此為必要屬性。</span><span class="sxs-lookup"><span data-stu-id="62eab-110">This property is REQUIRED.</span></span>

## <a name="requirements"></a><span data-ttu-id="62eab-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="62eab-111">Requirements</span></span>



| <span data-ttu-id="62eab-112">需求</span><span class="sxs-lookup"><span data-stu-id="62eab-112">Requirement</span></span> | <span data-ttu-id="62eab-113">值</span><span class="sxs-lookup"><span data-stu-id="62eab-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62eab-114">版本</span><span class="sxs-lookup"><span data-stu-id="62eab-114">Version</span></span><br/> | <span data-ttu-id="62eab-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="62eab-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62eab-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="62eab-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62eab-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="62eab-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="62eab-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="62eab-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62eab-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62eab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62eab-120">屬性</span><span class="sxs-lookup"><span data-stu-id="62eab-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




