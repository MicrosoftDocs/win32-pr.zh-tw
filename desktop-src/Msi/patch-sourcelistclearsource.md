---
description: 移除網路或 URL 來源。
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: SourceListClearSource 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995220"
---
# <a name="patchsourcelistclearsource-method"></a><span data-ttu-id="5df20-103">SourceListClearSource 方法</span><span class="sxs-lookup"><span data-stu-id="5df20-103">Patch.SourceListClearSource method</span></span>

<span data-ttu-id="5df20-104">**SourceListClearSource** 方法會移除網路或 URL 來源。</span><span class="sxs-lookup"><span data-stu-id="5df20-104">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="5df20-105">這個方法會呼叫 [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)。</span><span class="sxs-lookup"><span data-stu-id="5df20-105">This method calls [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="5df20-106">語法</span><span class="sxs-lookup"><span data-stu-id="5df20-106">Syntax</span></span>


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="5df20-107">參數</span><span class="sxs-lookup"><span data-stu-id="5df20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df20-108">*型別*</span><span class="sxs-lookup"><span data-stu-id="5df20-108">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="5df20-109">要移除之來源的類型。</span><span class="sxs-lookup"><span data-stu-id="5df20-109">Type of source to be removed.</span></span>

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

<span data-ttu-id="5df20-110">**MSISOURCETYPE \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="5df20-110">**MSISOURCETYPE\_NETWORK**</span></span>
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

<span data-ttu-id="5df20-111">**MSISOURCETYPE \_ URL**</span><span class="sxs-lookup"><span data-stu-id="5df20-111">**MSISOURCETYPE\_URL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="5df20-112">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="5df20-112">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="5df20-113">要移除之來源的路徑。</span><span class="sxs-lookup"><span data-stu-id="5df20-113">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df20-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5df20-114">Return value</span></span>

<span data-ttu-id="5df20-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5df20-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df20-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5df20-116">Requirements</span></span>



| <span data-ttu-id="5df20-117">需求</span><span class="sxs-lookup"><span data-stu-id="5df20-117">Requirement</span></span> | <span data-ttu-id="5df20-118">值</span><span class="sxs-lookup"><span data-stu-id="5df20-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5df20-119">版本</span><span class="sxs-lookup"><span data-stu-id="5df20-119">Version</span></span><br/> | <span data-ttu-id="5df20-120">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5df20-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5df20-121">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5df20-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5df20-122">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5df20-122">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="5df20-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5df20-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5df20-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5df20-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="5df20-125">IID</span><span class="sxs-lookup"><span data-stu-id="5df20-125">IID</span></span><br/>     | <span data-ttu-id="5df20-126">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5df20-126">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="5df20-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5df20-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df20-128">**Patch**</span><span class="sxs-lookup"><span data-stu-id="5df20-128">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="5df20-129">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="5df20-129">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="5df20-130">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="5df20-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




