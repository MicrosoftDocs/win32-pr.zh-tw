---
description: Session 物件的 FeatureInfo 方法會傳回 FeatureInfo 物件，其中包含指定功能的描述性資訊。
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: FeatureInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995394"
---
# <a name="sessionfeatureinfo-method"></a><span data-ttu-id="6c613-103">FeatureInfo 方法</span><span class="sxs-lookup"><span data-stu-id="6c613-103">Session.FeatureInfo method</span></span>

<span data-ttu-id="6c613-104">[**Session**](session-object.md)物件的 **FeatureInfo** 方法會傳回 **FeatureInfo** 物件，其中包含指定功能的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="6c613-104">The **FeatureInfo** method of the [**Session**](session-object.md) object returns a **FeatureInfo** object containing descriptive information for the specified feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c613-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c613-105">Syntax</span></span>


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="6c613-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c613-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c613-107">*功能*</span><span class="sxs-lookup"><span data-stu-id="6c613-107">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="6c613-108">識別感興趣的功能。</span><span class="sxs-lookup"><span data-stu-id="6c613-108">Identifies the feature of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c613-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c613-109">Return value</span></span>

<span data-ttu-id="6c613-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c613-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c613-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c613-111">Requirements</span></span>



| <span data-ttu-id="6c613-112">需求</span><span class="sxs-lookup"><span data-stu-id="6c613-112">Requirement</span></span> | <span data-ttu-id="6c613-113">值</span><span class="sxs-lookup"><span data-stu-id="6c613-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c613-114">版本</span><span class="sxs-lookup"><span data-stu-id="6c613-114">Version</span></span><br/> | <span data-ttu-id="6c613-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="6c613-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6c613-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="6c613-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6c613-117">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6c613-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6c613-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6c613-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="6c613-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c613-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6c613-120">IID</span><span class="sxs-lookup"><span data-stu-id="6c613-120">IID</span></span><br/>     | <span data-ttu-id="6c613-121">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6c613-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="6c613-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c613-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c613-123">**MsiGetFeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="6c613-123">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




