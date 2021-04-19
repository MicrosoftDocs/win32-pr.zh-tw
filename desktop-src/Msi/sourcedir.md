---
description: SourceDir 屬性是包含來源封包檔的根目錄，或是安裝套件的來源檔案樹狀目錄。 此值用於目錄解析。
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: SourceDir 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001186"
---
# <a name="sourcedir-property"></a><span data-ttu-id="c16fc-104">SourceDir 屬性</span><span class="sxs-lookup"><span data-stu-id="c16fc-104">SourceDir property</span></span>

<span data-ttu-id="c16fc-105">**SourceDir** 屬性是包含來源封包檔的根目錄，或是安裝套件的來源檔案樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="c16fc-105">The **SourceDir** property is the root directory that contains the source cabinet file or the source file tree of the installation package.</span></span> <span data-ttu-id="c16fc-106">此值用於目錄解析。</span><span class="sxs-lookup"><span data-stu-id="c16fc-106">This value is used for directory resolution.</span></span>

## <a name="default-value"></a><span data-ttu-id="c16fc-107">預設值</span><span class="sxs-lookup"><span data-stu-id="c16fc-107">Default Value</span></span>

<span data-ttu-id="c16fc-108">包含安裝套件的目錄。</span><span class="sxs-lookup"><span data-stu-id="c16fc-108">The directory that contains the installation package.</span></span>

## <a name="remarks"></a><span data-ttu-id="c16fc-109">備註</span><span class="sxs-lookup"><span data-stu-id="c16fc-109">Remarks</span></span>

<span data-ttu-id="c16fc-110">在任何運算式中使用 **SourceDir** 屬性，或嘗試使用 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)取得 **SourceDir** 的值之前，必須先呼叫 [ResolveSource 動作](resolvesource-action.md)。</span><span class="sxs-lookup"><span data-stu-id="c16fc-110">The [ResolveSource action](resolvesource-action.md) must be called before using the **SourceDir** property in any expression or attempting to retrieve the value of **SourceDir** with [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="c16fc-111">無法在來源無法使用時執行 ResolveSource 動作，例如在卸載應用程式時，因為這可能會導致來源媒體出現非預期的提示。</span><span class="sxs-lookup"><span data-stu-id="c16fc-111">The ResolveSource action should not be run while the source is unavailable, such as when uninstalling an application, because this can cause an unintended prompt for the source media.</span></span>

## <a name="requirements"></a><span data-ttu-id="c16fc-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c16fc-112">Requirements</span></span>



| <span data-ttu-id="c16fc-113">需求</span><span class="sxs-lookup"><span data-stu-id="c16fc-113">Requirement</span></span> | <span data-ttu-id="c16fc-114">值</span><span class="sxs-lookup"><span data-stu-id="c16fc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c16fc-115">版本</span><span class="sxs-lookup"><span data-stu-id="c16fc-115">Version</span></span><br/> | <span data-ttu-id="c16fc-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c16fc-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c16fc-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c16fc-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c16fc-118">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="c16fc-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c16fc-119">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="c16fc-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c16fc-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c16fc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c16fc-121">屬性</span><span class="sxs-lookup"><span data-stu-id="c16fc-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




