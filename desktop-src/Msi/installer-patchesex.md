---
description: PatchesEx 屬性會傳回 RecordList 物件，以列舉修補程式的清單。
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: PatchesEx 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975976"
---
# <a name="installerpatchesex-property"></a><span data-ttu-id="cfb38-103">PatchesEx 屬性</span><span class="sxs-lookup"><span data-stu-id="cfb38-103">Installer.PatchesEx property</span></span>

<span data-ttu-id="cfb38-104">**PatchesEx** 屬性會傳回 [**RecordList**](recordlist-object.md)物件，以列舉修補程式的清單。</span><span class="sxs-lookup"><span data-stu-id="cfb38-104">The **PatchesEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of patches.</span></span> <span data-ttu-id="cfb38-105">這個屬性會呼叫 [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)。</span><span class="sxs-lookup"><span data-stu-id="cfb38-105">This property calls [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span>

<span data-ttu-id="cfb38-106">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="cfb38-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb38-107">語法</span><span class="sxs-lookup"><span data-stu-id="cfb38-107">Syntax</span></span>


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a><span data-ttu-id="cfb38-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="cfb38-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb38-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfb38-109">Requirements</span></span>



| <span data-ttu-id="cfb38-110">需求</span><span class="sxs-lookup"><span data-stu-id="cfb38-110">Requirement</span></span> | <span data-ttu-id="cfb38-111">值</span><span class="sxs-lookup"><span data-stu-id="cfb38-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb38-112">版本</span><span class="sxs-lookup"><span data-stu-id="cfb38-112">Version</span></span><br/> | <span data-ttu-id="cfb38-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="cfb38-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cfb38-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="cfb38-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cfb38-115">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="cfb38-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="cfb38-116">DLL</span><span class="sxs-lookup"><span data-stu-id="cfb38-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="cfb38-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfb38-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="cfb38-118">IID</span><span class="sxs-lookup"><span data-stu-id="cfb38-118">IID</span></span><br/>     | <span data-ttu-id="cfb38-119">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cfb38-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="cfb38-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfb38-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb38-121">**安裝程式**</span><span class="sxs-lookup"><span data-stu-id="cfb38-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="cfb38-122">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="cfb38-122">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="cfb38-123">**Patch**</span><span class="sxs-lookup"><span data-stu-id="cfb38-123">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="cfb38-124">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="cfb38-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




