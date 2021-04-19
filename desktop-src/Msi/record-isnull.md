---
description: 記錄物件的 IsNull 屬性是唯讀屬性，如果指定的欄位為 Null，則會傳回 True，如果欄位包含資料，則會傳回 False。
ms.assetid: f36240fa-d4a2-461f-a404-ba867b5f2950
title: 'Record 屬性 (實例 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IsNull
- IRecord000C1093-0000-0000-C000-000000000046.get_IsNull
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 027d5f818b63ca1883034ae0dfc12b46ef47b005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982640"
---
# <a name="recordisnull-property"></a><span data-ttu-id="38caa-103">Record 屬性</span><span class="sxs-lookup"><span data-stu-id="38caa-103">Record.IsNull property</span></span>

<span data-ttu-id="38caa-104">[**記錄**](record-object.md)物件的 **IsNull** 屬性是唯讀屬性，如果指定的欄位為 Null，則會傳回 True，如果欄位包含資料，則會傳回 False。</span><span class="sxs-lookup"><span data-stu-id="38caa-104">The **IsNull** property of the [**Record**](record-object.md) object is a read-only property that returns True if the indicated field is Null and False if the field contains data.</span></span>

<span data-ttu-id="38caa-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="38caa-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="38caa-106">語法</span><span class="sxs-lookup"><span data-stu-id="38caa-106">Syntax</span></span>


```JScript
propVal = Record.IsNull
```



## <a name="property-value"></a><span data-ttu-id="38caa-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="38caa-107">Property value</span></span>

<span data-ttu-id="38caa-108">記錄中值的必要欄位編號（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="38caa-108">Required field number of the value within the record, 1-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="38caa-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="38caa-109">Requirements</span></span>



| <span data-ttu-id="38caa-110">需求</span><span class="sxs-lookup"><span data-stu-id="38caa-110">Requirement</span></span> | <span data-ttu-id="38caa-111">值</span><span class="sxs-lookup"><span data-stu-id="38caa-111">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38caa-112">版本</span><span class="sxs-lookup"><span data-stu-id="38caa-112">Version</span></span><br/> | <span data-ttu-id="38caa-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="38caa-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="38caa-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="38caa-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="38caa-115">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="38caa-115">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="38caa-116">標頭</span><span class="sxs-lookup"><span data-stu-id="38caa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="38caa-117"><dt>實例。h</dt></span><span class="sxs-lookup"><span data-stu-id="38caa-117"><dt>Instance.h</dt></span></span> </dl>                                                                                                                                                                   |
| <span data-ttu-id="38caa-118">DLL</span><span class="sxs-lookup"><span data-stu-id="38caa-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="38caa-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38caa-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="38caa-120">IID</span><span class="sxs-lookup"><span data-stu-id="38caa-120">IID</span></span><br/>     | <span data-ttu-id="38caa-121">IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="38caa-121">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




