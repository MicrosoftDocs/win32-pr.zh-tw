---
description: Session 物件的 ComponentCosts 屬性會傳回 RecordList 物件，以列舉安裝元件所需的每個磁片磁碟機的磁碟空間。
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: ComponentCosts 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982600"
---
# <a name="sessioncomponentcosts-property"></a><span data-ttu-id="5aadf-103">ComponentCosts 屬性</span><span class="sxs-lookup"><span data-stu-id="5aadf-103">Session.ComponentCosts property</span></span>

<span data-ttu-id="5aadf-104">[**Session**](session-object.md)物件的 ComponentCosts 屬性會傳回 [**RecordList**](recordlist-object.md)物件，以列舉安裝元件所需的每個磁片磁碟機的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="5aadf-104">The ComponentCosts property of the [**Session**](session-object.md) object returns a [**RecordList**](recordlist-object.md) object enumerating the disk space per drive required to install a component.</span></span> <span data-ttu-id="5aadf-105">使用者介面會使用這項資訊來顯示所有磁片磁碟機所需的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="5aadf-105">This information is used by the user interface to display the disk space required for all drives.</span></span> <span data-ttu-id="5aadf-106">傳回的磁碟空間成本是512個位元組的倍數。</span><span class="sxs-lookup"><span data-stu-id="5aadf-106">The returned disk space costs are in multiples of 512 bytes.</span></span>

<span data-ttu-id="5aadf-107">ComponentCosts 屬性只應在安裝程式完成檔案 [成本](file-costing.md) 及 [CostFinalize 動作](costfinalize-action.md)之後使用。</span><span class="sxs-lookup"><span data-stu-id="5aadf-107">The ComponentCosts property should only be used after the installer has completed [file costing](file-costing.md) and after the [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="5aadf-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5aadf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aadf-109">語法</span><span class="sxs-lookup"><span data-stu-id="5aadf-109">Syntax</span></span>


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a><span data-ttu-id="5aadf-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5aadf-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5aadf-111">備註</span><span class="sxs-lookup"><span data-stu-id="5aadf-111">Remarks</span></span>

<span data-ttu-id="5aadf-112">若要取得總成本，請新增所有元件的成本加上安裝程式引擎成本 (Component = "" ) 。</span><span class="sxs-lookup"><span data-stu-id="5aadf-112">To obtain the total cost, add the costs for all components plus the installer engine cost (Component = "").</span></span>

<span data-ttu-id="5aadf-113">ComponentCosts 會傳回 [**RecordList 物件**](recordlist-object.md)。</span><span class="sxs-lookup"><span data-stu-id="5aadf-113">ComponentCosts returns a [**RecordList object**](recordlist-object.md).</span></span> <span data-ttu-id="5aadf-114">傳回之 RecordList 物件中的每一筆記錄都有下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="5aadf-114">Each record in the returned RecordList object has the following fields:</span></span>



| <span data-ttu-id="5aadf-115">欄位</span><span class="sxs-lookup"><span data-stu-id="5aadf-115">Field</span></span> | <span data-ttu-id="5aadf-116">描述</span><span class="sxs-lookup"><span data-stu-id="5aadf-116">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="5aadf-117">1</span><span class="sxs-lookup"><span data-stu-id="5aadf-117">1</span></span>     | <span data-ttu-id="5aadf-118">磁片區/磁片磁碟機名稱</span><span class="sxs-lookup"><span data-stu-id="5aadf-118">Volume/Drive name</span></span>                                    |
| <span data-ttu-id="5aadf-119">2</span><span class="sxs-lookup"><span data-stu-id="5aadf-119">2</span></span>     | <span data-ttu-id="5aadf-120">最終磁碟空間的成本為512個位元組的倍數。</span><span class="sxs-lookup"><span data-stu-id="5aadf-120">Final disk space cost in multiples of 512 bytes.</span></span>     |
| <span data-ttu-id="5aadf-121">3</span><span class="sxs-lookup"><span data-stu-id="5aadf-121">3</span></span>     | <span data-ttu-id="5aadf-122">暫存磁碟空間的成本為512個位元組的倍數。</span><span class="sxs-lookup"><span data-stu-id="5aadf-122">Temporary disk space cost in multiples of 512 bytes.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5aadf-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5aadf-123">Requirements</span></span>



| <span data-ttu-id="5aadf-124">需求</span><span class="sxs-lookup"><span data-stu-id="5aadf-124">Requirement</span></span> | <span data-ttu-id="5aadf-125">值</span><span class="sxs-lookup"><span data-stu-id="5aadf-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aadf-126">版本</span><span class="sxs-lookup"><span data-stu-id="5aadf-126">Version</span></span><br/> | <span data-ttu-id="5aadf-127">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5aadf-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5aadf-128">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5aadf-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5aadf-129">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5aadf-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5aadf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5aadf-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="5aadf-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aadf-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5aadf-132">IID</span><span class="sxs-lookup"><span data-stu-id="5aadf-132">IID</span></span><br/>     | <span data-ttu-id="5aadf-133">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5aadf-133">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




