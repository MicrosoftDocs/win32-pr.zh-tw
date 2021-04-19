---
description: 只有在每部電腦或目前使用者安裝產品時，才會設定已安裝的屬性。
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: 已安裝屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979451"
---
# <a name="installed-property"></a><span data-ttu-id="f836f-103">已安裝屬性</span><span class="sxs-lookup"><span data-stu-id="f836f-103">Installed property</span></span>

<span data-ttu-id="f836f-104">只有在每部電腦或目前使用者安裝產品時，才會設定 **已安裝** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="f836f-104">The **Installed** property is set only if the product is installed per-machine or for the current user.</span></span> <span data-ttu-id="f836f-105">如果已針對不同的使用者安裝產品，則不會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="f836f-105">This property is not set if the product is installed for a different user.</span></span>

<span data-ttu-id="f836f-106">[ **已安裝** ] 屬性可用於條件運算式中，以判斷是否已針對每部電腦或目前使用者安裝產品。</span><span class="sxs-lookup"><span data-stu-id="f836f-106">The **Installed** property can be used in conditional expressions to determine whether a product is installed per-computer or for the current user.</span></span> <span data-ttu-id="f836f-107">例如，您可以在順序資料表的條件式資料行中使用屬性，或區別第一個安裝和維護安裝。</span><span class="sxs-lookup"><span data-stu-id="f836f-107">For example, the property can be used in the conditional column of a sequence table or to differentiate between a first installation and a maintenance installation.</span></span>

<span data-ttu-id="f836f-108">若要判斷是否已針對不同的使用者安裝產品，請檢查 [**ProductState**](productstate.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f836f-108">To determine whether the product is installed for a different user, check the [**ProductState**](productstate.md) property.</span></span>

<span data-ttu-id="f836f-109">[**ProductVersion**](productversion.md)屬性的值是字串格式的產品版本。</span><span class="sxs-lookup"><span data-stu-id="f836f-109">The value of the [**ProductVersion**](productversion.md) property is the version of the product in string format.</span></span>

## <a name="requirements"></a><span data-ttu-id="f836f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="f836f-110">Requirements</span></span>



| <span data-ttu-id="f836f-111">需求</span><span class="sxs-lookup"><span data-stu-id="f836f-111">Requirement</span></span> | <span data-ttu-id="f836f-112">值</span><span class="sxs-lookup"><span data-stu-id="f836f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f836f-113">版本</span><span class="sxs-lookup"><span data-stu-id="f836f-113">Version</span></span><br/> | <span data-ttu-id="f836f-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="f836f-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f836f-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="f836f-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f836f-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="f836f-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f836f-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="f836f-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f836f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f836f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f836f-119">屬性</span><span class="sxs-lookup"><span data-stu-id="f836f-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




