---
description: VerifyDiskSpace 屬性是唯讀屬性。
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: VerifyDiskSpace 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991351"
---
# <a name="sessionverifydiskspace-property"></a><span data-ttu-id="e32bd-103">VerifyDiskSpace 屬性</span><span class="sxs-lookup"><span data-stu-id="e32bd-103">Session.VerifyDiskSpace property</span></span>

<span data-ttu-id="e32bd-104">**VerifyDiskSpace** 屬性是唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="e32bd-104">The **VerifyDiskSpace** property is a read-only property.</span></span> <span data-ttu-id="e32bd-105">如果有足夠的磁碟空間，則會傳回 true，如果磁片已滿，則會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="e32bd-105">It returns true if enough disk space exists and false if the disk is full.</span></span> <span data-ttu-id="e32bd-106">因為此屬性會使用由成本動作所收集的資訊，所以應該只在 [CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和 [CostFinalize 動作](costfinalize-action.md)之後呼叫 **VerifyDiskSpace** 。</span><span class="sxs-lookup"><span data-stu-id="e32bd-106">Because this property uses information gathered by the costing actions, **VerifyDiskSpace** should only be called after the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="e32bd-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e32bd-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32bd-108">語法</span><span class="sxs-lookup"><span data-stu-id="e32bd-108">Syntax</span></span>


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a><span data-ttu-id="e32bd-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e32bd-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e32bd-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e32bd-110">Requirements</span></span>



| <span data-ttu-id="e32bd-111">需求</span><span class="sxs-lookup"><span data-stu-id="e32bd-111">Requirement</span></span> | <span data-ttu-id="e32bd-112">值</span><span class="sxs-lookup"><span data-stu-id="e32bd-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e32bd-113">版本</span><span class="sxs-lookup"><span data-stu-id="e32bd-113">Version</span></span><br/> | <span data-ttu-id="e32bd-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e32bd-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e32bd-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e32bd-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e32bd-116">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e32bd-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e32bd-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e32bd-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="e32bd-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e32bd-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e32bd-119">IID</span><span class="sxs-lookup"><span data-stu-id="e32bd-119">IID</span></span><br/>     | <span data-ttu-id="e32bd-120">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e32bd-120">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




