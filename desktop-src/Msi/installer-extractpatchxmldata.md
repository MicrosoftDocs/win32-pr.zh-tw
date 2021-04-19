---
description: 安裝程式物件的 ExtractPatchXMLData 方法會將修補程式的資訊以 XML 字串的形式解壓縮。 此資訊可以用來判斷修補程式是否適用于目標系統。 這個方法會呼叫 MsiExtractPatchXMLData。
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: ExtractPatchXMLData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985962"
---
# <a name="installerextractpatchxmldata-method"></a><span data-ttu-id="4c97d-105">ExtractPatchXMLData 方法</span><span class="sxs-lookup"><span data-stu-id="4c97d-105">Installer.ExtractPatchXMLData method</span></span>

<span data-ttu-id="4c97d-106">[**安裝程式**](installer-object.md)物件的 **ExtractPatchXMLData** 方法會將修補程式的資訊以 XML 字串的形式解壓縮。</span><span class="sxs-lookup"><span data-stu-id="4c97d-106">The **ExtractPatchXMLData** method of the [**Installer**](installer-object.md) object extracts information from a patch as an XML string.</span></span> <span data-ttu-id="4c97d-107">此資訊可以用來判斷修補程式是否適用于目標系統。</span><span class="sxs-lookup"><span data-stu-id="4c97d-107">The information can be used to determine whether the patch applies on a target system.</span></span> <span data-ttu-id="4c97d-108">這個方法會呼叫 [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)。</span><span class="sxs-lookup"><span data-stu-id="4c97d-108">This method calls [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c97d-109">語法</span><span class="sxs-lookup"><span data-stu-id="4c97d-109">Syntax</span></span>


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a><span data-ttu-id="4c97d-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c97d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c97d-111">*PatchPath*</span><span class="sxs-lookup"><span data-stu-id="4c97d-111">*PatchPath*</span></span> 
</dt> <dd>

<span data-ttu-id="4c97d-112">要從中解壓縮適用性資訊之修補程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4c97d-112">Full path to the patch from which the applicability information is to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c97d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c97d-113">Return value</span></span>

<span data-ttu-id="4c97d-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4c97d-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c97d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c97d-115">Requirements</span></span>



| <span data-ttu-id="4c97d-116">需求</span><span class="sxs-lookup"><span data-stu-id="4c97d-116">Requirement</span></span> | <span data-ttu-id="4c97d-117">值</span><span class="sxs-lookup"><span data-stu-id="4c97d-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c97d-118">版本</span><span class="sxs-lookup"><span data-stu-id="4c97d-118">Version</span></span><br/> | <span data-ttu-id="4c97d-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4c97d-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4c97d-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4c97d-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4c97d-121">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4c97d-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="4c97d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4c97d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4c97d-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c97d-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="4c97d-124">IID</span><span class="sxs-lookup"><span data-stu-id="4c97d-124">IID</span></span><br/>     | <span data-ttu-id="4c97d-125">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4c97d-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="4c97d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c97d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c97d-127">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="4c97d-127">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[<span data-ttu-id="4c97d-128">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="4c97d-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




