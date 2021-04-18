---
description: 設定此屬性就像設定 TransformsAtSource 原則原則一樣，不同之處在于範圍不同。
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: TRANSFORMSATSOURCE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996487"
---
# <a name="transformsatsource-property"></a><span data-ttu-id="6187f-103">TRANSFORMSATSOURCE 屬性</span><span class="sxs-lookup"><span data-stu-id="6187f-103">TRANSFORMSATSOURCE property</span></span>

<span data-ttu-id="6187f-104">設定此屬性就像設定 [TransformsAtSource 原則](transformsatsource-policy.md) 原則一樣，不同之處在于範圍不同。</span><span class="sxs-lookup"><span data-stu-id="6187f-104">Setting this property is like setting the [TransformsAtSource policy](transformsatsource-policy.md) policy except that the scope is different.</span></span> <span data-ttu-id="6187f-105">設定 TransformsAtSource 原則會套用至指定使用者所安裝的所有套件。</span><span class="sxs-lookup"><span data-stu-id="6187f-105">Setting TransformsAtSource policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="6187f-106">無論使用者是哪一種，設定 **TRANSFORMSATSOURCE** 屬性都會套用至套件。</span><span class="sxs-lookup"><span data-stu-id="6187f-106">Setting the **TRANSFORMSATSOURCE** property applies to the package regardless of the users.</span></span>

## <a name="remarks"></a><span data-ttu-id="6187f-107">備註</span><span class="sxs-lookup"><span data-stu-id="6187f-107">Remarks</span></span>

<span data-ttu-id="6187f-108">Windows Installer 會以 [**TRANSFORMSSECURE**](transformssecure.md)屬性的形式來解讀 **TRANSFORMSATSOURCE** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6187f-108">Windows Installer interprets the **TRANSFORMSATSOURCE** property as though it were the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="6187f-109">如果在 [**轉換**](transforms.md) 屬性中傳遞 @ 旗標，Windows Installer 會將清單中的轉換視為 [安全來源轉換](secure-at-source-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="6187f-109">If the @ flag is passed in the [**TRANSFORMS**](transforms.md) property, Windows Installer treats the transforms in the list as [secure-at-source transforms](secure-at-source-transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6187f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6187f-110">Requirements</span></span>



| <span data-ttu-id="6187f-111">需求</span><span class="sxs-lookup"><span data-stu-id="6187f-111">Requirement</span></span> | <span data-ttu-id="6187f-112">值</span><span class="sxs-lookup"><span data-stu-id="6187f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6187f-113">版本</span><span class="sxs-lookup"><span data-stu-id="6187f-113">Version</span></span><br/> | <span data-ttu-id="6187f-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="6187f-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6187f-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="6187f-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6187f-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="6187f-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6187f-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="6187f-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6187f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6187f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6187f-119">屬性</span><span class="sxs-lookup"><span data-stu-id="6187f-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




