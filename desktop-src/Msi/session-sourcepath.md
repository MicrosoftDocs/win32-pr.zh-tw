---
description: Session 物件的 SourcePath 屬性是唯讀屬性，可提供來源媒體或伺服器映射上所指定資料夾的完整路徑。
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Session 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996489"
---
# <a name="sessionsourcepath-property"></a><span data-ttu-id="4a9f5-103">Session 屬性</span><span class="sxs-lookup"><span data-stu-id="4a9f5-103">Session.SourcePath property</span></span>

<span data-ttu-id="4a9f5-104">[**Session**](session-object.md)物件的 **SourcePath** 屬性是唯讀屬性，可提供來源媒體或伺服器映射上所指定資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4a9f5-104">The **SourcePath** property of the [**Session**](session-object.md) object is a read-only property that provides the full path to the designated folder on the source media or server image.</span></span>

<span data-ttu-id="4a9f5-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4a9f5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a9f5-106">語法</span><span class="sxs-lookup"><span data-stu-id="4a9f5-106">Syntax</span></span>


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a><span data-ttu-id="4a9f5-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="4a9f5-107">Property value</span></span>

<span data-ttu-id="4a9f5-108">需要區分大小寫的資料夾屬性名稱，如 [目錄資料表](directory-table.md)的主鍵所指定。</span><span class="sxs-lookup"><span data-stu-id="4a9f5-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="4a9f5-109">如果資料夾不存在，就會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a9f5-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a9f5-110">備註</span><span class="sxs-lookup"><span data-stu-id="4a9f5-110">Remarks</span></span>

<span data-ttu-id="4a9f5-111">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="4a9f5-111">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a9f5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a9f5-112">Requirements</span></span>



| <span data-ttu-id="4a9f5-113">需求</span><span class="sxs-lookup"><span data-stu-id="4a9f5-113">Requirement</span></span> | <span data-ttu-id="4a9f5-114">值</span><span class="sxs-lookup"><span data-stu-id="4a9f5-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a9f5-115">版本</span><span class="sxs-lookup"><span data-stu-id="4a9f5-115">Version</span></span><br/> | <span data-ttu-id="4a9f5-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4a9f5-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4a9f5-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4a9f5-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4a9f5-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="4a9f5-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4a9f5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4a9f5-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4a9f5-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a9f5-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4a9f5-121">IID</span><span class="sxs-lookup"><span data-stu-id="4a9f5-121">IID</span></span><br/>     | <span data-ttu-id="4a9f5-122">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4a9f5-122">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




