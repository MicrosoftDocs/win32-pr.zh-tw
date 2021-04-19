---
description: Session 物件的 TargetPath 屬性是讀寫屬性，可提供安裝目標磁片磁碟機上指定之資料夾的完整路徑。
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: TargetPath 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984871"
---
# <a name="sessiontargetpath-property"></a><span data-ttu-id="50e21-103">TargetPath 屬性</span><span class="sxs-lookup"><span data-stu-id="50e21-103">Session.TargetPath property</span></span>

<span data-ttu-id="50e21-104">[**Session**](session-object.md)物件的 **TargetPath** 屬性是讀寫屬性，可提供安裝目標磁片磁碟機上指定之資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="50e21-104">The **TargetPath** property of the [**Session**](session-object.md) object is a read-write property that provides the full path to the designated folder on the installation target drive.</span></span>

<span data-ttu-id="50e21-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="50e21-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e21-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="50e21-106">Syntax</span></span>


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a><span data-ttu-id="50e21-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="50e21-107">Property value</span></span>

<span data-ttu-id="50e21-108">需要區分大小寫的資料夾屬性名稱，如 [目錄資料表](directory-table.md)的主鍵所指定。</span><span class="sxs-lookup"><span data-stu-id="50e21-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="50e21-109">如果資料夾不存在，就會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="50e21-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e21-110">備註</span><span class="sxs-lookup"><span data-stu-id="50e21-110">Remarks</span></span>

<span data-ttu-id="50e21-111">如果已為目前使用者或其他使用者安裝使用這些路徑的元件，請不要嘗試設定目標路徑。</span><span class="sxs-lookup"><span data-stu-id="50e21-111">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="50e21-112">檢查 [**ProductState**](productstate.md) 屬性，以判斷是否已安裝包含該元件的產品。</span><span class="sxs-lookup"><span data-stu-id="50e21-112">Check the [**ProductState**](productstate.md) property to determine if the product that contains the component is installed.</span></span>

<span data-ttu-id="50e21-113">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="50e21-113">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e21-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="50e21-114">Requirements</span></span>



| <span data-ttu-id="50e21-115">需求</span><span class="sxs-lookup"><span data-stu-id="50e21-115">Requirement</span></span> | <span data-ttu-id="50e21-116">值</span><span class="sxs-lookup"><span data-stu-id="50e21-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e21-117">版本</span><span class="sxs-lookup"><span data-stu-id="50e21-117">Version</span></span><br/> | <span data-ttu-id="50e21-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="50e21-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="50e21-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="50e21-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="50e21-120">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="50e21-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="50e21-121">DLL</span><span class="sxs-lookup"><span data-stu-id="50e21-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="50e21-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e21-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="50e21-123">IID</span><span class="sxs-lookup"><span data-stu-id="50e21-123">IID</span></span><br/>     | <span data-ttu-id="50e21-124">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="50e21-124">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




