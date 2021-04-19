---
description: 以 base64 編碼字串。
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Base64Encode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994656"
---
# <a name="utilitiesbase64encode-method"></a><span data-ttu-id="3cb1f-103">Base64Encode 方法</span><span class="sxs-lookup"><span data-stu-id="3cb1f-103">Utilities.Base64Encode method</span></span>

<span data-ttu-id="3cb1f-104">\[**Base64Encode** 方法可用於 [需求] 區段中指定的作業系統。\]</span><span class="sxs-lookup"><span data-stu-id="3cb1f-104">\[The **Base64Encode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="3cb1f-105">**Base64Encode** 方法會將字串編碼為 base64。</span><span class="sxs-lookup"><span data-stu-id="3cb1f-105">The **Base64Encode** method encodes a string as base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb1f-106">語法</span><span class="sxs-lookup"><span data-stu-id="3cb1f-106">Syntax</span></span>


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a><span data-ttu-id="3cb1f-107">參數</span><span class="sxs-lookup"><span data-stu-id="3cb1f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb1f-108">*SrcString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cb1f-108">*SrcString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb1f-109">要以 base64 編碼的字串。</span><span class="sxs-lookup"><span data-stu-id="3cb1f-109">The string to encode as base64.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb1f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cb1f-110">Return value</span></span>

<span data-ttu-id="3cb1f-111">Base64 編碼的字串。</span><span class="sxs-lookup"><span data-stu-id="3cb1f-111">The base64-encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb1f-112">備註</span><span class="sxs-lookup"><span data-stu-id="3cb1f-112">Remarks</span></span>

<span data-ttu-id="3cb1f-113">Base64 編碼是用來傳輸二進位資料的配置。</span><span class="sxs-lookup"><span data-stu-id="3cb1f-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="3cb1f-114">Base64 以24位群組的形式處理資料，將此資料對應到四個編碼的字元。</span><span class="sxs-lookup"><span data-stu-id="3cb1f-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="3cb1f-115">Base64 編碼有時稱為「3對4編碼」。</span><span class="sxs-lookup"><span data-stu-id="3cb1f-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="3cb1f-116">24位群組的每6位都是用來做為對應表的索引， (base64 字母) 來取得編碼資料的字元。</span><span class="sxs-lookup"><span data-stu-id="3cb1f-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="3cb1f-117">編碼的資料行長度限制為76個字元。</span><span class="sxs-lookup"><span data-stu-id="3cb1f-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb1f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cb1f-118">Requirements</span></span>



| <span data-ttu-id="3cb1f-119">需求</span><span class="sxs-lookup"><span data-stu-id="3cb1f-119">Requirement</span></span> | <span data-ttu-id="3cb1f-120">值</span><span class="sxs-lookup"><span data-stu-id="3cb1f-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb1f-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="3cb1f-121">Redistributable</span></span><br/> | <span data-ttu-id="3cb1f-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3cb1f-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3cb1f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3cb1f-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="3cb1f-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cb1f-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb1f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cb1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb1f-126">**公用程式**</span><span class="sxs-lookup"><span data-stu-id="3cb1f-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




