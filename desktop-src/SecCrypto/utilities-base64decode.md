---
description: 從 base64 解碼字串。
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Base64Decode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993343"
---
# <a name="utilitiesbase64decode-method"></a><span data-ttu-id="acad2-103">Base64Decode 方法</span><span class="sxs-lookup"><span data-stu-id="acad2-103">Utilities.Base64Decode method</span></span>

<span data-ttu-id="acad2-104">\[**Base64Decode** 方法可用於 [需求] 區段中指定的作業系統。\]</span><span class="sxs-lookup"><span data-stu-id="acad2-104">\[The **Base64Decode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="acad2-105">**Base64Decode** 方法會從 base64 解碼字串。</span><span class="sxs-lookup"><span data-stu-id="acad2-105">The **Base64Decode** method decodes a string from base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="acad2-106">語法</span><span class="sxs-lookup"><span data-stu-id="acad2-106">Syntax</span></span>


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a><span data-ttu-id="acad2-107">參數</span><span class="sxs-lookup"><span data-stu-id="acad2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acad2-108">*EncodedString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="acad2-108">*EncodedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acad2-109">要解碼的 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="acad2-109">The base64-encoded string to decode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acad2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="acad2-110">Return value</span></span>

<span data-ttu-id="acad2-111">解碼的字串。</span><span class="sxs-lookup"><span data-stu-id="acad2-111">The decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="acad2-112">備註</span><span class="sxs-lookup"><span data-stu-id="acad2-112">Remarks</span></span>

<span data-ttu-id="acad2-113">Base64 編碼是用來傳輸二進位資料的配置。</span><span class="sxs-lookup"><span data-stu-id="acad2-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="acad2-114">Base64 以24位群組的形式處理資料，將此資料對應到四個編碼的字元。</span><span class="sxs-lookup"><span data-stu-id="acad2-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="acad2-115">Base64 編碼有時稱為「3對4編碼」。</span><span class="sxs-lookup"><span data-stu-id="acad2-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="acad2-116">24位群組的每6位都是用來做為對應表的索引， (base64 字母) 來取得編碼資料的字元。</span><span class="sxs-lookup"><span data-stu-id="acad2-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="acad2-117">編碼的資料行長度限制為76個字元。</span><span class="sxs-lookup"><span data-stu-id="acad2-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="acad2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="acad2-118">Requirements</span></span>



| <span data-ttu-id="acad2-119">需求</span><span class="sxs-lookup"><span data-stu-id="acad2-119">Requirement</span></span> | <span data-ttu-id="acad2-120">值</span><span class="sxs-lookup"><span data-stu-id="acad2-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="acad2-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="acad2-121">Redistributable</span></span><br/> | <span data-ttu-id="acad2-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="acad2-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="acad2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="acad2-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="acad2-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acad2-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acad2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acad2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acad2-126">**公用程式**</span><span class="sxs-lookup"><span data-stu-id="acad2-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




