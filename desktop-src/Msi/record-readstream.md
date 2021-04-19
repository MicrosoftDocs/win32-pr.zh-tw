---
description: Record 物件的 ReadStream 方法會從包含資料流程資料的記錄欄位讀取指定的位元組數目。
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: ReadStream 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998841"
---
# <a name="recordreadstream-method"></a><span data-ttu-id="fc58b-103">ReadStream 方法</span><span class="sxs-lookup"><span data-stu-id="fc58b-103">Record.ReadStream method</span></span>

<span data-ttu-id="fc58b-104">[**Record**](record-object.md)物件的 **ReadStream** 方法會從包含資料流程資料的記錄欄位讀取指定的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="fc58b-104">The **ReadStream** method of the [**Record**](record-object.md) object reads a specified number of bytes from a record field that contains stream data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc58b-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc58b-105">Syntax</span></span>


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a><span data-ttu-id="fc58b-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc58b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc58b-107">*領域*</span><span class="sxs-lookup"><span data-stu-id="fc58b-107">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="fc58b-108">記錄中值的必要欄位編號（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="fc58b-108">The required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="fc58b-109">*length* (長度)</span><span class="sxs-lookup"><span data-stu-id="fc58b-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="fc58b-110">從資料流程中讀取所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="fc58b-110">The required number of bytes to read from the stream.</span></span>

</dd> <dt>

<span data-ttu-id="fc58b-111">*format*</span><span class="sxs-lookup"><span data-stu-id="fc58b-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="fc58b-112">需要資料位元組的解讀和傳回。</span><span class="sxs-lookup"><span data-stu-id="fc58b-112">Required interpretation and return of the data bytes.</span></span>



| <span data-ttu-id="fc58b-113">參數名稱</span><span class="sxs-lookup"><span data-stu-id="fc58b-113">Parameter name</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="fc58b-114">意義</span><span class="sxs-lookup"><span data-stu-id="fc58b-114">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <span data-ttu-id="fc58b-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fc58b-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="fc58b-116">長度必須是1到4的長整數。</span><span class="sxs-lookup"><span data-stu-id="fc58b-116">As a long integer the length must be 1 to 4.</span></span><br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <span data-ttu-id="fc58b-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fc58b-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="fc58b-118">以 **BSTR** 表示的資料，每個字元一個位元組。</span><span class="sxs-lookup"><span data-stu-id="fc58b-118">The data as a **BSTR**—one byte per character.</span></span><br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <span data-ttu-id="fc58b-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fc58b-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="fc58b-120">ANSI 位元組已轉譯成 Unicode **BSTR**。</span><span class="sxs-lookup"><span data-stu-id="fc58b-120">The ANSI bytes translated to a Unicode **BSTR**.</span></span><br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <span data-ttu-id="fc58b-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fc58b-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="fc58b-122">直接傳回為 **BSTR** 的位元組配對。</span><span class="sxs-lookup"><span data-stu-id="fc58b-122">The byte pairs that are returned directly as a **BSTR**.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc58b-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc58b-123">Return value</span></span>

<span data-ttu-id="fc58b-124">這個方法會傳回字串，其中包含從記錄欄位讀取之要求的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="fc58b-124">This method returns a string that contains the requested number of bytes read from a record field.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc58b-125">備註</span><span class="sxs-lookup"><span data-stu-id="fc58b-125">Remarks</span></span>

<span data-ttu-id="fc58b-126">不存在之欄位的傳回值為空白值。</span><span class="sxs-lookup"><span data-stu-id="fc58b-126">The returned value of a nonexistent field is an Empty value.</span></span> <span data-ttu-id="fc58b-127">如果資料流程的位元組數少於所要求的數目，則傳回的字串會適當地縮短。</span><span class="sxs-lookup"><span data-stu-id="fc58b-127">If the stream has fewer bytes that the count requested, the returned string is shortened appropriately.</span></span>

<span data-ttu-id="fc58b-128">如需這個方法的範例，請參閱 [將 ANSI 檔案複製到資料庫欄位](copy-ansi-file-into-a-database-field.md)。</span><span class="sxs-lookup"><span data-stu-id="fc58b-128">For an example of this method, see [Copy ANSI File Into a Database Field](copy-ansi-file-into-a-database-field.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc58b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc58b-129">Requirements</span></span>



| <span data-ttu-id="fc58b-130">需求</span><span class="sxs-lookup"><span data-stu-id="fc58b-130">Requirement</span></span> | <span data-ttu-id="fc58b-131">值</span><span class="sxs-lookup"><span data-stu-id="fc58b-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc58b-132">版本</span><span class="sxs-lookup"><span data-stu-id="fc58b-132">Version</span></span><br/> | <span data-ttu-id="fc58b-133">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="fc58b-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc58b-134">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="fc58b-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc58b-135">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fc58b-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fc58b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fc58b-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc58b-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc58b-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fc58b-138">IID</span><span class="sxs-lookup"><span data-stu-id="fc58b-138">IID</span></span><br/>     | <span data-ttu-id="fc58b-139">IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fc58b-139">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




