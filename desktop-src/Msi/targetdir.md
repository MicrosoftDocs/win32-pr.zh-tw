---
description: TARGETDIR 屬性會指定安裝的根目的地目錄。
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990689"
---
# <a name="targetdir-property"></a><span data-ttu-id="6763f-103">TARGETDIR 屬性</span><span class="sxs-lookup"><span data-stu-id="6763f-103">TARGETDIR property</span></span>

<span data-ttu-id="6763f-104">**TARGETDIR** 屬性會指定安裝的根目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="6763f-104">The **TARGETDIR** property specifies the root destination directory for the installation.</span></span> <span data-ttu-id="6763f-105">**TARGETDIR** 必須是 [目錄](directory-table.md) 資料表中一個根目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="6763f-105">**TARGETDIR** must be the name of one root in the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="6763f-106">可能只有一個根目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="6763f-106">There may be only a single root destination directory.</span></span> <span data-ttu-id="6763f-107">在 [系統管理安裝](administrative-installation.md) 期間，此屬性會指定要複製安裝套件的位置。</span><span class="sxs-lookup"><span data-stu-id="6763f-107">During an [administrative installation](administrative-installation.md) this property specifies the location to copy the installation package.</span></span> <span data-ttu-id="6763f-108">在非系統管理安裝期間，此屬性會指定根目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="6763f-108">During a non-administrative installation this property specifies the root destination directory.</span></span>

<span data-ttu-id="6763f-109">若要指定根目的地目錄，請將目錄資料表的 [目錄] 資料行設定為 [ **TARGETDIR** ] 屬性，並將 [DefaultDir] 資料行設定為 [ [**SourceDir**](sourcedir.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="6763f-109">To specify the root destination directory, set the Directory column of the Directory table to the **TARGETDIR** property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="6763f-110">如果定義了 **TARGETDIR** 屬性，則會將目的地目錄解析為屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6763f-110">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="6763f-111">如果未定義 **TARGETDIR** 屬性，則會使用 [**ROOTDRIVE**](rootdrive.md) 屬性來解析路徑。</span><span class="sxs-lookup"><span data-stu-id="6763f-111">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span> <span data-ttu-id="6763f-112">如需使用 **TARGETDIR** 屬性的詳細資訊，請參閱 [使用目錄資料表](using-the-directory-table.md)。</span><span class="sxs-lookup"><span data-stu-id="6763f-112">For more information about using the **TARGETDIR** property, see [Using the Directory Table](using-the-directory-table.md).</span></span>

<span data-ttu-id="6763f-113">請注意， **TARGETDIR** 屬性的值通常是在命令列或透過使用者介面設定。</span><span class="sxs-lookup"><span data-stu-id="6763f-113">Note that the value of the **TARGETDIR** property is typically set at the command line or through a user interface.</span></span> <span data-ttu-id="6763f-114">由於本機磁片磁碟機的設定不同，因此不建議在 [屬性工作表](property-table.md)中撰寫路徑來設定 **TARGETDIR** 。</span><span class="sxs-lookup"><span data-stu-id="6763f-114">Setting **TARGETDIR** by authoring a path into the [Property table](property-table.md) is not recommended because computers differ in the set up of the local drive.</span></span>

<span data-ttu-id="6763f-115">如需如何在安裝期間變更 TARGETDIR 的詳細資訊，請參閱 [變更目錄的目標位置。](changing-the-target-location-for-a-directory.md)</span><span class="sxs-lookup"><span data-stu-id="6763f-115">For more information on how to change TARGETDIR during an installation see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="6763f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6763f-116">Requirements</span></span>



| <span data-ttu-id="6763f-117">需求</span><span class="sxs-lookup"><span data-stu-id="6763f-117">Requirement</span></span> | <span data-ttu-id="6763f-118">值</span><span class="sxs-lookup"><span data-stu-id="6763f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6763f-119">版本</span><span class="sxs-lookup"><span data-stu-id="6763f-119">Version</span></span><br/> | <span data-ttu-id="6763f-120">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="6763f-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6763f-121">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="6763f-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6763f-122">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="6763f-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6763f-123">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="6763f-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6763f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6763f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6763f-125">屬性</span><span class="sxs-lookup"><span data-stu-id="6763f-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




