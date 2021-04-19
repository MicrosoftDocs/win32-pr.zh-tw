---
description: SOURCELIST 屬性是應用程式安裝套件的網路或 URL 來源路徑清單（以分號分隔）。
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SOURCELIST 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977599"
---
# <a name="sourcelist-property"></a><span data-ttu-id="5ebc4-103">SOURCELIST 屬性</span><span class="sxs-lookup"><span data-stu-id="5ebc4-103">SOURCELIST property</span></span>

<span data-ttu-id="5ebc4-104">**SOURCELIST** 屬性是應用程式安裝套件的網路或 URL 來源路徑清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-104">The **SOURCELIST** property is a semicolon-delimited list of network or URL source paths to the application's installation package.</span></span> <span data-ttu-id="5ebc4-105">這份清單會附加到應用程式的每個使用者現有來源清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-105">This list is appended to the end of each user's existing source list for the application.</span></span> <span data-ttu-id="5ebc4-106">安裝程式會藉由列舉來源路徑清單來找出來源，並使用它所找到的第一個可存取位置。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-106">The installer locates a source by enumerating the list of source paths and uses the first accessible location it finds.</span></span> <span data-ttu-id="5ebc4-107">只有此來源可用於安裝的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-107">Only this source can be used for the remainder of the installation.</span></span> <span data-ttu-id="5ebc4-108">因此，來源清單中指定的每個路徑都必須是具有應用程式完整來源的位置。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-108">Each path specified in the source list must therefore be to a location having a complete source for the application.</span></span> <span data-ttu-id="5ebc4-109">每個來源位置的整個目錄樹狀結構必須相同，而且必須包含所有必要的來源檔案，包括任何封包。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-109">The entire directory tree at each source location must be the same and must include all of the required source files, including any cabinets.</span></span> <span data-ttu-id="5ebc4-110">每個位置都必須有一個具有相同檔案名和產品代碼的 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-110">Each location must have an .msi file with the same file name and product code.</span></span>

## <a name="default-value"></a><span data-ttu-id="5ebc4-111">預設值</span><span class="sxs-lookup"><span data-stu-id="5ebc4-111">Default Value</span></span>

<span data-ttu-id="5ebc4-112">如果產品尚未公告或安裝，則安裝程式只會檢查 **SOURCELIST** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-112">The installer only checks the **SOURCELIST** property if the product has not already been advertised or installed.</span></span> <span data-ttu-id="5ebc4-113">在所有其他情況下，安裝程式會使用登錄中的現有來源清單。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-113">In all other cases the installer uses the existing source list that is in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ebc4-114">備註</span><span class="sxs-lookup"><span data-stu-id="5ebc4-114">Remarks</span></span>

<span data-ttu-id="5ebc4-115">使用 **SOURCELIST** 屬性加入的來源會直接加入至每個來源類型的清單結尾，而且一律會在 [**SourceDir**](sourcedir.md) 屬性指定的預設來源之後。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-115">Sources added using the **SOURCELIST** property are added directly to the end of the list for each type of source and always come after the default source specified by the [**SourceDir**](sourcedir.md) property.</span></span>

<span data-ttu-id="5ebc4-116">針對 Windows Installer **SOURCELIST** 屬性中的來源數目是無限制的。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-116">For Windows Installer the number of sources in the **SOURCELIST** property is unlimited.</span></span> <span data-ttu-id="5ebc4-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) 可以用來新增網路來源。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) can be used to add network sources.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ebc4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ebc4-118">Requirements</span></span>



| <span data-ttu-id="5ebc4-119">需求</span><span class="sxs-lookup"><span data-stu-id="5ebc4-119">Requirement</span></span> | <span data-ttu-id="5ebc4-120">值</span><span class="sxs-lookup"><span data-stu-id="5ebc4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebc4-121">版本</span><span class="sxs-lookup"><span data-stu-id="5ebc4-121">Version</span></span><br/> | <span data-ttu-id="5ebc4-122">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5ebc4-123">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5ebc4-124">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5ebc4-125">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ebc4-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ebc4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ebc4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebc4-127">屬性</span><span class="sxs-lookup"><span data-stu-id="5ebc4-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5ebc4-128">來源復原</span><span class="sxs-lookup"><span data-stu-id="5ebc4-128">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




