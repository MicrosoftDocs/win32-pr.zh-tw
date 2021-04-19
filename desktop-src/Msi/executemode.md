---
description: EXECUTEMODE 屬性會指定安裝程式執行系統更新的方式。
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: EXECUTEMODE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987987"
---
# <a name="executemode-property"></a><span data-ttu-id="2f030-103">EXECUTEMODE 屬性</span><span class="sxs-lookup"><span data-stu-id="2f030-103">EXECUTEMODE property</span></span>

<span data-ttu-id="2f030-104">**EXECUTEMODE** 屬性會指定安裝程式執行系統更新的方式。</span><span class="sxs-lookup"><span data-stu-id="2f030-104">The **EXECUTEMODE** property specifies how the installer executes system updates.</span></span> <span data-ttu-id="2f030-105">當需要執行安裝而不實際變更系統時，這個屬性可能很有用。</span><span class="sxs-lookup"><span data-stu-id="2f030-105">This property may be useful when it is necessary to run an installation without actually changing the system.</span></span> <span data-ttu-id="2f030-106">屬性可以設定為 [無] 以停用更新作業，例如安裝檔案和登錄值。</span><span class="sxs-lookup"><span data-stu-id="2f030-106">The property can be set to None to disable updating operations such as the installation of files and registry values.</span></span>

<span data-ttu-id="2f030-107">這個屬性可以是下列兩個值的其中之一。</span><span class="sxs-lookup"><span data-stu-id="2f030-107">This property can have one of the following two values.</span></span> <span data-ttu-id="2f030-108">安裝程式只會檢查值的第一個字母，並不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2f030-108">The installer only examines the first letter of the value and is case insensitive.</span></span>

<dl> <dt>

<span data-ttu-id="2f030-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>沒有</span><span class="sxs-lookup"><span data-stu-id="2f030-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span>
</dt> <dd>

<span data-ttu-id="2f030-110">系統不會進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="2f030-110">No changes are made to the system.</span></span> <span data-ttu-id="2f030-111">安裝程式會執行使用者介面，然後查詢資料庫。</span><span class="sxs-lookup"><span data-stu-id="2f030-111">The installer runs the user interface and then queries the database.</span></span>

</dd> <dt>

<span data-ttu-id="2f030-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>腳本</span><span class="sxs-lookup"><span data-stu-id="2f030-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script</span></span>
</dt> <dd>

<span data-ttu-id="2f030-113">系統會透過腳本執行來進行所有變更。</span><span class="sxs-lookup"><span data-stu-id="2f030-113">All changes to the system are made through script execution.</span></span> <span data-ttu-id="2f030-114">這是預設模式。</span><span class="sxs-lookup"><span data-stu-id="2f030-114">This is the default mode.</span></span>

</dd> </dl>

## <a name="default-value"></a><span data-ttu-id="2f030-115">預設值</span><span class="sxs-lookup"><span data-stu-id="2f030-115">Default Value</span></span>

<span data-ttu-id="2f030-116">如果未定義此屬性，執行模式會預設為腳本。</span><span class="sxs-lookup"><span data-stu-id="2f030-116">If this property is not defined, the execution mode defaults to Script.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f030-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f030-117">Requirements</span></span>



| <span data-ttu-id="2f030-118">需求</span><span class="sxs-lookup"><span data-stu-id="2f030-118">Requirement</span></span> | <span data-ttu-id="2f030-119">值</span><span class="sxs-lookup"><span data-stu-id="2f030-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f030-120">版本</span><span class="sxs-lookup"><span data-stu-id="2f030-120">Version</span></span><br/> | <span data-ttu-id="2f030-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="2f030-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2f030-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="2f030-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2f030-123">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="2f030-123">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2f030-124">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="2f030-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f030-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f030-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f030-126">屬性</span><span class="sxs-lookup"><span data-stu-id="2f030-126">Properties</span></span>](properties.md)
</dt> </dl>

 

 




