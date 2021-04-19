---
description: 這是記錄物件的 IntegerData 屬性。 此讀寫屬性會將32位整數資料傳入或傳出記錄內的指定欄位。 如果域值無法轉換成整數，則會傳回 msiDatabaseNullInteger。
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: IntegerData 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987149"
---
# <a name="recordintegerdata-property"></a><span data-ttu-id="5bae7-105">IntegerData 屬性</span><span class="sxs-lookup"><span data-stu-id="5bae7-105">Record.IntegerData property</span></span>

<span data-ttu-id="5bae7-106">這是 [**記錄**](record-object.md)物件的 **IntegerData** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5bae7-106">This is the **IntegerData** property of the [**Record**](record-object.md) object.</span></span> <span data-ttu-id="5bae7-107">此讀寫屬性會將32位整數資料傳入或傳出記錄內的指定欄位。</span><span class="sxs-lookup"><span data-stu-id="5bae7-107">This read-write property transfers 32-bit integer data in to or out of a specified field within the record.</span></span> <span data-ttu-id="5bae7-108">如果域值無法轉換成整數，則會傳回 msiDatabaseNullInteger。</span><span class="sxs-lookup"><span data-stu-id="5bae7-108">If a field value cannot be converted to an integer, msiDatabaseNullInteger is returned.</span></span>

<span data-ttu-id="5bae7-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5bae7-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bae7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bae7-110">Syntax</span></span>


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="5bae7-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="5bae7-111">Property value</span></span>

<span data-ttu-id="5bae7-112">記錄中值的必要欄位編號（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="5bae7-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bae7-113">備註</span><span class="sxs-lookup"><span data-stu-id="5bae7-113">Remarks</span></span>

<span data-ttu-id="5bae7-114">若要將記錄整數位段設定為 null，請使用 msiDatabaseNullInteger。</span><span class="sxs-lookup"><span data-stu-id="5bae7-114">To set a record integer field to null, use msiDatabaseNullInteger.</span></span> <span data-ttu-id="5bae7-115">不存在的欄位傳回的值為 msiDatabaseNullInteger。</span><span class="sxs-lookup"><span data-stu-id="5bae7-115">The returned value of a nonexistent field is msiDatabaseNullInteger.</span></span> <span data-ttu-id="5bae7-116">嘗試在不存在的欄位中儲存值會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="5bae7-116">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bae7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bae7-117">Requirements</span></span>



| <span data-ttu-id="5bae7-118">需求</span><span class="sxs-lookup"><span data-stu-id="5bae7-118">Requirement</span></span> | <span data-ttu-id="5bae7-119">值</span><span class="sxs-lookup"><span data-stu-id="5bae7-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bae7-120">版本</span><span class="sxs-lookup"><span data-stu-id="5bae7-120">Version</span></span><br/> | <span data-ttu-id="5bae7-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5bae7-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5bae7-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5bae7-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5bae7-123">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5bae7-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5bae7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5bae7-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5bae7-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bae7-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5bae7-126">IID</span><span class="sxs-lookup"><span data-stu-id="5bae7-126">IID</span></span><br/>     | <span data-ttu-id="5bae7-127">IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5bae7-127">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




