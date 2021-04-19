---
description: 安裝程式物件的 ForceSourceListResolution 方法會強制 Windows Installer 在來源清單中搜尋有效的產品來源。
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: ForceSourceListResolution 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988257"
---
# <a name="installerforcesourcelistresolution-method"></a><span data-ttu-id="0d52e-103">ForceSourceListResolution 方法</span><span class="sxs-lookup"><span data-stu-id="0d52e-103">Installer.ForceSourceListResolution method</span></span>

<span data-ttu-id="0d52e-104">[**安裝程式**](installer-object.md)物件的 **ForceSourceListResolution** 方法會強制安裝程式在下次需要來源時于來源清單中搜尋有效的產品來源，例如，當安裝程式執行安裝或重新安裝時，或需要將元件的路徑設定為從來源執行時。</span><span class="sxs-lookup"><span data-stu-id="0d52e-104">The **ForceSourceListResolution** method of the [**Installer**](installer-object.md) object forces the installer to search the source list for a valid product source the next time a source is needed, such as when the installer performs an installation or a reinstallation, or when it needs the path for a component set to run from source.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d52e-105">語法</span><span class="sxs-lookup"><span data-stu-id="0d52e-105">Syntax</span></span>


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="0d52e-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d52e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d52e-107">*產品*</span><span class="sxs-lookup"><span data-stu-id="0d52e-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="0d52e-108">指定產品代碼。</span><span class="sxs-lookup"><span data-stu-id="0d52e-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="0d52e-109">*使用者*</span><span class="sxs-lookup"><span data-stu-id="0d52e-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="0d52e-110">每個使用者安裝的使用者名稱;每一電腦安裝都是 null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="0d52e-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d52e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d52e-111">Return value</span></span>

<span data-ttu-id="0d52e-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0d52e-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d52e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d52e-113">Requirements</span></span>



| <span data-ttu-id="0d52e-114">需求</span><span class="sxs-lookup"><span data-stu-id="0d52e-114">Requirement</span></span> | <span data-ttu-id="0d52e-115">值</span><span class="sxs-lookup"><span data-stu-id="0d52e-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d52e-116">版本</span><span class="sxs-lookup"><span data-stu-id="0d52e-116">Version</span></span><br/> | <span data-ttu-id="0d52e-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="0d52e-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0d52e-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="0d52e-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0d52e-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0d52e-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0d52e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0d52e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d52e-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d52e-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0d52e-122">IID</span><span class="sxs-lookup"><span data-stu-id="0d52e-122">IID</span></span><br/>     | <span data-ttu-id="0d52e-123">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0d52e-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="0d52e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d52e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d52e-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="0d52e-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="0d52e-126">來源復原</span><span class="sxs-lookup"><span data-stu-id="0d52e-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




