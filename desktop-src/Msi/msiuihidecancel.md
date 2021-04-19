---
description: 這個 Windows Installer 屬性工作表示內部使用者介面層級已設定為隱藏 [取消] 按鈕。
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: MsiUIHideCancel 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001922"
---
# <a name="msiuihidecancel-property"></a><span data-ttu-id="9ead2-103">MsiUIHideCancel 屬性</span><span class="sxs-lookup"><span data-stu-id="9ead2-103">MsiUIHideCancel property</span></span>

<span data-ttu-id="9ead2-104">當內部使用者介面層級已設定為包含 \_ 具有 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)函數的 INSTALLUILEVEL HIDECANCEL 或 [**安裝程式**](installer-object.md)物件的 [UILevel](installer-uilevel.md)屬性，或使用 [命令列選項](command-line-options.md)時，安裝程式會將 MsiUIHideCancel 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="9ead2-104">The installer sets the **MsiUIHideCancel** property to 1 when the internal user interface level has been set to include INSTALLUILEVEL\_HIDECANCEL with the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function or the [UILevel](installer-uilevel.md)property of the [**Installer**](installer-object.md) object or by using [Command Line Options](command-line-options.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ead2-105">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ead2-105">Requirements</span></span>



| <span data-ttu-id="9ead2-106">需求</span><span class="sxs-lookup"><span data-stu-id="9ead2-106">Requirement</span></span> | <span data-ttu-id="9ead2-107">值</span><span class="sxs-lookup"><span data-stu-id="9ead2-107">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ead2-108">版本</span><span class="sxs-lookup"><span data-stu-id="9ead2-108">Version</span></span><br/> | <span data-ttu-id="9ead2-109">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9ead2-109">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9ead2-110">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9ead2-110">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9ead2-111">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9ead2-111">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9ead2-112">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="9ead2-112">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ead2-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ead2-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ead2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="9ead2-114">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9ead2-115">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="9ead2-115">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




