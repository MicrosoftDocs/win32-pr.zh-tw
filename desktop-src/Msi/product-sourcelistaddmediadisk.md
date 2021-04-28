---
description: SourceListAddMediaDisk 方法-SourceListAddMediaDisk 方法會將磁片新增至已註冊的磁片組。 接受 Diskid、VolumeLabel 和 DiskPrompt 做為參數。 這個方法會在 MsiSourceListAddMediaDisk 上呼叫。
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: SourceListAddMediaDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4cf5fac906b048930b47a07acb2c04c7243d5bbf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113576"
---
# <a name="productsourcelistaddmediadisk-method"></a><span data-ttu-id="fb342-105">SourceListAddMediaDisk 方法</span><span class="sxs-lookup"><span data-stu-id="fb342-105">Product.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="fb342-106">**SourceListAddMediaDisk** 方法會將磁片新增至已註冊的磁片集。</span><span class="sxs-lookup"><span data-stu-id="fb342-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="fb342-107">接受 *Diskid*、 *VolumeLabel* 和 *DiskPrompt* 做為參數。</span><span class="sxs-lookup"><span data-stu-id="fb342-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="fb342-108">這個方法會在 [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)上呼叫。</span><span class="sxs-lookup"><span data-stu-id="fb342-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb342-109">語法</span><span class="sxs-lookup"><span data-stu-id="fb342-109">Syntax</span></span>


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="fb342-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb342-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb342-111">*Diskid*</span><span class="sxs-lookup"><span data-stu-id="fb342-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="fb342-112">此參數提供要新增或更新之磁片的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb342-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="fb342-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="fb342-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="fb342-114">此參數提供要新增或更新之磁片的標籤。</span><span class="sxs-lookup"><span data-stu-id="fb342-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="fb342-115">更新會覆寫登錄中的現有磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="fb342-115">An update overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="fb342-116">若只要變更磁片提示，請取得現有的已註冊磁片區標籤，並將它與新的磁片提示一起提供。</span><span class="sxs-lookup"><span data-stu-id="fb342-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="fb342-117">此參數的空字串會將空字串（長度 (0 位元組）註冊為磁片區標籤) 。</span><span class="sxs-lookup"><span data-stu-id="fb342-117">An empty string for this parameter registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="fb342-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="fb342-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="fb342-119">此參數會提供要新增或更新之磁片的磁片提示。</span><span class="sxs-lookup"><span data-stu-id="fb342-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="fb342-120">更新會覆寫登錄中的現有磁片提示。</span><span class="sxs-lookup"><span data-stu-id="fb342-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="fb342-121">若只要變更磁片區標籤，請從登錄中取得現有的磁片提示，並提供新的磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="fb342-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="fb342-122">此參數的空字串會將空字串（長度 (0 位元組）註冊為磁片提示字元) 。</span><span class="sxs-lookup"><span data-stu-id="fb342-122">An empty string for this parameter registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb342-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb342-123">Return value</span></span>

<span data-ttu-id="fb342-124">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fb342-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb342-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb342-125">Requirements</span></span>



| <span data-ttu-id="fb342-126">需求</span><span class="sxs-lookup"><span data-stu-id="fb342-126">Requirement</span></span> | <span data-ttu-id="fb342-127">值</span><span class="sxs-lookup"><span data-stu-id="fb342-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb342-128">版本</span><span class="sxs-lookup"><span data-stu-id="fb342-128">Version</span></span><br/> | <span data-ttu-id="fb342-129">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="fb342-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fb342-130">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="fb342-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fb342-131">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fb342-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="fb342-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fb342-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb342-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb342-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="fb342-134">IID</span><span class="sxs-lookup"><span data-stu-id="fb342-134">IID</span></span><br/>     | <span data-ttu-id="fb342-135">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fb342-135">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="fb342-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb342-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb342-137">**產品**</span><span class="sxs-lookup"><span data-stu-id="fb342-137">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="fb342-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="fb342-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="fb342-139">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="fb342-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




