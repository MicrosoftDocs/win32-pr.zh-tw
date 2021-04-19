---
description: WPD \_ sms \_ 編碼 \_ 類型列舉類型會描述短訊息服務 (SMS) 訊息的編碼類型。
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: 'WPD_SMS_ENCODING_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994836"
---
# <a name="wpd_sms_encoding_types-enumeration"></a><span data-ttu-id="c7894-103">WPD \_ SMS \_ 編碼 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="c7894-103">WPD\_SMS\_ENCODING\_TYPES enumeration</span></span>

<span data-ttu-id="c7894-104">**WPD \_ sms \_ 編碼 \_ 類型** 列舉類型會描述短訊息服務 (SMS) 訊息的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="c7894-104">The **WPD\_SMS\_ENCODING\_TYPES** enumeration type describes the encoding type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7894-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7894-105">Syntax</span></span>


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="c7894-106">常數</span><span class="sxs-lookup"><span data-stu-id="c7894-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c7894-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS \_ 編碼 \_ 7 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="c7894-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS\_ENCODING\_7\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="c7894-108">七位編碼。</span><span class="sxs-lookup"><span data-stu-id="c7894-108">Seven-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="c7894-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS \_ 編碼 \_ 8 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="c7894-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS\_ENCODING\_8\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="c7894-110">八位編碼。</span><span class="sxs-lookup"><span data-stu-id="c7894-110">Eight-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="c7894-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS \_ 編碼 \_ utf-16 \_**</span><span class="sxs-lookup"><span data-stu-id="c7894-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS\_ENCODING\_UTF\_16**</span></span>
</dt> <dd>

<span data-ttu-id="c7894-112"> (UTF) 的十六位編碼。</span><span class="sxs-lookup"><span data-stu-id="c7894-112">Sixteen-bit encoding (UTF).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7894-113">備註</span><span class="sxs-lookup"><span data-stu-id="c7894-113">Remarks</span></span>

<span data-ttu-id="c7894-114">此列舉是由 [WPD \_ SMS \_ ENCODING](sms-properties.md) 屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="c7894-114">This enumeration is used by the [WPD\_SMS\_ENCODING](sms-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7894-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7894-115">Requirements</span></span>



| <span data-ttu-id="c7894-116">需求</span><span class="sxs-lookup"><span data-stu-id="c7894-116">Requirement</span></span> | <span data-ttu-id="c7894-117">值</span><span class="sxs-lookup"><span data-stu-id="c7894-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7894-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c7894-118">Header</span></span><br/> | <dl> <span data-ttu-id="c7894-119"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7894-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7894-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7894-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7894-121">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="c7894-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




