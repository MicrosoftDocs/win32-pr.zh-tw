---
description: 安裝程式物件的 ClearSourceList 方法會從來源清單中移除所有的網路來源。
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: ClearSourceList 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992574"
---
# <a name="installerclearsourcelist-method"></a><span data-ttu-id="4fb25-103">ClearSourceList 方法</span><span class="sxs-lookup"><span data-stu-id="4fb25-103">Installer.ClearSourceList method</span></span>

<span data-ttu-id="4fb25-104">[**安裝程式**](installer-object.md)物件的 **ClearSourceList** 方法會從來源清單中移除所有的網路來源。</span><span class="sxs-lookup"><span data-stu-id="4fb25-104">The **ClearSourceList** method of the [**Installer**](installer-object.md) object removes all network sources from the source list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb25-105">語法</span><span class="sxs-lookup"><span data-stu-id="4fb25-105">Syntax</span></span>


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="4fb25-106">參數</span><span class="sxs-lookup"><span data-stu-id="4fb25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb25-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="4fb25-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="4fb25-108">指定產品代碼。</span><span class="sxs-lookup"><span data-stu-id="4fb25-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="4fb25-109">*使用者*</span><span class="sxs-lookup"><span data-stu-id="4fb25-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="4fb25-110">每個使用者安裝的使用者名稱;每一電腦安裝都是 null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="4fb25-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fb25-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fb25-111">Return value</span></span>

<span data-ttu-id="4fb25-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4fb25-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb25-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fb25-113">Requirements</span></span>



| <span data-ttu-id="4fb25-114">需求</span><span class="sxs-lookup"><span data-stu-id="4fb25-114">Requirement</span></span> | <span data-ttu-id="4fb25-115">值</span><span class="sxs-lookup"><span data-stu-id="4fb25-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb25-116">版本</span><span class="sxs-lookup"><span data-stu-id="4fb25-116">Version</span></span><br/> | <span data-ttu-id="4fb25-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4fb25-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4fb25-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4fb25-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4fb25-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="4fb25-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4fb25-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4fb25-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4fb25-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fb25-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4fb25-122">IID</span><span class="sxs-lookup"><span data-stu-id="4fb25-122">IID</span></span><br/>     | <span data-ttu-id="4fb25-123">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4fb25-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="4fb25-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fb25-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb25-125">**MsiSourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="4fb25-125">**MsiSourceListClearAll**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[<span data-ttu-id="4fb25-126">來源復原</span><span class="sxs-lookup"><span data-stu-id="4fb25-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




