---
description: 安裝程式物件的 ProductInfoFromScript 屬性會傳回儲存在公告腳本中指定之屬性的值。
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: 安裝程式：:P roductInfoFromScript 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995967"
---
# <a name="installerproductinfofromscript-property"></a><span data-ttu-id="7f8ff-103">安裝程式：:P roductInfoFromScript 屬性</span><span class="sxs-lookup"><span data-stu-id="7f8ff-103">Installer::ProductInfoFromScript property</span></span>

<span data-ttu-id="7f8ff-104">[**安裝程式**](installer-object.md)物件的 **ProductInfoFromScript** 屬性會傳回儲存在公告腳本中指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-104">The **ProductInfoFromScript** property of the [**Installer**](installer-object.md) object returns the value of the specified attribute that is stored in an advertise script.</span></span>

<span data-ttu-id="7f8ff-105">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f8ff-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f8ff-106">Syntax</span></span>


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a><span data-ttu-id="7f8ff-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="7f8ff-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f8ff-108">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7f8ff-108">Error codes</span></span>

<span data-ttu-id="7f8ff-109">根據要求的屬性而定的字串或整數值。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-109">A string or integer value depending upon requested attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f8ff-110">備註</span><span class="sxs-lookup"><span data-stu-id="7f8ff-110">Remarks</span></span>

<span data-ttu-id="7f8ff-111">**ProductInfoFromScript** 屬性使用 [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta)函數。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-111">The **ProductInfoFromScript** property uses the [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) function.</span></span>

## <a name="examples"></a><span data-ttu-id="7f8ff-112">範例</span><span class="sxs-lookup"><span data-stu-id="7f8ff-112">Examples</span></span>

<span data-ttu-id="7f8ff-113">下列範例腳本示範如何使用 **ProductInfoFromScript** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-113">The following sample script demonstrates the use of the **ProductInfoFromScript** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a><span data-ttu-id="7f8ff-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f8ff-114">Requirements</span></span>



| <span data-ttu-id="7f8ff-115">需求</span><span class="sxs-lookup"><span data-stu-id="7f8ff-115">Requirement</span></span> | <span data-ttu-id="7f8ff-116">值</span><span class="sxs-lookup"><span data-stu-id="7f8ff-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8ff-117">版本</span><span class="sxs-lookup"><span data-stu-id="7f8ff-117">Version</span></span><br/> | <span data-ttu-id="7f8ff-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7f8ff-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7f8ff-120">Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5</span><span class="sxs-lookup"><span data-stu-id="7f8ff-120">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="7f8ff-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7f8ff-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="7f8ff-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f8ff-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="7f8ff-123">IID</span><span class="sxs-lookup"><span data-stu-id="7f8ff-123">IID</span></span><br/>     | <span data-ttu-id="7f8ff-124">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7f8ff-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="7f8ff-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f8ff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8ff-126">**安裝程式**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-126">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="7f8ff-127">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="7f8ff-127">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




