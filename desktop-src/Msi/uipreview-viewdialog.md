---
description: UIPreview 物件的 ViewDialog 方法會顯示儲存在目前資料庫中的 [撰寫的使用者介面] 對話方塊。
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: UIPreview. ViewDialog 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewDialog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d9ad3772ced2dba952a3d3b068aaa307d1c06398
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995926"
---
# <a name="uipreviewviewdialog-method"></a><span data-ttu-id="e2d4d-103">UIPreview. ViewDialog 方法</span><span class="sxs-lookup"><span data-stu-id="e2d4d-103">UIPreview.ViewDialog method</span></span>

<span data-ttu-id="e2d4d-104">[**UIPreview**](uipreview-object.md)物件的 **ViewDialog** 方法會顯示儲存在目前資料庫中的 [撰寫的使用者介面] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e2d4d-104">The **ViewDialog** method of the [**UIPreview**](uipreview-object.md) object displays an authored user interface dialog box stored in the current database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d4d-105">語法</span><span class="sxs-lookup"><span data-stu-id="e2d4d-105">Syntax</span></span>


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a><span data-ttu-id="e2d4d-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2d4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d4d-107">*對話 框*</span><span class="sxs-lookup"><span data-stu-id="e2d4d-107">*dialog*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d4d-108">對話方塊的必要名稱、區分大小寫，以及對話方塊資料庫資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e2d4d-108">Required name of the dialog box, case-sensitive, and the primary key of the Dialog database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2d4d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2d4d-109">Return value</span></span>

<span data-ttu-id="e2d4d-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e2d4d-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d4d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2d4d-111">Requirements</span></span>



| <span data-ttu-id="e2d4d-112">需求</span><span class="sxs-lookup"><span data-stu-id="e2d4d-112">Requirement</span></span> | <span data-ttu-id="e2d4d-113">值</span><span class="sxs-lookup"><span data-stu-id="e2d4d-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d4d-114">版本</span><span class="sxs-lookup"><span data-stu-id="e2d4d-114">Version</span></span><br/> | <span data-ttu-id="e2d4d-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e2d4d-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e2d4d-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e2d4d-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e2d4d-117">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e2d4d-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e2d4d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e2d4d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2d4d-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2d4d-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e2d4d-120">IID</span><span class="sxs-lookup"><span data-stu-id="e2d4d-120">IID</span></span><br/>     | <span data-ttu-id="e2d4d-121">IID \_ IUIPreview 定義為 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e2d4d-121">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




