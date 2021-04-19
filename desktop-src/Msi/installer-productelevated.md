---
description: 如果產品是受控的，安裝程式物件的 ProductElevated 屬性會傳回 True，如果產品不受管理，則傳回 False。
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: 安裝程式：:P roductElevated 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976249"
---
# <a name="installerproductelevated-property"></a><span data-ttu-id="8e214-103">安裝程式：:P roductElevated 屬性</span><span class="sxs-lookup"><span data-stu-id="8e214-103">Installer::ProductElevated property</span></span>

<span data-ttu-id="8e214-104">如果產品是受控的，[**安裝程式**](installer-object.md)物件的 **ProductElevated** 屬性會傳回 True，如果產品不受管理，則傳回 False。</span><span class="sxs-lookup"><span data-stu-id="8e214-104">The **ProductElevated** property of the [**Installer**](installer-object.md) object returns True if the product is managed or False if the product is not managed.</span></span>

<span data-ttu-id="8e214-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8e214-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e214-106">語法</span><span class="sxs-lookup"><span data-stu-id="8e214-106">Syntax</span></span>


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a><span data-ttu-id="8e214-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="8e214-107">Property value</span></span>

<span data-ttu-id="8e214-108">產品的完整產品代碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="8e214-108">The full product code GUID of the product.</span></span> <span data-ttu-id="8e214-109">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="8e214-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e214-110">備註</span><span class="sxs-lookup"><span data-stu-id="8e214-110">Remarks</span></span>

<span data-ttu-id="8e214-111">**ProductElevated** 屬性使用 [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)函數。</span><span class="sxs-lookup"><span data-stu-id="8e214-111">The **ProductElevated** property uses the [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) function.</span></span> <span data-ttu-id="8e214-112">傳回屬性不會考慮 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則。</span><span class="sxs-lookup"><span data-stu-id="8e214-112">The return of the property does not take into account the [AlwaysInstallElevated](alwaysinstallelevated.md) policy.</span></span>

## <a name="examples"></a><span data-ttu-id="8e214-113">範例</span><span class="sxs-lookup"><span data-stu-id="8e214-113">Examples</span></span>

<span data-ttu-id="8e214-114">下列範例腳本示範如何使用 **ProductElevated** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8e214-114">The following sample script demonstrates the use of the **ProductElevated** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a><span data-ttu-id="8e214-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e214-115">Requirements</span></span>



| <span data-ttu-id="8e214-116">需求</span><span class="sxs-lookup"><span data-stu-id="8e214-116">Requirement</span></span> | <span data-ttu-id="8e214-117">值</span><span class="sxs-lookup"><span data-stu-id="8e214-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e214-118">版本</span><span class="sxs-lookup"><span data-stu-id="8e214-118">Version</span></span><br/> | <span data-ttu-id="8e214-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="8e214-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8e214-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="8e214-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8e214-121">Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5</span><span class="sxs-lookup"><span data-stu-id="8e214-121">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="8e214-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8e214-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8e214-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e214-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="8e214-124">IID</span><span class="sxs-lookup"><span data-stu-id="8e214-124">IID</span></span><br/>     | <span data-ttu-id="8e214-125">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8e214-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="8e214-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e214-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e214-127">**安裝程式**</span><span class="sxs-lookup"><span data-stu-id="8e214-127">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="8e214-128">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="8e214-128">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




