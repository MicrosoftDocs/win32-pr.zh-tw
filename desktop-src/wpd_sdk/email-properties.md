---
description: Windows 可攜式裝置支援下列電子郵件屬性。
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: '電子郵件屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985569"
---
# <a name="email-properties"></a><span data-ttu-id="50f18-103">電子郵件屬性</span><span class="sxs-lookup"><span data-stu-id="50f18-103">Email Properties</span></span>

<span data-ttu-id="50f18-104">Windows 可攜式裝置支援下列電子郵件屬性。</span><span class="sxs-lookup"><span data-stu-id="50f18-104">Windows Portable Devices supports the following email properties.</span></span>



| <span data-ttu-id="50f18-105">屬性</span><span class="sxs-lookup"><span data-stu-id="50f18-105">Property</span></span>                         | <span data-ttu-id="50f18-106">VarType</span><span class="sxs-lookup"><span data-stu-id="50f18-106">VarType</span></span>        | <span data-ttu-id="50f18-107">Description</span><span class="sxs-lookup"><span data-stu-id="50f18-107">Description</span></span>                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f18-108">**WPD \_ 電子郵件 \_ 密件副本 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="50f18-108">**WPD\_EMAIL\_BCC\_LINE**</span></span>        | <span data-ttu-id="50f18-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="50f18-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="50f18-110">電子郵件訊息的密件副本收件者。</span><span class="sxs-lookup"><span data-stu-id="50f18-110">The BCC recipients of the e-mail message.</span></span> <span data-ttu-id="50f18-111">密件副本收件者會收到電子郵件的副本，但其名稱不會顯示為收件者。</span><span class="sxs-lookup"><span data-stu-id="50f18-111">BCC recipients receive a copy of the e-mail, but their names are not displayed as recipients.</span></span>   |
| <span data-ttu-id="50f18-112">**WPD \_ 電子郵件 \_ 抄送 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="50f18-112">**WPD\_EMAIL\_CC\_LINE**</span></span>         | <span data-ttu-id="50f18-113">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="50f18-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="50f18-114">電子郵件訊息的抄送收件者。</span><span class="sxs-lookup"><span data-stu-id="50f18-114">The CC recipients of the e-mail message.</span></span> <span data-ttu-id="50f18-115">CC 收件者會收到一份電子郵件訊息，而其名稱會顯示為收件者。</span><span class="sxs-lookup"><span data-stu-id="50f18-115">CC recipients receive a copy of the e-mail message, and their names are displayed as recipients.</span></span> |
| <span data-ttu-id="50f18-116">**WPD \_ 電子郵件 \_ 有 \_ 附件**</span><span class="sxs-lookup"><span data-stu-id="50f18-116">**WPD\_EMAIL\_HAS\_ATTACHMENTS**</span></span> | <span data-ttu-id="50f18-117">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="50f18-117">**VT\_BOOL**</span></span>   | <span data-ttu-id="50f18-118">布林值，指定此電子郵件訊息是否有附件。</span><span class="sxs-lookup"><span data-stu-id="50f18-118">A Boolean value that specifies whether this e-mail message has attachments.</span></span>                                                               |
| <span data-ttu-id="50f18-119">**已 \_ 閱讀 WPD 電子郵件 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="50f18-119">**WPD\_EMAIL\_HAS\_BEEN\_READ**</span></span>  | <span data-ttu-id="50f18-120">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="50f18-120">**VT\_BOOL**</span></span>   | <span data-ttu-id="50f18-121">指定是否已讀取此電子郵件訊息的布林值。</span><span class="sxs-lookup"><span data-stu-id="50f18-121">A Boolean value that specifies whether this e-mail message has been read.</span></span>                                                                 |
| <span data-ttu-id="50f18-122">**WPD \_ 電子郵件 \_ 收到 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="50f18-122">**WPD\_EMAIL\_RECEIVED\_TIME**</span></span>   | <span data-ttu-id="50f18-123">**VT \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="50f18-123">**VT\_DATE**</span></span>   | <span data-ttu-id="50f18-124">值，指定接收電子郵件訊息的時間。</span><span class="sxs-lookup"><span data-stu-id="50f18-124">A value that specifies when the e-mail message was received.</span></span>                                                                              |
| <span data-ttu-id="50f18-125">**WPD \_ 電子郵件 \_ 寄件者 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="50f18-125">**WPD\_EMAIL\_SENDER\_ADDRESS**</span></span>  | <span data-ttu-id="50f18-126">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="50f18-126">**VT\_LPWSTR**</span></span> | <span data-ttu-id="50f18-127">寄件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="50f18-127">The e-mail address of the sender.</span></span>                                                                                                         |
| <span data-ttu-id="50f18-128">**WPD \_ 電子郵件 \_ 到 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="50f18-128">**WPD\_EMAIL\_TO\_LINE**</span></span>         | <span data-ttu-id="50f18-129">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="50f18-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="50f18-130">電子郵件訊息的主要收件者。</span><span class="sxs-lookup"><span data-stu-id="50f18-130">The main recipients of the e-mail message.</span></span>                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="50f18-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="50f18-131">Requirements</span></span>



| <span data-ttu-id="50f18-132">需求</span><span class="sxs-lookup"><span data-stu-id="50f18-132">Requirement</span></span> | <span data-ttu-id="50f18-133">值</span><span class="sxs-lookup"><span data-stu-id="50f18-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f18-134">標頭</span><span class="sxs-lookup"><span data-stu-id="50f18-134">Header</span></span><br/> | <dl> <span data-ttu-id="50f18-135"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="50f18-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50f18-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50f18-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f18-137">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="50f18-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




