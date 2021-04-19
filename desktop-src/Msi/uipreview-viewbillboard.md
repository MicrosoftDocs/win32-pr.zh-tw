---
description: UIPreview 物件的 ViewBillboard 方法會使用目前顯示之對話方塊中的主控制項來顯示撰寫的佈告欄。
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: UIPreview. ViewBillboard 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990209"
---
# <a name="uipreviewviewbillboard-method"></a><span data-ttu-id="a20cd-103">UIPreview. ViewBillboard 方法</span><span class="sxs-lookup"><span data-stu-id="a20cd-103">UIPreview.ViewBillboard method</span></span>

<span data-ttu-id="a20cd-104">[**UIPreview**](uipreview-object.md)物件的 **ViewBillboard** 方法會使用目前顯示之對話方塊中的主控制項來顯示撰寫的佈告欄。</span><span class="sxs-lookup"><span data-stu-id="a20cd-104">The **ViewBillboard** method of the [**UIPreview**](uipreview-object.md) object displays an authored billboard using the host control in the currently displayed dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="a20cd-105">Syntax</span></span>


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a><span data-ttu-id="a20cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="a20cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a20cd-107">*control*</span><span class="sxs-lookup"><span data-stu-id="a20cd-107">*control*</span></span> 
</dt> <dd>

<span data-ttu-id="a20cd-108">裝載佈告欄、區分大小寫、以及控制項資料庫資料表之主鍵的控制項所需的名稱。</span><span class="sxs-lookup"><span data-stu-id="a20cd-108">Required name of the control hosting the billboard, case-sensitive, along with the dialog box, and the primary keys of the Control database table.</span></span>

</dd> <dt>

<span data-ttu-id="a20cd-109">*廣告 牌*</span><span class="sxs-lookup"><span data-stu-id="a20cd-109">*billboard*</span></span> 
</dt> <dd>

<span data-ttu-id="a20cd-110">使用指定的控制項和目前的對話方塊，以及佈告欄資料庫資料表的主鍵，所要顯示的佈告欄的必要名稱。</span><span class="sxs-lookup"><span data-stu-id="a20cd-110">Required name of the billboard to display using the specified control and current dialog box, and the primary key of the Billboard database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a20cd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a20cd-111">Return value</span></span>

<span data-ttu-id="a20cd-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a20cd-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a20cd-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a20cd-113">Requirements</span></span>



| <span data-ttu-id="a20cd-114">需求</span><span class="sxs-lookup"><span data-stu-id="a20cd-114">Requirement</span></span> | <span data-ttu-id="a20cd-115">值</span><span class="sxs-lookup"><span data-stu-id="a20cd-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a20cd-116">版本</span><span class="sxs-lookup"><span data-stu-id="a20cd-116">Version</span></span><br/> | <span data-ttu-id="a20cd-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a20cd-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a20cd-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a20cd-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a20cd-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a20cd-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a20cd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a20cd-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a20cd-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a20cd-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a20cd-122">IID</span><span class="sxs-lookup"><span data-stu-id="a20cd-122">IID</span></span><br/>     | <span data-ttu-id="a20cd-123">IID \_ IUIPreview 定義為 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a20cd-123">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




