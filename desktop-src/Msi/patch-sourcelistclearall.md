---
description: Patch 物件的 SourceListClearAll 方法會清除所指定類型之所有來源的完整來源清單，以取得修補程式。 接受型別做為參數。 這個方法會呼叫 MsiSourceListClearAllEx。
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: SourceListClearAll 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000861"
---
# <a name="patchsourcelistclearall-method"></a><span data-ttu-id="03f09-105">SourceListClearAll 方法</span><span class="sxs-lookup"><span data-stu-id="03f09-105">Patch.SourceListClearAll method</span></span>

<span data-ttu-id="03f09-106">[**Patch**](patch-object.md)物件的 **SourceListClearAll** 方法會清除所指定類型之所有來源的完整來源清單，以取得修補程式。</span><span class="sxs-lookup"><span data-stu-id="03f09-106">The **SourceListClearAll** method of the [**Patch**](patch-object.md) object clears the complete source list of all sources of the specified type for a patch.</span></span> <span data-ttu-id="03f09-107">接受 *型* 別做為參數。</span><span class="sxs-lookup"><span data-stu-id="03f09-107">Accepts *Type* as a parameter.</span></span> <span data-ttu-id="03f09-108">這個方法會呼叫 [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)。</span><span class="sxs-lookup"><span data-stu-id="03f09-108">This method calls [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="03f09-109">語法</span><span class="sxs-lookup"><span data-stu-id="03f09-109">Syntax</span></span>


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="03f09-110">參數</span><span class="sxs-lookup"><span data-stu-id="03f09-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f09-111">*型別*</span><span class="sxs-lookup"><span data-stu-id="03f09-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="03f09-112">來源類型的類型（例如網路、URL 或媒體）。</span><span class="sxs-lookup"><span data-stu-id="03f09-112">The type of source type, such as network, URL or media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03f09-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="03f09-113">Return value</span></span>

<span data-ttu-id="03f09-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="03f09-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f09-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="03f09-115">Requirements</span></span>



| <span data-ttu-id="03f09-116">需求</span><span class="sxs-lookup"><span data-stu-id="03f09-116">Requirement</span></span> | <span data-ttu-id="03f09-117">值</span><span class="sxs-lookup"><span data-stu-id="03f09-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03f09-118">版本</span><span class="sxs-lookup"><span data-stu-id="03f09-118">Version</span></span><br/> | <span data-ttu-id="03f09-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="03f09-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="03f09-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="03f09-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="03f09-121">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="03f09-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="03f09-122">DLL</span><span class="sxs-lookup"><span data-stu-id="03f09-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="03f09-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f09-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="03f09-124">IID</span><span class="sxs-lookup"><span data-stu-id="03f09-124">IID</span></span><br/>     | <span data-ttu-id="03f09-125">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="03f09-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="03f09-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03f09-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f09-127">**Patch**</span><span class="sxs-lookup"><span data-stu-id="03f09-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="03f09-128">**MsiSourceListClearAllEx**</span><span class="sxs-lookup"><span data-stu-id="03f09-128">**MsiSourceListClearAllEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[<span data-ttu-id="03f09-129">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="03f09-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




