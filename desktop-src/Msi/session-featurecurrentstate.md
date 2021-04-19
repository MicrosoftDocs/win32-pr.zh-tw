---
description: Session 物件的 FeatureCurrentState 屬性是唯讀屬性，會傳回指定功能目前已安裝的狀態。 如需狀態值的詳細資料，請參閱 FeatureRequestState 屬性。
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: FeatureCurrentState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982648"
---
# <a name="sessionfeaturecurrentstate-property"></a><span data-ttu-id="60113-104">FeatureCurrentState 屬性</span><span class="sxs-lookup"><span data-stu-id="60113-104">Session.FeatureCurrentState property</span></span>

<span data-ttu-id="60113-105">[**Session**](session-object.md)物件的 **FeatureCurrentState** 屬性是唯讀屬性，會傳回指定功能目前已安裝的狀態。</span><span class="sxs-lookup"><span data-stu-id="60113-105">The **FeatureCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated feature.</span></span> <span data-ttu-id="60113-106">如需狀態值的詳細資料，請參閱 [**FeatureRequestState**](session-featurerequeststate.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="60113-106">For state values, see the [**FeatureRequestState**](session-featurerequeststate.md) property.</span></span>

<span data-ttu-id="60113-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="60113-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="60113-108">語法</span><span class="sxs-lookup"><span data-stu-id="60113-108">Syntax</span></span>


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a><span data-ttu-id="60113-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="60113-109">Property value</span></span>

<span data-ttu-id="60113-110">要求的功能所需的字串名稱，以及 [功能資料表](feature-table.md)中的主鍵。</span><span class="sxs-lookup"><span data-stu-id="60113-110">Required string name of the requested feature, and a primary key into the [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="60113-111">備註</span><span class="sxs-lookup"><span data-stu-id="60113-111">Remarks</span></span>

<span data-ttu-id="60113-112">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="60113-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="60113-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="60113-113">Requirements</span></span>



| <span data-ttu-id="60113-114">需求</span><span class="sxs-lookup"><span data-stu-id="60113-114">Requirement</span></span> | <span data-ttu-id="60113-115">值</span><span class="sxs-lookup"><span data-stu-id="60113-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60113-116">版本</span><span class="sxs-lookup"><span data-stu-id="60113-116">Version</span></span><br/> | <span data-ttu-id="60113-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="60113-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="60113-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="60113-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="60113-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="60113-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="60113-120">DLL</span><span class="sxs-lookup"><span data-stu-id="60113-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="60113-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60113-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="60113-122">IID</span><span class="sxs-lookup"><span data-stu-id="60113-122">IID</span></span><br/>     | <span data-ttu-id="60113-123">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="60113-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="60113-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60113-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60113-125">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="60113-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="60113-126">**FeatureRequestState 屬性**</span><span class="sxs-lookup"><span data-stu-id="60113-126">**FeatureRequestState property**</span></span>](session-featurerequeststate.md)
</dt> </dl>

 

 




