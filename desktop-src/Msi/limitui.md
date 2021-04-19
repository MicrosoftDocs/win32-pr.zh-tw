---
description: 如果設定了 LIMITUI 屬性，則在安裝套件時所使用的使用者介面 (UI) 層級會限制為「基本」。
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: LIMITUI 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992800"
---
# <a name="limitui-property"></a><span data-ttu-id="d0801-103">LIMITUI 屬性</span><span class="sxs-lookup"><span data-stu-id="d0801-103">LIMITUI property</span></span>

<span data-ttu-id="d0801-104">如果設定了 **LIMITUI** 屬性，則在安裝套件時所使用的使用者介面 (UI) 層級會限制為「基本」。</span><span class="sxs-lookup"><span data-stu-id="d0801-104">If the **LIMITUI** property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span> <span data-ttu-id="d0801-105">如果封裝中沒有任何撰寫的 UI，但仍包含 [對話方塊資料表](dialog-table.md)之類的 ui 資料表，則此屬性是必要的。</span><span class="sxs-lookup"><span data-stu-id="d0801-105">This property is required in packages that have no authored UI but still contain UI tables such as the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="d0801-106">如需 UI 層級的說明，請參閱 [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span><span class="sxs-lookup"><span data-stu-id="d0801-106">For a description of UI levels, see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span></span>

## <a name="remarks"></a><span data-ttu-id="d0801-107">備註</span><span class="sxs-lookup"><span data-stu-id="d0801-107">Remarks</span></span>

<span data-ttu-id="d0801-108">包含 **LIMITUI** 屬性的安裝套件也必須包含 [**ARPNOMODIFY**](arpnomodify.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0801-108">Installation packages containing the **LIMITUI** property must also contain the [**ARPNOMODIFY**](arpnomodify.md) property.</span></span> <span data-ttu-id="d0801-109">當您嘗試設定產品時，使用者必須從 **主控台** 公用程式中的 [**新增或移除程式**] 取得正確的行為。</span><span class="sxs-lookup"><span data-stu-id="d0801-109">This is required for a user to obtain the correct behavior from the **Add or Remove Programs** in the **Control Panel** utility when attempting to configure a product.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0801-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0801-110">Requirements</span></span>



| <span data-ttu-id="d0801-111">需求</span><span class="sxs-lookup"><span data-stu-id="d0801-111">Requirement</span></span> | <span data-ttu-id="d0801-112">值</span><span class="sxs-lookup"><span data-stu-id="d0801-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0801-113">版本</span><span class="sxs-lookup"><span data-stu-id="d0801-113">Version</span></span><br/> | <span data-ttu-id="d0801-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d0801-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d0801-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d0801-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d0801-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d0801-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d0801-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="d0801-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0801-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0801-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0801-119">屬性</span><span class="sxs-lookup"><span data-stu-id="d0801-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d0801-120">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="d0801-120">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[<span data-ttu-id="d0801-121">**ARPNOMODIFY**</span><span class="sxs-lookup"><span data-stu-id="d0801-121">**ARPNOMODIFY**</span></span>](arpnomodify.md)
</dt> </dl>

 

 




