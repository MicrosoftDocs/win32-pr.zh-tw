---
description: View 物件的 ColumnInfo 屬性會傳回包含結果集中每個資料行之要求資訊的記錄物件。
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: ColumnInfo 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994253"
---
# <a name="viewcolumninfo-property"></a><span data-ttu-id="713fc-103">ColumnInfo 屬性</span><span class="sxs-lookup"><span data-stu-id="713fc-103">View.ColumnInfo property</span></span>

<span data-ttu-id="713fc-104">[**View**](view-object.md)物件的 **ColumnInfo** 屬性會傳回包含結果集中每個資料行之要求資訊的 [**記錄**](record-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="713fc-104">The **ColumnInfo** property of the [**View**](view-object.md) object returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span> <span data-ttu-id="713fc-105">可以要求資料行名稱或資料行定義。</span><span class="sxs-lookup"><span data-stu-id="713fc-105">Either the column names or the column definitions may be requested.</span></span> <span data-ttu-id="713fc-106">選取清單中提供的常數沒有名稱。</span><span class="sxs-lookup"><span data-stu-id="713fc-106">Constants supplied in the Select list do not have names.</span></span>

<span data-ttu-id="713fc-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="713fc-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="713fc-108">語法</span><span class="sxs-lookup"><span data-stu-id="713fc-108">Syntax</span></span>


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a><span data-ttu-id="713fc-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="713fc-109">Property value</span></span>

<span data-ttu-id="713fc-110">每個資料行所需的必要資訊。</span><span class="sxs-lookup"><span data-stu-id="713fc-110">Required information needed for each column.</span></span>



| <span data-ttu-id="713fc-111">參數名稱</span><span class="sxs-lookup"><span data-stu-id="713fc-111">Parameter name</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="713fc-112">意義</span><span class="sxs-lookup"><span data-stu-id="713fc-112">Meaning</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <span data-ttu-id="713fc-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="713fc-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="713fc-114">傳回結果集內所有非常數資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="713fc-114">Returns the names of all nonconstant columns in result set.</span></span><br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <span data-ttu-id="713fc-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="713fc-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="713fc-116">傳回結果集內所有非常數資料行的類型。</span><span class="sxs-lookup"><span data-stu-id="713fc-116">Returns the types of all nonconstant columns in result set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="713fc-117">備註</span><span class="sxs-lookup"><span data-stu-id="713fc-117">Remarks</span></span>

<span data-ttu-id="713fc-118">**ColumnInfo** 屬性所傳回的資料行描述採用資料 [行定義格式](column-definition-format.md)所述的格式。</span><span class="sxs-lookup"><span data-stu-id="713fc-118">The column descriptions returned by the **ColumnInfo** property are in the format described in [Column Definition Format](column-definition-format.md).</span></span> <span data-ttu-id="713fc-119">每個資料行都是由對應的 [記錄] 欄位中的字串所描述。</span><span class="sxs-lookup"><span data-stu-id="713fc-119">Each column is described by a string in the corresponding record field.</span></span> <span data-ttu-id="713fc-120">定義字串是由代表資料類型的單一字母，以及資料行的寬度 (（如果適用的話）或其他位元組) 。</span><span class="sxs-lookup"><span data-stu-id="713fc-120">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, or else bytes).</span></span> <span data-ttu-id="713fc-121">寬度為零會指定未系結的寬度 (長文字欄位和資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="713fc-121">A width of zero designates an unbounded width (long text fields and streams).</span></span> <span data-ttu-id="713fc-122">大寫字母表示資料行中允許 Null 值。</span><span class="sxs-lookup"><span data-stu-id="713fc-122">An uppercase letter indicates that Null values are allowed in the column.</span></span>

## <a name="requirements"></a><span data-ttu-id="713fc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="713fc-123">Requirements</span></span>



| <span data-ttu-id="713fc-124">需求</span><span class="sxs-lookup"><span data-stu-id="713fc-124">Requirement</span></span> | <span data-ttu-id="713fc-125">值</span><span class="sxs-lookup"><span data-stu-id="713fc-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="713fc-126">版本</span><span class="sxs-lookup"><span data-stu-id="713fc-126">Version</span></span><br/> | <span data-ttu-id="713fc-127">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="713fc-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="713fc-128">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="713fc-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="713fc-129">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="713fc-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="713fc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="713fc-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="713fc-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="713fc-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="713fc-132">IID</span><span class="sxs-lookup"><span data-stu-id="713fc-132">IID</span></span><br/>     | <span data-ttu-id="713fc-133">IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="713fc-133">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




