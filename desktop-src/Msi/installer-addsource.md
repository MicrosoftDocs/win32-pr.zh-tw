---
description: 安裝程式物件的 AddSource 方法會將來源新增至 sourcelist 中有效網路來源的清單。
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: AddSource 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981631"
---
# <a name="installeraddsource-method"></a><span data-ttu-id="0d40a-103">AddSource 方法</span><span class="sxs-lookup"><span data-stu-id="0d40a-103">Installer.AddSource method</span></span>

<span data-ttu-id="0d40a-104">[**安裝程式**](installer-object.md)物件的 **AddSource** 方法會將來源新增至 sourcelist 中有效網路來源的清單。</span><span class="sxs-lookup"><span data-stu-id="0d40a-104">The **AddSource** method of the [**Installer**](installer-object.md) object adds a source to the list of valid network sources in the sourcelist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d40a-105">語法</span><span class="sxs-lookup"><span data-stu-id="0d40a-105">Syntax</span></span>


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a><span data-ttu-id="0d40a-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d40a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d40a-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="0d40a-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="0d40a-108">指定產品代碼。</span><span class="sxs-lookup"><span data-stu-id="0d40a-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="0d40a-109">*使用者*</span><span class="sxs-lookup"><span data-stu-id="0d40a-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="0d40a-110">每個使用者安裝的使用者名稱;每一電腦安裝都是 null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="0d40a-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> <dt>

<span data-ttu-id="0d40a-111">*來源*</span><span class="sxs-lookup"><span data-stu-id="0d40a-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="0d40a-112">指定來源之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="0d40a-112">Pointer to the string specifying the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d40a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d40a-113">Return value</span></span>

<span data-ttu-id="0d40a-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0d40a-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d40a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d40a-115">Requirements</span></span>



| <span data-ttu-id="0d40a-116">需求</span><span class="sxs-lookup"><span data-stu-id="0d40a-116">Requirement</span></span> | <span data-ttu-id="0d40a-117">值</span><span class="sxs-lookup"><span data-stu-id="0d40a-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d40a-118">版本</span><span class="sxs-lookup"><span data-stu-id="0d40a-118">Version</span></span><br/> | <span data-ttu-id="0d40a-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="0d40a-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0d40a-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="0d40a-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0d40a-121">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0d40a-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0d40a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0d40a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d40a-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d40a-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0d40a-124">IID</span><span class="sxs-lookup"><span data-stu-id="0d40a-124">IID</span></span><br/>     | <span data-ttu-id="0d40a-125">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0d40a-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="0d40a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d40a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d40a-127">**MsiSourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="0d40a-127">**MsiSourceListAddSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[<span data-ttu-id="0d40a-128">來源復原</span><span class="sxs-lookup"><span data-stu-id="0d40a-128">source resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




