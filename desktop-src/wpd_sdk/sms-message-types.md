---
description: SMS \_ 訊息 \_ 類型列舉類型會描述短訊息服務的內容類型 (SMS) 訊息。
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: 'SMS_MESSAGE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977658"
---
# <a name="sms_message_types-enumeration"></a><span data-ttu-id="656de-103">SMS \_ 訊息 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="656de-103">SMS\_MESSAGE\_TYPES enumeration</span></span>

<span data-ttu-id="656de-104">**Sms \_ 訊息 \_ 類型** 列舉類型會描述短訊息服務的內容類型 (SMS) 訊息。</span><span class="sxs-lookup"><span data-stu-id="656de-104">The **SMS\_MESSAGE\_TYPES** enumeration type describes the content type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="656de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="656de-105">Syntax</span></span>


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="656de-106">常數</span><span class="sxs-lookup"><span data-stu-id="656de-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="656de-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS \_ 文字 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="656de-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS\_TEXT\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="656de-108">文字訊息。</span><span class="sxs-lookup"><span data-stu-id="656de-108">A text message.</span></span>

</dd> <dt>

<span data-ttu-id="656de-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS \_ 二進位 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="656de-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS\_BINARY\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="656de-110">二進位訊息。</span><span class="sxs-lookup"><span data-stu-id="656de-110">A binary message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="656de-111">備註</span><span class="sxs-lookup"><span data-stu-id="656de-111">Remarks</span></span>

<span data-ttu-id="656de-112">[**WPD \_ 命令 \_ SMS \_ SEND 命令**](wpd-command-sms-send-command.md)會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="656de-112">This enumeration is used by the [**WPD\_COMMAND\_SMS\_SEND Command**](wpd-command-sms-send-command.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="656de-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="656de-113">Requirements</span></span>



| <span data-ttu-id="656de-114">需求</span><span class="sxs-lookup"><span data-stu-id="656de-114">Requirement</span></span> | <span data-ttu-id="656de-115">值</span><span class="sxs-lookup"><span data-stu-id="656de-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="656de-116">標頭</span><span class="sxs-lookup"><span data-stu-id="656de-116">Header</span></span><br/> | <dl> <span data-ttu-id="656de-117"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="656de-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656de-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="656de-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656de-119">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="656de-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




