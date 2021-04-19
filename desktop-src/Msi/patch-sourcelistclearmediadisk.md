---
description: Patch 物件的 SourceListClearMediaDisk 方法會從已註冊的磁片集合移除指定的磁片以進行修補。 接受 Diskid 做為參數。 這個方法會呼叫 MsiSourceListClearMediaDisk。
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: SourceListClearMediaDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995221"
---
# <a name="patchsourcelistclearmediadisk-method"></a><span data-ttu-id="1d71e-105">SourceListClearMediaDisk 方法</span><span class="sxs-lookup"><span data-stu-id="1d71e-105">Patch.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="1d71e-106">[**Patch**](patch-object.md)物件的 **SourceListClearMediaDisk** 方法會從已註冊的磁片集合移除指定的磁片以進行修補。</span><span class="sxs-lookup"><span data-stu-id="1d71e-106">The **SourceListClearMediaDisk** method of the [**Patch**](patch-object.md) object removes a specified disk from the set of registered disks for a patch.</span></span> <span data-ttu-id="1d71e-107">接受 *Diskid* 做為參數。</span><span class="sxs-lookup"><span data-stu-id="1d71e-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="1d71e-108">這個方法會呼叫 [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)。</span><span class="sxs-lookup"><span data-stu-id="1d71e-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d71e-109">語法</span><span class="sxs-lookup"><span data-stu-id="1d71e-109">Syntax</span></span>


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="1d71e-110">參數</span><span class="sxs-lookup"><span data-stu-id="1d71e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d71e-111">*Diskid*</span><span class="sxs-lookup"><span data-stu-id="1d71e-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="1d71e-112">此參數提供要移除之磁片的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d71e-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d71e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d71e-113">Return value</span></span>

<span data-ttu-id="1d71e-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1d71e-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d71e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d71e-115">Requirements</span></span>



| <span data-ttu-id="1d71e-116">需求</span><span class="sxs-lookup"><span data-stu-id="1d71e-116">Requirement</span></span> | <span data-ttu-id="1d71e-117">值</span><span class="sxs-lookup"><span data-stu-id="1d71e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d71e-118">版本</span><span class="sxs-lookup"><span data-stu-id="1d71e-118">Version</span></span><br/> | <span data-ttu-id="1d71e-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="1d71e-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1d71e-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="1d71e-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1d71e-121">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1d71e-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="1d71e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1d71e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="1d71e-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d71e-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="1d71e-124">IID</span><span class="sxs-lookup"><span data-stu-id="1d71e-124">IID</span></span><br/>     | <span data-ttu-id="1d71e-125">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1d71e-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="1d71e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d71e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d71e-127">**Patch**</span><span class="sxs-lookup"><span data-stu-id="1d71e-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="1d71e-128">**MsiSourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="1d71e-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="1d71e-129">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="1d71e-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




