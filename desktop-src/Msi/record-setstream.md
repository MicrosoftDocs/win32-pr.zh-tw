---
description: Record 物件的 SetStream 方法會將指定之檔案的內容複寫到指定的記錄欄位中，做為資料流程資料。 資料流程資料無法插入暫存欄位。
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: SetStream 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987880"
---
# <a name="recordsetstream-method"></a><span data-ttu-id="91fde-104">SetStream 方法</span><span class="sxs-lookup"><span data-stu-id="91fde-104">Record.SetStream method</span></span>

<span data-ttu-id="91fde-105">[**Record**](record-object.md)物件的 **SetStream** 方法會將指定之檔案的內容複寫到指定的記錄欄位中，做為資料流程資料。</span><span class="sxs-lookup"><span data-stu-id="91fde-105">The **SetStream** method of the [**Record**](record-object.md) object copies the content of the specified file into the designated record field as stream data.</span></span> <span data-ttu-id="91fde-106">資料流程資料無法插入暫存欄位。</span><span class="sxs-lookup"><span data-stu-id="91fde-106">Stream data cannot be inserted into temporary fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="91fde-107">語法</span><span class="sxs-lookup"><span data-stu-id="91fde-107">Syntax</span></span>


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a><span data-ttu-id="91fde-108">參數</span><span class="sxs-lookup"><span data-stu-id="91fde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91fde-109">*領域*</span><span class="sxs-lookup"><span data-stu-id="91fde-109">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="91fde-110">記錄中值的必要欄位編號（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="91fde-110">Required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="91fde-111">*filePath*</span><span class="sxs-lookup"><span data-stu-id="91fde-111">*filePath*</span></span> 
</dt> <dd>

<span data-ttu-id="91fde-112">要複製之檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="91fde-112">The location of the file to copy.</span></span> <span data-ttu-id="91fde-113">不會執行任何類型的轉譯。</span><span class="sxs-lookup"><span data-stu-id="91fde-113">No translation of any type is performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91fde-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="91fde-114">Return value</span></span>

<span data-ttu-id="91fde-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="91fde-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91fde-116">備註</span><span class="sxs-lookup"><span data-stu-id="91fde-116">Remarks</span></span>

<span data-ttu-id="91fde-117">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="91fde-117">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91fde-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="91fde-118">Requirements</span></span>



| <span data-ttu-id="91fde-119">需求</span><span class="sxs-lookup"><span data-stu-id="91fde-119">Requirement</span></span> | <span data-ttu-id="91fde-120">值</span><span class="sxs-lookup"><span data-stu-id="91fde-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91fde-121">版本</span><span class="sxs-lookup"><span data-stu-id="91fde-121">Version</span></span><br/> | <span data-ttu-id="91fde-122">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="91fde-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="91fde-123">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="91fde-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="91fde-124">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="91fde-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="91fde-125">DLL</span><span class="sxs-lookup"><span data-stu-id="91fde-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="91fde-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91fde-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="91fde-127">IID</span><span class="sxs-lookup"><span data-stu-id="91fde-127">IID</span></span><br/>     | <span data-ttu-id="91fde-128">IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="91fde-128">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




