---
description: PatchFiles 屬性會傳回 StringList 物件，其中包含可由提供的修補程式清單更新的檔案清單。
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: PatchFiles 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981663"
---
# <a name="installerpatchfiles-property"></a><span data-ttu-id="e8f44-103">PatchFiles 屬性</span><span class="sxs-lookup"><span data-stu-id="e8f44-103">Installer.PatchFiles property</span></span>

<span data-ttu-id="e8f44-104">**PatchFiles** 屬性會傳回 [**StringList**](stringlist-object.md)物件，其中包含可由提供的修補程式清單更新的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="e8f44-104">The **PatchFiles** property returns a [**StringList**](stringlist-object.md) object that contains a list of files that can be updated by the provided list of patches.</span></span> <span data-ttu-id="e8f44-105">這個屬性會呼叫 [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)。</span><span class="sxs-lookup"><span data-stu-id="e8f44-105">This property calls [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="e8f44-106">如需使用 **PatchFiles** 屬性的詳細資訊，請參閱 [列出可更新的](listing-the-files-that-can-be-updated.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="e8f44-106">For more information about using the **PatchFiles** property see [Listing the Files that can be Updated](listing-the-files-that-can-be-updated.md).</span></span>

<span data-ttu-id="e8f44-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e8f44-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8f44-108">語法</span><span class="sxs-lookup"><span data-stu-id="e8f44-108">Syntax</span></span>


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a><span data-ttu-id="e8f44-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e8f44-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e8f44-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8f44-110">Requirements</span></span>



| <span data-ttu-id="e8f44-111">需求</span><span class="sxs-lookup"><span data-stu-id="e8f44-111">Requirement</span></span> | <span data-ttu-id="e8f44-112">值</span><span class="sxs-lookup"><span data-stu-id="e8f44-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f44-113">版本</span><span class="sxs-lookup"><span data-stu-id="e8f44-113">Version</span></span><br/> | <span data-ttu-id="e8f44-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e8f44-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e8f44-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e8f44-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e8f44-116">Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5</span><span class="sxs-lookup"><span data-stu-id="e8f44-116">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="e8f44-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e8f44-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="e8f44-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8f44-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="e8f44-119">IID</span><span class="sxs-lookup"><span data-stu-id="e8f44-119">IID</span></span><br/>     | <span data-ttu-id="e8f44-120">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e8f44-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="e8f44-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8f44-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f44-122">**安裝程式物件**</span><span class="sxs-lookup"><span data-stu-id="e8f44-122">**Installer Object**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="e8f44-123">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="e8f44-123">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




