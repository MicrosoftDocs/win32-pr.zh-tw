---
description: UIPreview 物件的屬性（Property）屬性（Property）是讀寫屬性（property），表示指定之安裝程式屬性的字串值，如果前面加上百分比符號 (% ) ，則為目前進程的系統內容變數值。
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: UIPreview 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989809"
---
# <a name="uipreviewproperty-property"></a><span data-ttu-id="dd64c-103">UIPreview 屬性</span><span class="sxs-lookup"><span data-stu-id="dd64c-103">UIPreview.Property property</span></span>

<span data-ttu-id="dd64c-104">[**UIPreview**](uipreview-object.md)物件的 **屬性（property** ）屬性（property）是讀寫屬性（property），表示指定之安裝程式屬性的字串值，如果前面加上百分比符號 (% ) ，則為目前進程的系統內容變數值。</span><span class="sxs-lookup"><span data-stu-id="dd64c-104">The **Property** property of the [**UIPreview**](uipreview-object.md) object is a read-write property that represents the string value of a named installer property, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="dd64c-105">這是為了允許適當地顯示相依于屬性值的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="dd64c-105">This is exposed to allow proper display of dialog boxes that are dependent upon property values.</span></span> <span data-ttu-id="dd64c-106">可能會提供字串或整數值。</span><span class="sxs-lookup"><span data-stu-id="dd64c-106">Either string or integer values may be supplied.</span></span> <span data-ttu-id="dd64c-107">不存在的屬性或環境變數相當於其值為 null。</span><span class="sxs-lookup"><span data-stu-id="dd64c-107">A nonexistent property or environment variable is equivalent to its value being null.</span></span>

<span data-ttu-id="dd64c-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="dd64c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd64c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd64c-109">Syntax</span></span>


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="dd64c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="dd64c-110">Property value</span></span>

<span data-ttu-id="dd64c-111">需要區分大小寫的屬性名稱，或前面加上百分比符號 (% ) 的環境變數名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dd64c-111">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd64c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd64c-112">Requirements</span></span>



| <span data-ttu-id="dd64c-113">需求</span><span class="sxs-lookup"><span data-stu-id="dd64c-113">Requirement</span></span> | <span data-ttu-id="dd64c-114">值</span><span class="sxs-lookup"><span data-stu-id="dd64c-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd64c-115">版本</span><span class="sxs-lookup"><span data-stu-id="dd64c-115">Version</span></span><br/> | <span data-ttu-id="dd64c-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="dd64c-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dd64c-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="dd64c-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dd64c-118">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="dd64c-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dd64c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="dd64c-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd64c-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd64c-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dd64c-121">IID</span><span class="sxs-lookup"><span data-stu-id="dd64c-121">IID</span></span><br/>     | <span data-ttu-id="dd64c-122">IID \_ IUIPreview 定義為 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dd64c-122">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




