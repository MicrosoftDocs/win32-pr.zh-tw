---
description: Session 物件的 ComponentCurrentState 屬性是唯讀屬性，它會傳回指定元件的目前已安裝狀態。 如需狀態值的詳細資料，請參閱 ComponentRequestState 屬性。
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: ComponentCurrentState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989847"
---
# <a name="sessioncomponentcurrentstate-property"></a><span data-ttu-id="934a0-104">ComponentCurrentState 屬性</span><span class="sxs-lookup"><span data-stu-id="934a0-104">Session.ComponentCurrentState property</span></span>

<span data-ttu-id="934a0-105">[**Session**](session-object.md)物件的 **ComponentCurrentState** 屬性是唯讀屬性，它會傳回指定元件的目前已安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="934a0-105">The **ComponentCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated component.</span></span> <span data-ttu-id="934a0-106">如需狀態值的詳細資料，請參閱 [**ComponentRequestState**](session-componentrequeststate.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="934a0-106">For state values, see the [**ComponentRequestState**](session-componentrequeststate.md) property.</span></span>

<span data-ttu-id="934a0-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="934a0-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="934a0-108">語法</span><span class="sxs-lookup"><span data-stu-id="934a0-108">Syntax</span></span>


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a><span data-ttu-id="934a0-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="934a0-109">Property value</span></span>

<span data-ttu-id="934a0-110">所要求元件的必要字串名稱，以及元件資料表中的主要金鑰。</span><span class="sxs-lookup"><span data-stu-id="934a0-110">Required string name of the requested component, primary key into the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="934a0-111">備註</span><span class="sxs-lookup"><span data-stu-id="934a0-111">Remarks</span></span>

<span data-ttu-id="934a0-112">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="934a0-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="934a0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="934a0-113">Requirements</span></span>



| <span data-ttu-id="934a0-114">需求</span><span class="sxs-lookup"><span data-stu-id="934a0-114">Requirement</span></span> | <span data-ttu-id="934a0-115">值</span><span class="sxs-lookup"><span data-stu-id="934a0-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="934a0-116">版本</span><span class="sxs-lookup"><span data-stu-id="934a0-116">Version</span></span><br/> | <span data-ttu-id="934a0-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="934a0-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="934a0-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="934a0-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="934a0-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="934a0-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="934a0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="934a0-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="934a0-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="934a0-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="934a0-122">IID</span><span class="sxs-lookup"><span data-stu-id="934a0-122">IID</span></span><br/>     | <span data-ttu-id="934a0-123">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="934a0-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="934a0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="934a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934a0-125">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="934a0-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="934a0-126">**ComponentRequestState 屬性**</span><span class="sxs-lookup"><span data-stu-id="934a0-126">**ComponentRequestState property**</span></span>](session-componentrequeststate.md)
</dt> </dl>

 

 




