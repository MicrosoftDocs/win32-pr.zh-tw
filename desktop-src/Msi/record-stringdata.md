---
description: 記錄物件的至 convertfrom-stringdata 屬性是讀寫屬性，可將字串資料傳入或傳出記錄內的指定欄位。 如果已儲存整數或物件，則會傳回其字串值。
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: 至 convertfrom-stringdata 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989835"
---
# <a name="recordstringdata-property"></a><span data-ttu-id="d65c8-104">至 convertfrom-stringdata 屬性</span><span class="sxs-lookup"><span data-stu-id="d65c8-104">Record.StringData property</span></span>

<span data-ttu-id="d65c8-105">[**記錄**](record-object.md)物件的 **至 convertfrom-stringdata** 屬性是讀寫屬性，可將字串資料傳入或傳出記錄內的指定欄位。</span><span class="sxs-lookup"><span data-stu-id="d65c8-105">The **StringData** property of the [**Record**](record-object.md) object is a read-write property that transfers string data in to or out of a specified field within the record.</span></span> <span data-ttu-id="d65c8-106">如果已儲存整數或物件，則會傳回其字串值。</span><span class="sxs-lookup"><span data-stu-id="d65c8-106">If an integer or object has been stored, its string value is returned.</span></span>

<span data-ttu-id="d65c8-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d65c8-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d65c8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d65c8-108">Syntax</span></span>


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="d65c8-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d65c8-109">Property value</span></span>

<span data-ttu-id="d65c8-110">記錄中值的必要欄位編號（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="d65c8-110">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="d65c8-111">備註</span><span class="sxs-lookup"><span data-stu-id="d65c8-111">Remarks</span></span>

<span data-ttu-id="d65c8-112">不存在之欄位的傳回值為空字串。</span><span class="sxs-lookup"><span data-stu-id="d65c8-112">The returned value of a nonexistent field is an empty string.</span></span> <span data-ttu-id="d65c8-113">若要將記錄字串欄位設定為 null，請使用空的 variant 或空字串。</span><span class="sxs-lookup"><span data-stu-id="d65c8-113">To set a record string field to null, use either an empty variant or an empty string.</span></span> <span data-ttu-id="d65c8-114">嘗試在不存在的欄位中儲存值會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="d65c8-114">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d65c8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d65c8-115">Requirements</span></span>



| <span data-ttu-id="d65c8-116">需求</span><span class="sxs-lookup"><span data-stu-id="d65c8-116">Requirement</span></span> | <span data-ttu-id="d65c8-117">值</span><span class="sxs-lookup"><span data-stu-id="d65c8-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d65c8-118">版本</span><span class="sxs-lookup"><span data-stu-id="d65c8-118">Version</span></span><br/> | <span data-ttu-id="d65c8-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d65c8-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d65c8-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d65c8-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d65c8-121">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d65c8-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d65c8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d65c8-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d65c8-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d65c8-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d65c8-124">IID</span><span class="sxs-lookup"><span data-stu-id="d65c8-124">IID</span></span><br/>     | <span data-ttu-id="d65c8-125">IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d65c8-125">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




