---
description: Session 物件的 FeatureCost 屬性會傳回指定功能所需的磁碟空間總量 (（以512位元組為單位）) 所需的大小，以及 (到功能資料表) 的根目錄的父功能。
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: FeatureCost 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977759"
---
# <a name="sessionfeaturecost-property"></a><span data-ttu-id="df4f9-103">FeatureCost 屬性</span><span class="sxs-lookup"><span data-stu-id="df4f9-103">Session.FeatureCost property</span></span>

<span data-ttu-id="df4f9-104">[**Session**](session-object.md)物件的 **FeatureCost** 屬性會傳回指定功能所需的磁碟空間總量 (（以512位元組為單位）) 所需的大小，以及 (到功能資料表) 的根目錄的父功能。</span><span class="sxs-lookup"><span data-stu-id="df4f9-104">The **FeatureCost** property of the [**Session**](session-object.md) object returns the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the Feature table).</span></span> <span data-ttu-id="df4f9-105">針對每個功能，總成本是由連結至該功能之每個元件的磁片成本所組成。</span><span class="sxs-lookup"><span data-stu-id="df4f9-105">For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.</span></span>

<span data-ttu-id="df4f9-106">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="df4f9-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df4f9-107">語法</span><span class="sxs-lookup"><span data-stu-id="df4f9-107">Syntax</span></span>


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a><span data-ttu-id="df4f9-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="df4f9-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="df4f9-109">備註</span><span class="sxs-lookup"><span data-stu-id="df4f9-109">Remarks</span></span>

<span data-ttu-id="df4f9-110">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="df4f9-110">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="df4f9-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="df4f9-111">Requirements</span></span>



| <span data-ttu-id="df4f9-112">需求</span><span class="sxs-lookup"><span data-stu-id="df4f9-112">Requirement</span></span> | <span data-ttu-id="df4f9-113">值</span><span class="sxs-lookup"><span data-stu-id="df4f9-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df4f9-114">版本</span><span class="sxs-lookup"><span data-stu-id="df4f9-114">Version</span></span><br/> | <span data-ttu-id="df4f9-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="df4f9-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="df4f9-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="df4f9-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="df4f9-117">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="df4f9-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="df4f9-118">DLL</span><span class="sxs-lookup"><span data-stu-id="df4f9-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="df4f9-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df4f9-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="df4f9-120">IID</span><span class="sxs-lookup"><span data-stu-id="df4f9-120">IID</span></span><br/>     | <span data-ttu-id="df4f9-121">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="df4f9-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




