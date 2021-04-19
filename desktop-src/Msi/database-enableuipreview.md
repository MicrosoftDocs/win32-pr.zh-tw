---
description: 資料庫物件的 EnableUIPreview 方法可提供所需的支援來查看儲存在安裝程式資料庫中的使用者介面對話方塊，藉此協助撰寫對話方塊和公告欄。
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: EnableUIPreview 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1224bb100e0403e8df9f3bdb0cc0b5dbe017233f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984391"
---
# <a name="databaseenableuipreview-method"></a><span data-ttu-id="830d2-103">EnableUIPreview 方法</span><span class="sxs-lookup"><span data-stu-id="830d2-103">Database.EnableUIPreview method</span></span>

<span data-ttu-id="830d2-104">[**資料庫**](database-object.md)物件的 **EnableUIPreview** 方法可提供所需的支援來查看儲存在安裝程式資料庫中的使用者介面對話方塊，藉此協助撰寫對話方塊和公告欄。</span><span class="sxs-lookup"><span data-stu-id="830d2-104">The **EnableUIPreview** method of the [**Database**](database-object.md) object facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span> <span data-ttu-id="830d2-105">方法會藉由傳回預覽 **資料庫** 物件來啟動預覽模式。</span><span class="sxs-lookup"><span data-stu-id="830d2-105">The method starts the preview mode by returning a preview **Database** object.</span></span> <span data-ttu-id="830d2-106">預覽模式會在預覽物件發行時結束。</span><span class="sxs-lookup"><span data-stu-id="830d2-106">The preview mode ends when the preview object is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="830d2-107">語法</span><span class="sxs-lookup"><span data-stu-id="830d2-107">Syntax</span></span>


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a><span data-ttu-id="830d2-108">參數</span><span class="sxs-lookup"><span data-stu-id="830d2-108">Parameters</span></span>

<span data-ttu-id="830d2-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="830d2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="830d2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="830d2-110">Return value</span></span>

<span data-ttu-id="830d2-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="830d2-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="830d2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="830d2-112">Requirements</span></span>



| <span data-ttu-id="830d2-113">需求</span><span class="sxs-lookup"><span data-stu-id="830d2-113">Requirement</span></span> | <span data-ttu-id="830d2-114">值</span><span class="sxs-lookup"><span data-stu-id="830d2-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="830d2-115">版本</span><span class="sxs-lookup"><span data-stu-id="830d2-115">Version</span></span><br/> | <span data-ttu-id="830d2-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="830d2-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="830d2-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="830d2-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="830d2-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="830d2-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="830d2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="830d2-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="830d2-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="830d2-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="830d2-121">IID</span><span class="sxs-lookup"><span data-stu-id="830d2-121">IID</span></span><br/>     | <span data-ttu-id="830d2-122">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="830d2-122">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




