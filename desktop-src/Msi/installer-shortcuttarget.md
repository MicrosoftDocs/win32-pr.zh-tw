---
description: 安裝程式物件的 ShortcutTarget 屬性會檢查快捷方式，並傳回其產品、功能名稱和元件（如果有的話）。
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: ShortcutTarget 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983187"
---
# <a name="installershortcuttarget-property"></a><span data-ttu-id="bedbc-103">ShortcutTarget 屬性</span><span class="sxs-lookup"><span data-stu-id="bedbc-103">Installer.ShortcutTarget property</span></span>

<span data-ttu-id="bedbc-104">[**安裝程式**](installer-object.md)物件的 **ShortcutTarget** 屬性會檢查快捷方式，並傳回其產品、功能名稱和元件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="bedbc-104">The **ShortcutTarget** property of the [**Installer**](installer-object.md) object examines a shortcut and returns its product, feature name, and component if available.</span></span>

<span data-ttu-id="bedbc-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="bedbc-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bedbc-106">語法</span><span class="sxs-lookup"><span data-stu-id="bedbc-106">Syntax</span></span>


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a><span data-ttu-id="bedbc-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="bedbc-107">Property value</span></span>

<span data-ttu-id="bedbc-108">檔案的完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="bedbc-108">Full path and file name for the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="bedbc-109">備註</span><span class="sxs-lookup"><span data-stu-id="bedbc-109">Remarks</span></span>

<span data-ttu-id="bedbc-110">ShortcutTarget 會傳回包含三個欄位的 [**記錄物件**](record-object.md) ：</span><span class="sxs-lookup"><span data-stu-id="bedbc-110">ShortcutTarget returns a [**Record object**](record-object.md) that contains three fields:</span></span>

-   <span data-ttu-id="bedbc-111">[欄位 1] 是快捷方式的產品代碼 GUID （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="bedbc-111">Field 1 is a GUID for the product code of the shortcut, if available.</span></span> <span data-ttu-id="bedbc-112">這個欄位可以是 null。</span><span class="sxs-lookup"><span data-stu-id="bedbc-112">This field can be null.</span></span>
-   <span data-ttu-id="bedbc-113">欄位2是快捷方式的功能識別碼（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="bedbc-113">Field 2 is the Feature ID of the shortcut, if available.</span></span> <span data-ttu-id="bedbc-114">這個欄位可以是 null。</span><span class="sxs-lookup"><span data-stu-id="bedbc-114">This field can be null.</span></span>
-   <span data-ttu-id="bedbc-115">欄位3是元件程式碼的 GUID （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="bedbc-115">Field 3 is a GUID for the component code, if available.</span></span> <span data-ttu-id="bedbc-116">這個欄位可以是 null。</span><span class="sxs-lookup"><span data-stu-id="bedbc-116">This field can be null.</span></span>

## <a name="requirements"></a><span data-ttu-id="bedbc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bedbc-117">Requirements</span></span>



| <span data-ttu-id="bedbc-118">需求</span><span class="sxs-lookup"><span data-stu-id="bedbc-118">Requirement</span></span> | <span data-ttu-id="bedbc-119">值</span><span class="sxs-lookup"><span data-stu-id="bedbc-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bedbc-120">版本</span><span class="sxs-lookup"><span data-stu-id="bedbc-120">Version</span></span><br/> | <span data-ttu-id="bedbc-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="bedbc-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bedbc-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="bedbc-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bedbc-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="bedbc-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bedbc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bedbc-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="bedbc-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bedbc-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bedbc-126">IID</span><span class="sxs-lookup"><span data-stu-id="bedbc-126">IID</span></span><br/>     | <span data-ttu-id="bedbc-127">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bedbc-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="bedbc-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bedbc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bedbc-129">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="bedbc-129">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[<span data-ttu-id="bedbc-130">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="bedbc-130">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




